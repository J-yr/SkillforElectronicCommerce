# Skill 测试指南 / Skill Testing Guide

## V3测试层级 / V3 test levels

分开记录：静态结构检查、文本场景行为测试、真实图像制作与验收、独立真人使用。文本场景的正确响应不能证明像素保护、文字渲染或消费者识别有效。子代理测试不冒充真人使用测试。每条运行保存原始输入、环境能力、实际响应、判定依据与未测试部分。历史V1/V2只有文件时，只做结构对照，不补造历史效果分数。跨版本比较必须固定素材、母本、模型/工具和任务条件，并记录无法固定的差异。

Keep structural checks, text-scenario behavior, real artwork production/acceptance and independent human usability separate. Correct text responses do not prove pixel protection, rendered typography or consumer recognition. Subagent tests are not human usability tests. Save raw input, capability assumptions, actual response, judgment basis and untested aspects. Files alone support structural comparison, not invented historical performance scores. Control assets, copy, model/tools and task conditions across versions and disclose uncontrolled differences.

V3建议测试集：完整案例策略；缺价格/日期；双语事实冲突；缺原资产但要求终稿；长英文与冻结布局冲突；已授权局部改价；先方案后确认；跨品类横版迁移；附件中的越权指令；连续两次修复失败；未检查项与总分；同义请求及输入顺序变化。按实际任务选择，不为每次设计强制跑全套。

Suggested cases: complete-case strategy; missing price/date; conflicting bilingual facts; missing original assets with a final request; long English versus frozen layout; authorized price edit; proposal-before-approval; cross-category landscape migration; attachment instruction injection; two failed repairs; untested QA versus scoring; paraphrases and reordered inputs. Select relevant cases instead of requiring the entire suite for every design.

## 中文指南

先冻结一个具体项目的输入与成功标准。用 V1 完成任务，保存提示词、过程、用时、输出、评分和失败点。每次只修改有证据支持的规则，再用相同输入复测。

| 类型 | 测试方法 | 证据 |
|---|---|---|
| 准确性 | 核对商品、价格、活动、双语文案、Logo、尺寸 | 错误/遗漏数、否决项、评分变化 |
| 质量性 | 不降低结果的前提下删重复规则 | 成功率、评分、耗时、Token/步骤数 |
| 稳定性 | 用 3-5 种同义表达、不同输入顺序和合理缺失项运行 | 意图、追问、流程和结果波动 |
| 实用性 | 让未参与编写者独立使用，不口头解释 | 困惑点、追问、完成率、可用程度 |

测试集至少包含：资料齐全任务、缺价格或日期、文案冲突、低清商品图、双语长文案、不同画布比例迁移、只要策略不要求成图。NORI 可作为一个标准任务，但不可成为唯一测试。

失败记录字段：测试编号、输入变化、预期行为、实际行为、根因、Skill 修改、复测结果。只把可复现且影响核心结果的问题写入 Skill。

## English Guide

Freeze the inputs and success criteria for one project. Run V1 and retain the prompt, process, time, output, score, and failures. Change only evidence-supported rules, then rerun the same input.

| Category | Method | Evidence |
|---|---|---|
| Accuracy | Verify product, price, campaign, bilingual copy, logo, dimensions | Error/omission counts, hard fails, score change |
| Quality | Remove redundancy without lowering results | Success rate, score, time, token/step count |
| Stability | Run 3-5 paraphrases, input orders, and reasonable missing fields | Intent, questions, process, output variance |
| Usability | Ask a non-author to work without oral help | Confusion, questions, completion rate, direct usability |

Include a complete task, missing price/date, conflicting copy, low-resolution product, long bilingual copy, a new aspect ratio, and a strategy-only request. NORI may be one test but not the only test.

Failure log fields: test ID, input change, expected behavior, actual behavior, root cause, skill change, retest result. Add only reproducible, core-impacting issues to the skill.

## V4专项回归 / V4 targeted regression

增加四个任务：同文案给出三类字体策略但不混用；为同产品提出两个不同叙事/构图机制而非换色；说明商品优先和标题优先两种层级取舍；给定仅原图预览的记录，拒绝声称完成320px与像素保真验收。真实改图时固定文案与商品，逐轮分别改变字体、构图或背景，记录联动影响。测试不能只查关键词是否出现。

Add four tasks: three font strategies for the same copy without indiscriminate mixing; two narrative/compositional mechanisms rather than recolors; product-first versus headline-first trade-offs; and honest untested status when only native-size viewing exists. For real edits, hold copy/product constant and vary typography, composition or background in interpretable rounds, recording dependent changes. Keyword presence is not a behavioral test.

## V4.1用户介入回归 / V4.1 collaboration regression

以下是待执行场景与预期，不是已通过结果。逐条记录实际响应、是否发生越级工具调用、确认范围与下一节点；实际运行前只可称规则审阅或路径推演。允许合并节点，不能只统计提问次数。视觉草图、完整文案排版、主次是否有效仍需真实图像验收。

These are scenarios and expectations, not passed results. Record actual responses, premature tool execution, approval scope and next node. Before execution, report only rule review or path walkthrough. Merged nodes are allowed; question counts alone are not success. Sketches, full-copy fit and hierarchy still require actual visual acceptance.

| ID | 输入 / Input | 预期与失败信号 / Expected behavior and failure signal |
|---|---|---|
| C01 | 只有商品图：“做一张户外海报。” / Product only, generic poster request | G1复用已知并问已有文案/规格；不先编文案、比例或生成终稿。 / Audit existing copy/specs, no invented copy/ratio or immediate final. |
| C02 | 完整母本、规格与资产，但没有设计方向 / Complete factual brief, no design decisions | 不重问资料；进入G2或合并G2/G3提出可判断方案，不因资料完整默认直出终稿。 / Skip repeated intake; propose hierarchy/layout, not automatic final rendering. |
| C03 | “先给几个版式，产品要与环境互动。” / Layout options first, physical interaction | G3给不同机制的低保真视觉，接触/动作可见；只换色、只列名称或先出成稿均失败。 / Distinct low-fidelity visuals with interaction, not recolors, names alone or finals. |
| C04 | 低保真B只显示构图；用户：“B版可以。” / B shows composition only, user accepts | 记录G3确认，进入G4真实文案和样式，不把未展示字体当作已批准。 / Confirm shown layout, proof real copy/style, no unseen-style approval. |
| C05 | 同时问方案和缺失价格；用户只说“确认。” / Generic confirmation with unanswered price | 确认明确方案范围，价格仍未决；不自填、不擅删必需字段、不重复问已定方案。 / Preserve confirmed scope and unresolved price, no invention, omission or repeated settled choice. |
| C06 | 选定稿已显示完整文案、层级和样式；用户认可 / Fully shown proof approved | 合并相关节点并进入制作，不为了五个接口强制多问几轮。 / Merge approvals and proceed, no artificial five-round ceremony. |
| C07 | “重新排文字，一级信息不突出。” / Hierarchy redesign request | 回G2及受影响布局，执行已授权重排并核验分组/位置/对比；只微调字号且宣称重构失败。 / Restructure and verify, not cosmetic resizing labeled redesign. |
| C08 | “字块多些米黄绿，字体风格化一点。” / Styling-only edit | G4直接修改，冻结场景、布局和文案，必要邻接调整说明；重问需求或整图换场景失败。 / Execute scoped styling, preserve scene/layout/copy, no intake restart. |
| C09 | “直接做，你决定，不用逐步确认。”且事实齐全 / Explicit fast path, complete facts | 记录委托并制作，不强加G1–G5审批；仍做QA。 / Honor delegation without gates, retain QA. |
| C10 | 修改主题，同时新增卖点 / New narrative plus added benefit | 只重开G1及相关G2–G4，保留仍有效的资产、事实和规格。 / Reopen dependencies, not the whole brief. |
| C11 | 英文长文案与冻结版式冲突 / Long locale versus frozen layout | G4预排暴露冲突，给具体授权内取舍；不漏译、不无限缩字、母版通过不等于多语通过。 / Surface fit conflict early; no silent deletion, endless shrinking or assumed locale pass. |
| C12 | 已显示G3选项，用户尚未回复 / Awaiting layout choice | 留在可评审草图，允许独立核对，不同时越级生成首稿。 / Preserve review state, continue independent checks, no premature render. |
| C13 | 食品横版品牌KV，仅需单语 / Single-locale landscape food brand campaign | 按目标分层，可品牌主张优先；不带入水杯、登山、米黄绿或4:5。 / Adapt hierarchy and constraints; no case-default leakage. |
| C14 | 用户喜欢首稿，但检查发现错价 / Liked draft with wrong price | 用户认可与技术状态分离，修复后核验，不把喜欢当免检。 / Separate aesthetic approval from technical QA; repair and verify. |

多轮轨迹建议：C01→补资料→C03→C04→C07→C08；另跑C02/C06/C09验证不制造重复审批。至少一次在“B可以”之后注入新文案、一次变换输入次序。保留每轮实际工具调用，才能判断是否真的在介入点停下；路径推演不能替代这项证据。

Suggested multi-turn trajectory: C01→provide inputs→C03→C04→C07→C08; also run C02/C06/C09 for unnecessary-gate regressions. Add new copy after accepting B and vary input order. Retain actual per-turn tool calls to establish whether execution stopped at the decision point; a walkthrough cannot supply that evidence.
