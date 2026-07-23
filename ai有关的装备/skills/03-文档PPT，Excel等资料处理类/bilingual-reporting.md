---
name: bilingual-reporting
description: "Use when generating reports, digests, briefings, summaries, or research notes that should be written in bilingual reading format for the user: English first, then the Chinese translation immediately below each paragraph or section, with a table of contents and original source links preserved."
---

# Bilingual Reporting

## Overview

Use this skill whenever the user wants a report that helps them learn English while reading information. The preferred output is a Markdown report with:

- a table of contents
- English content first
- the Chinese translation immediately below each corresponding English paragraph/section
- original source links visible on each item
- bilingual titles, tables, charts, keywords, and visual cues
- both a high-level mind map and a detailed knowledge map

## Required format

Follow this order unless the user explicitly asks otherwise:

1. Title
2. Short intro or selection summary
3. Table of contents
4. High-level bilingual mind map / 思维导图
   - Use large readable fonts.
   - Show the whole report's knowledge system at a glance.
   - Keep labels short and bilingual.
   - Use the user's preferred "learning poster" style:
     - soft gradient background
     - large centered title
     - blue central circle
     - rounded colorful topic cards around the center
     - smooth curved connector lines
     - generous spacing and padding
     - large readable fonts that remain legible inside Obsidian
5. Detailed bilingual knowledge map / 知识地图
   - Use large readable fonts and a wider visual layout.
   - Show categories, themes, and details.
   - Prefer SVG or another image-like format when Mermaid text becomes too small in Obsidian.
6. For each item:
   - English title
   - Chinese title directly below it
   - English paragraph(s)
   - Chinese title or Chinese translation line
   - Chinese paragraph(s) directly under the matching English text
   - source URL(s) and discussion link(s)
   - a bilingual keyword block at the bottom
   - an optional comparison table or chart if it helps the user understand the topic faster

## Core rules

- Keep English and Chinese aligned at the paragraph level, not as separate language sections.
- Preserve original website URLs and discussion links in the report.
- If there are multiple items, include a clickable table of contents.
- Keep Markdown clean and Obsidian-friendly.
- Prefer concise, readable translations over overly literal ones.
- If a source report is already bilingual, keep the same pairing structure when rewriting or summarizing it.
- Include both:
  - **Mind map / 思维导图**: a high-level overview of the report knowledge system.
  - **Knowledge map / 知识地图**: a larger and more detailed concept board.
- Use large readable fonts for both maps. If Obsidian scales the image down, make the text larger relative to the canvas.
- The maps should summarize concepts, categories, relationships, trade-offs, and takeaways. Do not use them to restate the report structure.
- For the high-level mind map, default to a polished learning-poster layout: gradient background, central hub, colorful rounded cards, curved connectors, and clear typography. Avoid cramped Mermaid diagrams for the main mind map unless the user explicitly asks for Mermaid.
- Add lightweight visuals when they help understanding, such as an image, chart, or comparison table.

## When editing or generating reports

- If the input is a news digest or research roundup, rewrite it into the bilingual paired format.
- If the user asks for a quick-reading version, keep the same structure but shorten each paragraph.
- If the user asks for a full version, keep all references and links intact.
- If the user wants stronger learning support, include bilingual keywords and a compact visual summary near the bottom of each item.
- If the user wants a mind map, make it a concept map or knowledge tree with categories and relationships, not an outline of the report sections.
- For daily Horizon-style digests, use the Horizon-style bilingual learning digest template in `references/horizon-daily-template.md`:
  - bilingual frontmatter
  - intro + trade-offs
  - Mind map / 思维导图
  - Knowledge map / 知识地图
  - per-item bilingual sections
  - 3 things to remember
  - learning visuals
  - bilingual keywords
  - empty-day fallback section when no items pass the threshold


## Learning summary template for the user

When the user adds new learning material, source notes, webpages, videos, papers, project notes, or Horizon items and asks to organize/summarize them, prefer the user's learning-summary structure in `references/learning-summary-template.md`.

Use this structure especially for the user's identity as a student and AI enthusiast:

- basic metadata and radar category
- one-sentence bilingual summary
- core summary
- English paragraph followed by Chinese understanding
- 3 things to remember
- key concepts table
- knowledge framework / mind map
- comparison table
- impact and study-priority judgment
- Feynman explanation
- questions
- next actions
- links to concept/source/comparison/overview notes

## Reference
See [report-format.md](references/report-format.md) for the preferred template.
