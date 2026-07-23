---
name: echarts
description: Build, debug, and review Apache ECharts visualizations in HTML, JavaScript, TypeScript, React, Vue, dashboards, and data reports. Use when the user asks for ECharts, Apache ECharts, chart options, chart configuration, line/bar/pie/scatter/map/heatmap/treemap/sankey/graph charts, dataset/encode, tooltip/legend/dataZoom/visualMap, responsive chart resize, chart lifecycle cleanup, event handling, accessibility/aria, performance for large chart data, ECharts v6 migration, or installing/using echarts from npm/CDN.
---

# Apache ECharts

Use this skill when creating, modifying, debugging, or reviewing Apache ECharts code. Prefer project-native patterns, but keep ECharts option objects structured, data-driven, responsive, and easy to inspect.

## Source Priority

Use official ECharts docs for unstable or version-sensitive details:

- Install/import: https://echarts.apache.org/handbook/en/basics/import/
- Option reference: https://echarts.apache.org/en/option.html
- API reference: https://echarts.apache.org/en/api.html
- Dataset: https://echarts.apache.org/handbook/en/concepts/dataset/
- Events: https://echarts.apache.org/handbook/en/concepts/event/
- Accessibility: https://echarts.apache.org/handbook/en/best-practices/aria/
- ECharts 6 upgrade: https://echarts.apache.org/handbook/en/basics/release-note/v6-upgrade-guide/

When the user asks for latest ECharts behavior, verify against official docs or the package metadata before answering.

## Install

For application projects, install from npm:

```bash
npm install echarts
```

Use a pinned version when the user asks for one, for example:

```bash
npm install echarts@6.1.0
```

For standalone HTML demos, use a CDN or a checked-in local build. Do not treat `apache/echarts/dist` as a Codex skill; it contains browser/module build artifacts, not `SKILL.md`.

## Import Strategy

Use the simple import for prototypes, small apps, or when bundle size is not a concern:

```ts
import * as echarts from "echarts";
```

Use the modular import for production apps where bundle size matters:

```ts
import * as echarts from "echarts/core";
import { BarChart, LineChart } from "echarts/charts";
import {
  GridComponent,
  LegendComponent,
  TooltipComponent,
  DatasetComponent,
  DataZoomComponent,
  AriaComponent
} from "echarts/components";
import { CanvasRenderer } from "echarts/renderers";

echarts.use([
  BarChart,
  LineChart,
  GridComponent,
  LegendComponent,
  TooltipComponent,
  DatasetComponent,
  DataZoomComponent,
  AriaComponent,
  CanvasRenderer
]);
```

Include every chart, component, feature, and renderer used by the option. Missing modular imports are a common cause of blank charts.

## Core Workflow

1. Inspect the container dimensions. ECharts needs a real width and height before `init`.
2. Normalize data first. Prefer `dataset.source` plus `series.encode` when data is tabular or reused across series.
3. Build a complete `option` with `title`, `tooltip`, `legend`, axes/coordinates, dataset, and series.
4. Call `chart.setOption(option)` after `echarts.init(container)`.
5. Add resize handling with `ResizeObserver` or a debounced window resize.
6. Dispose on unmount or page teardown with `chart.dispose()`.

## Option Structure

Prefer this order for readable options:

```ts
const option = {
  title: { text: "Revenue by Month" },
  tooltip: { trigger: "axis" },
  legend: {},
  grid: { left: 40, right: 24, top: 56, bottom: 40, containLabel: true },
  dataset: { source: rows },
  xAxis: { type: "category" },
  yAxis: { type: "value" },
  series: [
    { type: "bar", encode: { x: "month", y: "revenue" } }
  ],
  aria: { enabled: true }
};
```

Use `notMerge: true` when replacing incompatible option shapes, such as changing chart type, coordinate system, or series count:

```ts
chart.setOption(nextOption, { notMerge: true });
```

Use `replaceMerge: ["series"]` when preserving global components while replacing series.

## Data Modeling

Prefer `dataset` for table-like data:

```ts
dataset: {
  source: [
    { month: "Jan", revenue: 120, cost: 80 },
    { month: "Feb", revenue: 160, cost: 90 }
  ]
},
series: [
  { name: "Revenue", type: "line", encode: { x: "month", y: "revenue" } },
  { name: "Cost", type: "line", encode: { x: "month", y: "cost" } }
]
```

Use `series.data` directly only for small one-off charts or series-specific structures, such as graph nodes/links, sankey links, candlestick OHLC arrays, or map regions.

## Framework Lifecycle

React:

- Initialize in `useEffect` or a client-only hook after the DOM node exists.
- Store the chart instance in a ref.
- Use `ResizeObserver` for responsive containers.
- Remove observers/listeners and call `chart.dispose()` in cleanup.
- Avoid calling `echarts.init` during SSR.

Vue/Svelte:

- Initialize in `onMounted` / `onMount`.
- Update with `setOption` when data changes.
- Dispose in `onUnmounted` / returned cleanup.

If the container can be hidden, tabbed, or initially zero-sized, call `chart.resize()` after it becomes visible.

## Events and Actions

Bind events on the chart instance:

```ts
chart.on("click", (params) => {
  console.log(params.seriesName, params.name, params.value);
});
```

Use lowercase DOM-style event names (`click`, `mouseover`) and documented component events such as `legendselectchanged` and `datazoom`. Unbind long-lived handlers on teardown:

```ts
chart.off("click", handler);
```

Use `dispatchAction` for programmatic interactions such as highlighting, selecting legends, showing tooltips, or data zooming.

## Responsiveness

Prefer `ResizeObserver` over only listening to `window.resize` because dashboard panels often resize without viewport changes:

```ts
const observer = new ResizeObserver(() => chart.resize());
observer.observe(container);
```

Always give the container a stable height. A blank chart is often a zero-height container, not an ECharts option problem.

## Accessibility

Add `aria` when charts communicate important information. With modular imports, register `AriaComponent` or `aria` settings will not work:

```ts
aria: {
  enabled: true,
  decal: { show: true }
}
```

For critical dashboards, provide adjacent text summaries or tables. Do not rely on color alone; use labels, symbols, patterns, or clear legends.

## Performance

- For large datasets, use Canvas renderer first; consider SVG for small charts needing crisp DOM/SVG output.
- Use `large`, `largeThreshold`, `progressive`, or sampling options only when supported by the selected series.
- Avoid recreating chart instances on every render. Reuse the instance and call `setOption`.
- Avoid huge labels on every point. Use tooltip, emphasis, or sampled labels instead.
- Use `dataZoom`, aggregation, downsampling, or server-side pre-aggregation for dense time series.
- Prefer stable object construction and minimal option changes in reactive frameworks.

## Debug Checklist

For blank or broken charts, check in this order:

1. Container exists and has non-zero width/height.
2. ECharts JS/module is loaded and `echarts.init` is available.
3. Modular imports include the chart type, components, and renderer.
4. The option uses valid series `type`, axes, coordinates, and data shape.
5. `setOption` runs after initialization.
6. Console has no import, runtime, or invalid DOM errors.
7. Hidden containers call `resize()` when shown.
8. Old instances are not stacked on the same DOM node.

## References

For reusable snippets and framework templates, read `references/patterns.md`.
