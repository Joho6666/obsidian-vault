---
name: ai-experiment-report-zh
description: Use this skill when the user needs help completing Chinese AI course experiment homework end-to-end: read an experiment guide or lab manual, choose easier experiments, run AI web experiments with personal info in prompts, preserve screenshots, and fill a school experiment-report template into final DOCX/PDF deliverables.
---

# AI Experiment Report ZH

## Overview

Use this skill for Chinese course assignments built around AI tools, experiment guides, and report templates. It is designed for jobs like: reading a `实验指导书`, choosing 3 to 4 feasible experiments, actually running DeepSeek or Doubao style tasks, preserving screenshots with the student's personal information visible, and producing a final report in the teacher's template.

Read only the reference file you need:

- For the full workflow, read [references/workflow.md](references/workflow.md).
- For ready-made Chinese prompt structures, read [references/prompt-templates.md](references/prompt-templates.md).
- For report formatting, screenshots, and template rules, read [references/report-rules.md](references/report-rules.md).

## Quick Trigger Cases

Use this skill when the user says or implies any of the following:

- “帮我读实验指导书，然后选实验来做”
- “把个人信息加进提示词里，做实验并截图”
- “把实验内容套进实验报告模板”
- “生成一份可直接交的 AI 实验报告”
- “以后类似课程作业也按这个流程做”

## Workflow

Follow this order unless the user explicitly asks for a different sequence:

1. Read the experiment guide and identify all candidate experiments.
2. Choose the easiest experiments first.
3. Confirm or collect personal info needed in prompts and report fields.
4. Run the experiments in the browser where possible.
5. Preserve screenshots that visibly contain the user's personal info and generated results.
6. Draft Markdown notes for each experiment.
7. Fill the school template and export final `docx` and, if possible, `pdf`.

Detailed execution rules are in [references/workflow.md](references/workflow.md).

## Tooling Rules

- Prefer the `documents` skill/plugin for final document generation and edits.
- Prefer the in-app browser workflow when the user wants real experiment process screenshots.
- If a provided report template is `.doc`, convert it to `.docx` before deterministic edits.
- If a site login is required, pause only for login; continue immediately after the user logs in.
- If Chinese text cannot be reliably auto-typed into a site input box, ask the user to paste the prepared prompt once, then resume automation from submission onward.

## Deliverable Rules

- Final reports should preserve the teacher's template structure unless the user asks for a redesign.
- Prefer screenshots that show:
  - the personal-info prompt,
  - the generated answer or image result,
  - and, when available, the optimization follow-up step.
- If multiple screenshots exist, prefer “过程图 + 结果图” over only final result images.
- When the teacher's template is strict, prioritize template fidelity over visual embellishment.

## Validation

Before finishing, verify:

1. The selected experiments do come from the provided guide.
2. Personal info appears in both prompts and report fields where required.
3. Screenshots used in the report are the best available ones with visible personal info.
4. The output document contains the correct experiment titles, dates, class, name, and student ID.
5. The final deliverable exists as a `.docx`; export a `.pdf` too when the environment supports it.
