# 精准修改与版本协议 / Precise editing and versions

## 中文

在标注、局部反馈或精准修改任务中读取。以当前对话授权为准，不把修改价格等已授权动作再次当成审批事项。

按[协作协议](user-collaboration.md)只重开受影响决策：文案事实回G1，信息主次回G2，场景交互/构图回G2或G3，字体/字块配色回G4，技术错误留在制作与QA。已明确授权的反馈可直接执行，不因“重开”再索要一次相同许可；只有未解决取舍或范围冲突才等待选择。保留其他已确认节点及版本依据。

用户说“没有修改”“看不出变化”时，先比较原目标和可见差异：问题若在信息分组与阅读顺序，就重排分组、位置、留白和对比，而不是再次轻微改字号或换色。执行前明确本轮可观察的验收目标，执行后提供父版/新版对照或具体变化说明；没有核验不得声称明显改善。

1. 定位编辑目标及父版本。为每条反馈记录：对象、观察偏差、目标状态、验收方法、允许区域、冻结对象、允许联动的邻域。区分局部排版、局部图形、结构调整、概念重构。
2. 若用户要求只改标题，则不改产品、Logo、价格、背景、裁切等。已授权的相邻间距调整可执行；必然影响明确冻结对象时，解释冲突并请求范围选择。用户要求先确认，或反馈互相矛盾时先解决依赖。
3. 查看工具是否具备实际区域编辑、蒙版、图层、原资产合成、可控排版或图像比对能力。提示词冻结不是技术保证。不得声称用了不存在的蒙版或合成工具。
4. 编辑提示明确：编辑目标、本轮改动、必须保持、允许联动、禁止新增、验收条件。有蒙版不等于自动通过，仍检查结果。
5. 检查修改命中情况和所有冻结对象。若要求像素完全一致，需在同尺寸同坐标下验证编辑区之外的像素；有压缩或重渲染时，不可仅凭肉眼声称像素一致。若只要求内容不变，则核对结构、文案、位置和比例，并声明检查方式。
6. 意外误改即不通过，优先恢复原资产或回退。先修事实资产，再修越界可读性，再修主次和风格。同一问题连续两次无改善后停止当前方法，记录并回退，不覆盖满意稿。

每轮记录：版本ID、父版本、素材/母本版本、用户原始反馈、授权范围、实际改动、冻结项核验及证据、未解决项、输出路径和状态。保存为新文件，例如 `brand-hero-v03-title.png`。不要把待测父版本称为合格版。

## English

Read for annotations, local feedback or precise edits. Existing conversation authorization governs; an authorized price change needs no repeated approval.

Reopen only affected decisions under the [collaboration protocol](user-collaboration.md): copy/facts at G1, priority at G2, interaction/composition at G2 or G3, font/block styling at G4, technical errors in production/QA. Explicit feedback authorizes execution; reopening is not another request for the same permission. Await a choice only for unresolved trade-offs or scope conflicts, preserving other approvals and version evidence.

For “nothing changed” feedback, compare the original target with visible differences. If grouping and reading order are wrong, restructure grouping, placement, space and contrast instead of repeating slight scaling or recoloring. State an observable acceptance target, then provide a parent/new comparison or specific change description; do not claim clear improvement without checking.

1. Identify target and parent version. Record object, observed issue, target, acceptance method, editable region, frozen objects and permitted neighboring adjustments. Distinguish typography, local graphics, structural changes and conceptual redesign.
2. A title-only request freezes product, logo, price, background and crop. Execute already-authorized neighboring adjustments. If a change necessarily affects an explicitly frozen object, explain the conflict and request a scope choice. Honor proposal-first requests and resolve contradictory feedback before dependent work.
3. Check actual regional editing, masking, layers, compositing, controlled typography and comparison capabilities. A prompt is not a technical guarantee; never claim unavailable capabilities.
4. Specify target, allowed changes, preservation, adjacent permissions, prohibited additions and acceptance conditions. Masks still require output review.
5. Verify requested changes and every frozen object. Pixel identity requires aligned, same-size comparison outside the edit area; visual inspection cannot establish it after compression or rerendering. Content preservation instead checks structures, copy, positions and proportions with an explicit method.
6. Unintended changes fail review. Restore original assets or revert. Repair facts/assets, readability, then hierarchy/style. After two consecutive non-improving attempts, stop that method and revert without overwriting approved work.

Record version, parent, asset/copy revisions, original feedback, authorization, actual changes, preservation evidence, unresolved issues, path and status. Save a new file. Do not call an untested parent acceptable.
