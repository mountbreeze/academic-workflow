# Academic workflow

Read papers in Chinese and prepare evidence-grounded English academic presentations with the confirmed detailed teaching and design preferences.

## Use from a new conversation

Attach the paper and any technical appendix, then paste:

> 请读取并遵循这个工作流的最新版本：  
> https://github.com/mountbreeze/academic-workflow/blob/main/skills/paper-to-presentation/SKILL.md  
> 先用中文精读这篇论文，逐步解释关键公式，再制作详细版 presentation。沿用工作流默认的蓝色主题、英文 slides、英文在上中文在下的双语 notes、编号标题、每页页码与可点击导航，并清楚呈现 key findings、implications 和适用边界。

The assistant must read the linked instructions and required relative references. A URL alone does not install a skill or guarantee automatic activation in unrelated conversations.

## If the skill is already installed

Use `$paper-to-presentation` or select Paper to Presentation in the skill picker. If it is unavailable, use the URL prompt above. An installed local copy can lag behind this repository, so ask to follow the latest GitHub version when needed.

### Read only

> 使用 $paper-to-presentation，只做中文精读，暂时不要生成 slides。先解释研究问题和直觉，再逐步推导关键公式，最后讨论主要结论、implications 和局限。

### Detailed presentation

> 使用 $paper-to-presentation，按默认要求制作详细版 presentation，不限定页数。保留完整推导，讲稿英文在上、中文在下。

### Timed presentation

> 使用 $paper-to-presentation，制作 12 分钟的英文 journal-club presentation。保持双语 notes 和蓝色主题，正文讲清核心逻辑，完整推导放附录，并保留 findings、implications 与局限。

### Revise a deck

> 使用 $paper-to-presentation，基于我上传的可编辑版本修改，保留已有改动。沿用默认样式、双语 notes 和导航，不重做已经核实的内容。

## Defaults and files

- [Workflow instructions](skills/paper-to-presentation/SKILL.md)
- [Full confirmed requirements](skills/paper-to-presentation/references/user-requirements.md)
- [Rendering and verification guide](skills/paper-to-presentation/references/rendering.md)
- [Editable Quarto template](skills/paper-to-presentation/assets/deck-template.qmd)
- [Blue theme](skills/paper-to-presentation/assets/deck.css)
- [Permanent navigation](skills/paper-to-presentation/assets/deck-nav.html)

Default presentations are detailed learning decks, not automatically limited to 12 minutes or a fixed number of slides. User-specified timing and format override the defaults. Reading-only requests do not generate presentations.

To render a project, copy all three template assets into one directory, rename the QMD to deck.qmd, fill it with verified content, then run `quarto preview deck.qmd`. Press S for speaker view. Follow the rendering guide for PDF export and verification.

Updating this repository does not automatically update a separately installed copy. The URL-based invocation explicitly loads the current workflow.
