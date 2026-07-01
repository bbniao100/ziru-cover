# Generation Prompt Pack

Use this reference when the current agent cannot directly generate or edit images, or when the user wants prompts for ChatGPT Image, image2, or another official image-generation interface.

## Principle

Do not say that an image was created when no image tool is available. Deliver a ready-to-use prompt pack that preserves the same design intelligence:

- Click reason
- Main image role
- Layout model
- Text hierarchy
- Visual path
- Platform ratio
- Chinese text handling
- Negative constraints

## Prompt Pack Structure

For each variant, output this structure:

```text
版本名：
适用目标：
点击理由：

给图像模型的提示词：
请基于我上传的主图，设计一张中文社交媒体高点击封面。画面比例为 [ratio]。保留主图中 [person/object/scene] 的真实身份和核心姿态，优化构图、光线、背景干净度和视觉冲击力。

版式要求：
- 第一眼看到：[primary visual]
- 主标题区域：[position, size, relationship to face/object]
- 副标题区域：[position]
- 标签/小字：[position and function]
- 留白：[where and why]
- 视线路径：[first -> second -> third]

风格要求：
- 风格：[magazine/editorial/high-impact/clean/professional/etc.]
- 色彩：[attention color + neutral base + support color]
- 字体感觉：[bold sans/display/editorial; do not request exact unavailable fonts]
- 质感：[clean, premium, paper, poster, course cover, etc.]

需要出现的文字：
主标题：[exact Chinese text]
副标题：[exact Chinese text]
标签：[exact Chinese text]

重要文字规则：
中文必须准确、清晰、可读。如果模型无法稳定生成中文，请先生成无文字版背景和版式空间，把文字区域留空，之后再手动排中文字。

避免：
[negative list]

输出要求：
生成 [ratio] 封面，移动端信息流可读，主标题在缩略图中清楚，人物/主物体不被裁切，不要添加错误中文、乱码、伪文字或无关装饰。
```

## Chinese Text Strategy

Prefer one of two strategies:

- **Text-in-image**: Use when the user specifically wants the image tool to include text and the model is known to handle Chinese well.
- **No-text background + overlay plan**: Use by default for reliability. Ask the image tool to leave clean text zones, then provide exact overlay instructions for Canva, Photoshop, Figma, CapCut, Jianying, or another editor.

When using the no-text strategy, include this extra block:

```text
后期加字方案：
- 主标题：[text], place at [position], large bold, color [color], line break [break]
- 副标题：[text], place at [position], color [color], size about [relative size]
- 标签/小字：[text], place at [position], low contrast, decorative only
- 色块/底板：[shape/color/opacity], behind [title/support line]
```

## Prompt Writing Rules

- Mention the uploaded main image as the base image.
- Specify what to preserve: face, expression, gesture, object, brand cues, or scene.
- Specify what to improve: background cleanup, contrast, crop, lighting, title space, color block, poster feeling.
- Keep one primary cover idea per prompt.
- Avoid overloading the prompt with too many decorative elements.
- State the platform ratio explicitly.
- Include exact Chinese copy separately from the visual description.

## Negative List Examples

Use a concise avoid list:

- no garbled Chinese text
- no pseudo-characters
- no extra fingers or distorted hands
- no changed face identity
- no unrelated people
- no cluttered background
- no tiny unreadable main title
- no random logos or watermarks
- no heavy blur over the subject

## Default Variant Set

If the user did not ask for a different number, produce:

1. **Click-first prompt**: louder title, stronger color block, clearer pain/result.
2. **Professional-first prompt**: cleaner layout, stronger trust, magazine/editorial feel.
3. **Conversion-first prompt**: visible proof/result/action cue, but still one main hook.
