# 电商商品主视觉设计 Skill / E-commerce Key Visual Design Skill

通过分阶段用户确认，完成电商商品海报、促销 KV 和首图的构思、制作、多语言适配与迭代，而不是收到简单需求后直接交付成稿。

Develop, produce, localize and refine product posters, campaign key visuals and hero images through staged user decisions, rather than jumping from a short brief to finished artwork.

- 调用名 / Invocation name: `ecommerce-main-visual-v4`
- 规则版本 / Rule version: `4.1.0`
- 中英对照入口 / Paired bilingual entry: [SKILL.md](SKILL.md)
- 独立中文版 / Chinese-only entry: [SKILL.zh-CN.md](SKILL.zh-CN.md)
- 独立英文版 / English-only entry: [SKILL.en.md](SKILL.en.md)

本发布包以中英对照方式呈现README与默认技能入口。参考文档在同一文件内提供中英对应内容；独立语言入口便于按工作语言读取。三份入口不需要重复加载。此次只调整发布包的语言呈现，不改变4.1.0设计流程，也不替换本机已安装技能。

This distribution pairs Chinese and English in the README and default skill entry. Reference documents provide corresponding Chinese and English content within the same file; language-specific entries support focused reading. Load only one entry. This update changes the package's language presentation, not the 4.1.0 design workflow or the locally installed skill.

## 工作流程 / Workflow

| 阶段 / Stage | 用户参与的决策 / User decision | 评审材料 / Review material |
|---|---|---|
| G1 资料与文案<br>Inputs and copy | 要说什么，哪些必须保留<br>What to communicate and what must remain | 简报、文案清单、事实与素材缺口<br>Brief, copy inventory, factual and asset gaps |
| G2 信息主次与视觉叙事<br>Hierarchy and narrative | 第一眼看什么，商品与环境如何互动<br>What to notice first and how the product interacts with its scene | 一级/二级/三级信息、场景叙事建议<br>Primary/secondary/tertiary information and scene proposal |
| G3 低保真版式<br>Low-fidelity layouts | 商品与文字如何组织<br>How to arrange the product and text | 2–3个有实质差异的视觉草图<br>2–3 genuinely different visual sketches |
| G4 真实文案与字块样式<br>Real-copy and styling proof | 换行、字体、色块及价格/CTA组合<br>Wrapping, typography, color blocks and price/CTA grouping | 选中布局的完整文案排版校样<br>Selected layout proof with all actual copy |
| G5 首稿定向反馈<br>Focused first-draft feedback | 约定效果是否实现<br>Whether the agreed objectives are achieved | 首稿、缩略预览与重点反馈问题<br>First draft, thumbnail and focused review questions |

之后执行必要的技术验收、语言适配与已授权导出。详见[分阶段协作协议](references/user-collaboration.md)。

Then perform required technical QA, localization and authorized exports. See the [staged collaboration protocol](references/user-collaboration.md).

五个接口不等于强制五轮审批：已确认节点直接沿用，相邻节点可以合并。用户明确委托“直接制作，你决定”时可走快速路径；明确的局部修改只重开相关节点。任何路径都不能编造商品事实或把未检查项标为通过。

Five interfaces do not mean five mandatory approval rounds: reuse confirmed decisions and combine adjacent nodes when appropriate. Explicit “produce directly, you decide” delegation enables a fast path; scoped edits reopen only affected nodes. No path permits invented product facts or marking untested checks as passed.

## 适用范围与能力边界 / Scope and capability limits

- 适用于商品营销主视觉、促销海报、平台首图、局部改稿和多语言适配。
  - Supports product key visuals, campaign posters, platform hero images, local edits and localization.
- 不用于完整商品详情页、交互界面或品牌识别系统。
  - Excludes complete product-detail pages, interfaces and brand identity systems.
- 这是指令型技能，不是独立的图像生成程序；不包含模型、API密钥、字体或外部工具。
  - This is an instruction-based skill, not a standalone image-generation application; it includes no model, API key, font or external tool.
- 实际图像生成、局部编辑、合成和可控排版取决于使用环境。没有图像能力时应明确交付简报或布局规格，不冒充完成成图。
  - Image generation, regional editing, compositing and controlled typography depend on the host environment. Without image capability, clearly deliver a brief or layout specification rather than claiming completed artwork.
- 不承诺生成式编辑的像素冻结、特定字体还原或商业效果；按真实检查结果报告。
  - Do not promise pixel-identical generative edits, exact typeface reproduction or commercial results; report only actual checks.

## 使用方法 / Usage

将整个 `ecommerce-main-visual-v4` 文件夹放入目标环境指定的技能目录，保持内部相对路径不变。技能发现或刷新方式以目标环境为准。

Place the complete `ecommerce-main-visual-v4` folder in the skill directory designated by your host environment, preserving relative paths. Follow that environment's skill discovery or refresh procedure.

在支持该技能调用方式的 Codex 环境中，可使用：

In a Codex environment supporting this invocation syntax, use either language:

```text
$ecommerce-main-visual-v4
为这个产品设计电商主视觉。请先核对我已有的文案和规格，再给低保真版式，不要直接出成稿。
```

```text
$ecommerce-main-visual-v4
Design an e-commerce key visual for this product. First check my existing copy and specifications, then show low-fidelity layouts rather than finished artwork.
```

也可以明确限定修改范围：

You can also explicitly limit the edit scope:

```text
$ecommerce-main-visual-v4
保持商品、背景、文案和构图，只调整标题与价格字块的配色和字体气质。
```

```text
$ecommerce-main-visual-v4
Preserve the product, background, copy and composition. Adjust only the colors and typographic character of the headline and price blocks.
```

提供商品原图、Logo原件、必须出现的文案、规格和语言需求会帮助减少返工。尚未确定的内容可以说明需要拟写或希望先比较方案。

Original product images, logo assets, mandatory copy, specifications and locale requirements help reduce rework. For undecided items, state whether you want proposed wording or options to compare first.

## 仓库结构 / Repository structure

```text
ecommerce-main-visual-v4/
├── README.md
├── SKILL.md
├── SKILL.zh-CN.md
├── SKILL.en.md
├── .gitignore
├── agents/
│   └── openai.yaml
└── references/
    ├── intake-template.md
    ├── user-collaboration.md
    ├── creative-direction.md
    ├── production-and-localization.md
    ├── iteration-protocol.md
    ├── visual-qa-checklist.md
    ├── qa-rubric.md
    ├── testing-guide.md
    └── nori-course-case.md
```

## 上传到 GitHub / Upload to GitHub

解压发布包后，把 `ecommerce-main-visual-v4` 文件夹中的内容作为仓库根目录上传，包括 `.gitignore`。如果需要在 GitHub 中直接浏览或编辑技能，不要只把 ZIP 当作唯一仓库文件上传；ZIP可以另作发布附件。

Extract the package and upload the contents of `ecommerce-main-visual-v4`, including `.gitignore`, to the repository root. To browse or edit the skill directly on GitHub, do not upload only the ZIP as the repository's sole content; the ZIP can also serve as a release attachment.

该包不包含 `.git` 历史、本机配置、工作目录、生成海报、产品图片、Logo原件或来源PDF。没有创建远程仓库或执行推送。

The package excludes `.git` history, local configuration, working files, generated posters, product images, original logos and source PDFs. No remote repository has been created or pushed.

## 案例与验证状态 / Examples and validation status

[NORI案例](references/nori-course-case.md)是可选课程测试资料，不是独立的商品性能证明或所有海报的默认输入。其中历史素材状态须按实际任务更新；原始PDF、商品图和Logo不随包提供。品牌、价格、日期、配色、语言数量与画布比例不得套用到其他项目。

[The NORI fixture](references/nori-course-case.md) is optional course test material, not independent evidence of product performance or a default brief for every poster. Refresh its historical asset status against the current task; the source PDF, product image and logo are not bundled. Do not transfer its brand, price, dates, colors, locale count or aspect ratio to unrelated projects.

版本4.1.0已完成入口结构与本地文档链接检查。测试指南新增14条用户介入回归场景，仍属于待执行用例；没有声称通过真实多轮模型行为、图像效果或独立真人使用测试。详见[测试指南](references/testing-guide.md)。

Version 4.1.0 has undergone entrypoint structure and local-link checks. The 14 added collaboration regression scenarios are still unexecuted fixtures; no claim is made of passed multi-turn model behavior, image-quality or independent human usability tests. See the [testing guide](references/testing-guide.md).

## 许可证 / License

本导出包未指定许可证，也没有代替作者选择或添加开源许可证。发布者如需声明复用许可，请自行确定后添加相应文件。

No license is specified in this package, and no open-source license has been chosen or added on the author's behalf. Publishers wishing to state reuse permissions should decide on and add the appropriate license file themselves.
