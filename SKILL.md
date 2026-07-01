---
name: ziru-cover
description: Create Ziru-style high-click, conversion-oriented Chinese social media cover images or complete image-generation prompt packs from a video script, topic, and main image. Use when Codex is asked to design or improve a main image, thumbnail, cover, 小红书封面, 抖音/视频号封面, 公众号主图, 课程/训练营推广封面, or when the user says 子儒封面, 子儒主图, 子儒高点击封面, 高点击封面, 主图设计, 脚本加主图做封面, 一眼想点, 文字很多怎么排版, or wants reusable cover variants optimized for click-through and conversion. If image-generation/editing tools are unavailable, output complete prompts and layout specs for the user to paste into ChatGPT Image or another official image-generation interface.
---

# Ziru Cover

## Operating Principle

Design the cover as a decision system, not as decoration. Convert the script and main image into a clear click reason, then build a visual path that lets a mobile user stop, understand, and want to click.

Default to action. If the user provides a script/topic and a main image, do not ask for more information before producing useful directions or drafts. Ask only when the script or main image is missing, the platform/dimensions are impossible to infer, or the user requests a specific brand constraint that is unavailable.

## Interaction Modes

Use one of these modes based on the user's request:

- **Fast mode**: Use when the user wants weekly or routine production. Produce 3 cover directions directly: click-first, professional-first, and conversion-first.
- **Co-creation mode**: Use when the cover is important, commercial, or the user asks to choose first. Present 3 strategic directions with title hierarchy and layout notes, then wait for selection before making final assets.
- **Review mode**: Use when the user provides existing covers or performance data. Diagnose click reason, information hierarchy, visual path, small-screen readability, and conversion signal. Recommend precise changes.

If the user does not specify a mode, use Fast mode.

## Required Inputs

Prefer these inputs, but proceed with reasonable assumptions when possible:

- Video script or topic
- Main image or screenshot
- Platform and size, if known
- Goal: clicks, followers, private messages, course signups, trust, or sales
- Account positioning and style preferences, if known

Default assumptions: Chinese social media cover, mobile-first, high readability, 3:4 or 4:5 for Xiaohongshu-style feeds unless the user asks for 9:16 video cover.

## Workflow

1. **Extract the click reason**
   - Identify the audience pain, desired result, contradiction, curiosity gap, identity signal, or concrete benefit.
   - Pick one primary click reason. Do not let the cover argue multiple ideas at the same strength.

2. **Create the text hierarchy**
   - Write 3-5 title sets.
   - For each set, split copy into: main hook, support line, label, and optional atmosphere text.
   - Keep the main hook short enough to survive small-screen preview.

3. **Select a layout model**
   - Choose a model from `references/layout-patterns.md`.
   - Match the model to the input image: face direction, hand gesture, object position, background clutter, empty space, and emotional tone.

4. **Design the visual path**
   - Decide what is seen first, second, and third.
   - Use face, gaze, gesture, object, color block, alignment, and contrast to guide attention.
   - Separate image area, text area, white space, and decorative micro-information.

5. **Produce variants**
   - Fast mode default: produce 3 variants.
   - Name each variant by strategy, not style alone: click-first, professional-first, conversion-first.
   - Explain each variant with: click reason, title hierarchy, layout, color/typography, and why it should work.

6. **Choose the production path**
   - **Direct image path**: If image-generation or image-editing tools are available, use them to generate or edit the cover. Prefer deterministic/local text layout for Chinese words when possible.
   - **Prompt-pack path**: If image-generation or image-editing tools are unavailable, do not pretend to create an image. Read `references/generation-prompt-pack.md` and output complete prompt packs the user can paste into ChatGPT Image or another official image-generation interface.
   - In both paths, include exact title text, layout placement, color direction, crop ratio, and quality-check notes.

7. **Quality-check before delivery**
   - Read `references/quality-checklist.md`.
   - Verify small-screen readability, one dominant message, visual path, platform crop safety, contrast, and conversion cue.

## Reference Loading

- Read `references/cover-theory.md` when deciding click strategy, title hierarchy, or what theory to apply.
- Read `references/layout-patterns.md` when choosing or explaining layout models.
- Read `references/generation-prompt-pack.md` when the agent cannot directly generate/edit images, when the user asks for prompts, or when handing off to ChatGPT Image / image2 / another official image tool.
- Read `references/quality-checklist.md` before finalizing, reviewing, or comparing cover options.

## Output Format

For strategy-only requests, return:

- Best click reason
- 3 title hierarchy options
- 3 cover directions with layout notes
- Recommended direction and reason

For asset-generation requests, return:

- Generated file paths or image previews
- Variant names and intended use
- Short quality-check summary
- Any limitations, especially if Chinese text rendering was not deterministic

For no-image-tool environments, return:

- 3 complete image-generation prompt packs
- A separate Chinese text overlay plan if text should be added after generation
- Size/crop instructions
- Negative prompt or avoid list
- A short note telling the user which prompt to try first and why

For reviews, lead with the strongest fixes first, then explain the underlying principle briefly.
