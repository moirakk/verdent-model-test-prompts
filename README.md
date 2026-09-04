# Verdent Model Test Prompt Collection

A reusable collection of high-density coding prompts for comparing models inside Verdent.

Each prompt is designed to be copied directly into Verdent. The goal is not to test whether a model can answer a coding question, but whether it can turn an ambitious product or engineering brief into a working result that can be opened, inspected, and compared across models.

The format follows a presentation-order prompt collection: numbered prompts, strong titles, collapsed prompt text, and self-contained specifications. Each entry contains only what the builder model needs to run the test.

## Prompt Design Rules

These prompts are intentionally written as pressure tests, not feature requests:

- First screen first: the opening screen or first playable moment must prove the concept immediately.
- One ambitious object: each prompt asks for a specific product, tool, demo, or rescue outcome, not a vague category.
- Must-not clauses: every prompt names common low-effort failures so models cannot satisfy the task with a generic template.
- Layered systems: prompts combine product logic, interaction, state, visual quality, technical constraints, and verification.
- Local by default: external services are simulated with local data so model runs stay comparable.
- Reviewable output: every prompt ends with an audit packet for cross-model review.

## Common Failure Modes To Watch

These are the failures this collection is designed to expose:

- Template substitution: the model builds a familiar generic app instead of the specific requested product.
- Static theater: controls, charts, timelines, maps, or game objects look real but do not change state.
- First-screen weakness: the page opens with marketing copy, empty setup, or a bland dashboard instead of the requested working surface.
- Fake computation: totals, recommendations, scores, or alerts are hard-coded instead of derived from sample data.
- Shallow interaction: the model implements clicks but not the cross-panel consequences the prompt asks for.
- Visual collapse: text overlaps, mobile breaks, 3D scenes render blank, or dense tools become unreadable.
- Verification bluffing: the model claims success without running, previewing, or honestly describing what could not be checked.

## Sections

| Section | Prompts | Count |
|---|---:|---:|
| [Complete Product Builds](#complete-product-builds) | 1-6 | 6 |
| [Complex Interactive Tools](#complex-interactive-tools) | 7-12 | 6 |
| [Data-To-Decision Workspaces](#data-to-decision-workspaces) | 13-18 | 6 |
| [Playable Browser Worlds](#playable-browser-worlds) | 19-24 | 6 |
| [Repair, Rescue, And Refactor](#repair-rescue-and-refactor) | 25-30 | 6 |
| [Global Landmark Architecture Modeling](#global-landmark-architecture-modeling) | 31-37 | 7 |

## Quick Index

### Complete Product Builds

| # | Title |
|---:|---|
| 1 | [Photo Meal Coach - From Camera Moment To Weekly Nutrition Loop](#prompt-01) |
| 2 | [Founder Operating Room - One Screen To Run A Tiny Startup](#prompt-02) |
| 3 | [Solo Consultant Command Center - Clients, Invoices, Scope And Next Actions](#prompt-03) |
| 4 | [Family Logistics Console - The Week, The Fridge, The Budget And The Ride](#prompt-04) |
| 5 | [Creator Launch Studio - From Idea Backlog To Scheduled Release](#prompt-05) |
| 6 | [Local Knowledge Garden - Notes That Turn Into Tasks And Briefs](#prompt-06) |

### Complex Interactive Tools

| # | Title |
|---:|---|
| 7 | [Timeline Surgery - Edit A Podcast Without Playing Video](#prompt-07) |
| 8 | [Spatial Kanban - Projects As A Living Risk Map](#prompt-08) |
| 9 | [Logic Form Builder - Conditional Fields, Validation And Live Preview](#prompt-09) |
| 10 | [Command Palette File Explorer - Search, Actions And Keyboard Flow](#prompt-10) |
| 11 | [Visual Workflow Builder - Nodes, Edges, Runs And Failure States](#prompt-11) |
| 12 | [Design Review Board - Pin Comments Directly Onto Screens](#prompt-12) |

### Data-To-Decision Workspaces

| # | Title |
|---:|---|
| 13 | [Ad Spend War Room - Campaigns That Explain Themselves](#prompt-13) |
| 14 | [CSV Forensics - Find The Story In A Messy Export](#prompt-14) |
| 15 | [Subscription Leak Detector - Where The Money Quietly Leaves](#prompt-15) |
| 16 | [Support Inbox Intelligence - Turn Tickets Into Product Signals](#prompt-16) |
| 17 | [Workout Progress Lab - Training Load, Recovery And Plateaus](#prompt-17) |
| 18 | [Revenue Cohort Explorer - Retention, Expansion And Churn In One View](#prompt-18) |

### Playable Browser Worlds

| # | Title |
|---:|---|
| 19 | [Desert Evacuation Drive - Sandstorm, Signal Truck, Playable Escape](#prompt-19) |
| 20 | [Tiny Factory That Teaches Itself - Belts, Bottlenecks And Upgrades](#prompt-20) |
| 21 | [Rooftop Drone Rescue - Wind, Battery And Path Planning](#prompt-21) |
| 22 | [Ecosystem Sandbox - Water, Plants, Weather And Balance](#prompt-22) |
| 23 | [Cyber Train Dispatch - Prevent Delays Across A Living Network](#prompt-23) |
| 24 | [Particle Music Sequencer - Soundless Visual Rhythm Machine](#prompt-24) |

### Repair, Rescue, And Refactor

| # | Title |
|---:|---|
| 25 | [Save This Half-Built App - From Static Mockup To Working Product](#prompt-25) |
| 26 | [Performance Rescue - Keep The Spectacle, Remove The Jank](#prompt-26) |
| 27 | [Mobile Overflow Cleanup - Make The Desktop Beauty Survive A Phone](#prompt-27) |
| 28 | [Design System Migration - Tokens, Components And No Regressions](#prompt-28) |
| 29 | [Test The Untested Flow - Add Confidence Without Rewriting The App](#prompt-29) |
| 30 | [Bug Triage Gauntlet - Five Reports, Three Real Bugs, One Clean Patch Set](#prompt-30) |

### Global Landmark Architecture Modeling

| # | Title |
|---:|---|
| 31 | [Asia - Taj Mahal Architectural Model, Marble Symmetry And Garden Axis](#prompt-31) |
| 32 | [Europe - Sagrada Familia Procedural Facades, Towers And Interior Light](#prompt-32) |
| 33 | [Africa - Great Pyramid Complex, Limestone Massing And Desert Context](#prompt-33) |
| 34 | [North America - Empire State Building, Art Deco Vertical City Model](#prompt-34) |
| 35 | [South America - Machu Picchu Citadel, Terraces And Mountain Topography](#prompt-35) |
| 36 | [Oceania - Sydney Opera House, Shell Roofs And Harbor Setting](#prompt-36) |
| 37 | [Antarctica - South Pole Research Station, Extreme-Climate Modular Architecture](#prompt-37) |

## Case Capability Matrix / 测试能力矩阵

用这张表快速选择要跑哪条 prompt：它标注了每个 case 的类型、适合展示的模型能力、主要测试点，以及是否适合公开宣发。

展示适配度：

- High：适合公开 demo，最终结果在视觉或交互上比较容易一眼看懂。
- Medium：适合产品 walkthrough、模型横评、技术对比，需要稍微解释才看得出强弱。
- Low：更适合内部工程评估，不一定适合做首发宣传视频。

| # | 类型 | 适合展示的能力 | 主要测试点 | 展示适配度 |
|---:|---|---|---|---|
| 1 | 移动端 AI 产品 | AI 应用体验、移动端完成度、本地状态闭环 | 产品塑形、移动端 UI、可编辑估算、状态更新、可信 AI 模拟 | High |
| 2 | 创始人运营看板 | 创业者工作流、高密度单屏指挥台 | 信息架构、优先级逻辑、场景模拟、B2B 产品判断 | Medium |
| 3 | 咨询服务工作台 | 实用 B2B 工作流、客户/发票运营 | 工作流建模、表格、状态逻辑、容量规划、业务具体性 | Medium |
| 4 | 家庭协作应用 | 日常复杂产品、移动端实用性 | 跨系统状态、冲突解决、日历/列表 UX、移动端易用性 | Medium |
| 5 | 创作者发布工作台 | 创作者工具、多平台发布流程 | 内容管线、ready score、平台差异、内容运营 | High |
| 6 | 本地知识工作台 | 研究到行动、local-first 生产力 | 搜索/筛选、笔记关联、证据处理、三栏布局、模拟提取 | Medium |
| 7 | 创作者剪辑工具 | 复杂产品 UI、同步编辑工作流 | 文稿选择、时间线状态、clip 规则、导出队列、高密度工作台设计 | High |
| 8 | 空间化项目管理 | 新型交互模型、视觉化项目管理 | 拖拽/更新状态、空间推理、筛选、依赖/风险建模 | High |
| 9 | 表单构建器 | App builder / product builder 能力 | schema 状态、条件逻辑、校验、实时预览、表单 UX | High |
| 10 | 开发者工具 | 键盘优先的 coding 工作流 | 模糊搜索、命令操作、文件预览、本地状态变更、开发者 UX | Medium |
| 11 | 自动化画布 | Agentic workflow 界面、节点系统 | 图 UI、运行模拟、失败状态、审批节点、日志、自动化状态 | High |
| 12 | 设计协作工具 | 视觉反馈工作流 | 空间评论、pin/thread 同步、评审状态、屏幕版本、缩放行为 | High |
| 13 | 数据分析工作台 | 业务决策 dashboard | 计算指标、筛选/排序、下钻、建议动作、数据产品判断 | High |
| 14 | 数据清洗工具 | 脏数据推理、分析师工作流 | 数据画像、异常检测、清洗开关、表格状态、洞察总结 | Medium |
| 15 | 订阅成本工具 | 成本浪费识别、决策工作流 | 周期成本建模、建议逻辑、节省场景、续费状态 | Medium |
| 16 | 客服智能工作台 | 文本运营、产品信号提取 | 聚类元数据、工单状态、筛选、创建 action、客服到产品桥接 | Medium |
| 17 | 训练分析应用 | 个人数据分析、教练型 UX | 时间序列趋势、建议逻辑、训练记录状态、健康边界表达 | Medium |
| 18 | SaaS 收入分析 | 高管分析、cohort 探索 | cohort 计算、热力图交互、MRR bridge、账号下钻 | Medium |
| 19 | 3D 浏览器游戏 demo | 电影感视觉冲击、可玩 3D | Three.js/canvas、开场镜头、控制、游戏状态、性能、场景密度 | High |
| 20 | 工厂模拟游戏 | 可运行系统、可见机制、gameplay loop | 动画循环、吞吐模拟、瓶颈、升级、反馈系统 | High |
| 21 | 任务型小游戏 | 控制约束、路径规划、HUD 清晰度 | 游戏物理、资源限制、目标设计、重开/失败状态 | High |
| 22 | 系统沙盒 | 因果模拟、参数控制 | 模拟变量、场景控制、视觉状态变化、恢复逻辑 | High |
| 23 | 调度模拟器 | 运营游戏、动态网络 | 实时移动、冲突检测、优先级调度、事件处理 | High |
| 24 | 创意 coding 玩具 | 视觉节奏、可玩交互 | 动画时间、sequencer 状态、pattern 控制、canvas polish | High |
| 25 | 现有应用救援 | Agent 实用性、补完成品能力 | 代码库检查、范围控制、状态修复、响应式修复、诚实总结 | Medium |
| 26 | 性能救援 | 技术深度、保留视觉复杂度 | 瓶颈判断、优化取舍、行为保持、性能验证 | Low |
| 27 | 移动端救援 | UI 可靠性、响应式工艺 | 布局调试、viewport 检查、overflow 修复、保留桌面行为 | Medium |
| 28 | 设计系统迁移 | 可维护 UI 改造 | token/component 抽取、一致性、渐进重构、回归控制 | Low |
| 29 | 测试覆盖补强 | 工程纪律 | 测试模式识别、行为覆盖、最小可测试性改动、诚实边界 | Low |
| 30 | Bug 分诊 | 高级 coding agent 判断力 | 分诊、优先级、范围控制、not-a-bug 处理、逐项验证 | Low |
| 31 | 亚洲地标建筑建模 | 对称建筑、材质、园林轴线 | 3D 比例、白色大理石材质、穹顶/尖塔、倒影水池、相机导览 | High |
| 32 | 欧洲地标建筑建模 | 高复杂立面、塔楼、室内光 | 程序化细节、哥特/现代主义混合形体、彩窗光、性能控制 | High |
| 33 | 非洲地标建筑建模 | 巨型尺度、历史建筑群、地形 | 金字塔体量、石块层次、沙漠环境、太阳角度、游客尺度对比 | High |
| 34 | 北美地标建筑建模 | 摩天楼、城市峡谷、Art Deco | 垂直比例、退台结构、窗格阵列、夜景灯光、城市上下文 | High |
| 35 | 南美地标建筑建模 | 山地遗址、台地、复杂地形 | 梯田、石墙、路径、云雾、海拔感、地形生成 | High |
| 36 | 大洋洲地标建筑建模 | 壳状屋顶、海港环境、曲面表达 | 曲面近似、结构节奏、水面反射、桥港关系、日夜光照 | High |
| 37 | 南极地标建筑建模 | 极地建筑、模块化基地、极端环境 | 架空结构、冰雪材质、风雪粒子、生活/科研模块、环境叙事 | Medium |

## Suggested Prompt Picks / 推荐选题

公开展示模型能力：

- 想要第一眼就有视觉冲击：优先选 19、20、21、22、23、24。
- 想证明模型能做严肃产品软件，而不只是炫技：优先选 7、9、11、12、13。
- 想让更广泛的观众容易理解产品价值：优先选 1 或 5。

平衡横评模型：

- 视觉/可玩：19 或 20
- 复杂工作流：7 或 11
- 数据产品：13 或 14
- 移动端产品：1 或 4
- 工程纪律：25、27 或 30

内部工程评估：

- 用 25-30 测模型是否会读现有项目、保留产品意图、避免大范围乱改，并诚实验证。
- 用 13-18 测模型是否真的基于数据计算，而不是只装饰静态指标。
- 用 7-12 测模型是否能让多面板、选中状态和复杂控件保持同步。
- 用 31-37 测模型是否能把真实世界建筑转成可检查的 3D 结构，而不是做成抽象地标剪影。

## Suggested Model Comparison Notes

For each model run, judge the final output more than the explanation.

Suggested dimensions:

- Completion: did it build the requested experience end to end?
- First screen: is the opening screen immediately convincing and useful?
- Interaction depth: can the user actually operate the product or demo?
- Product judgment: did the model choose sensible defaults and flows?
- Visual quality: does it feel intentional rather than template-generated?
- State handling: are empty, loading, error, and edge states represented?
- Engineering discipline: is the implementation coherent and maintainable?
- Verification: did the model run or inspect the result before claiming success?

## Recommended Test Run Protocol

For fair model comparisons, keep the run conditions as stable as possible:

1. Start each model from the same clean project state.
2. Paste exactly one prompt, without extra hints.
3. Let the model work until it claims completion or asks for a necessary decision.
4. Save the final app, patch, screenshots if available, and final response.
5. Run the cross-audit instruction with a different model or in a separate review pass.
6. Score the built result, not the elegance of the narrative.

Suggested run record:

```text
Model:
Model version:
Date:
Prompt number:
Project starting state:
Time budget:
Tools available:
Completion status:
Verification performed:
Human score:
Cross-audit score:
Best observed strength:
Biggest failure:
Would use this model for this task type again:
```

## Scoring Sheet

Use 1-5 for each dimension:

| Dimension | 1 | 3 | 5 |
|---|---|---|---|
| Completion | Mostly missing or only planned | Partial working slice | Complete requested experience |
| First-screen quality | Generic or unclear | Understandable but ordinary | Immediately proves the concept |
| Interaction depth | Static or fake controls | Some working interactions | Core workflow works end to end |
| Product judgment | Template choices | Reasonable defaults | Strong domain-specific decisions |
| Visual/UX quality | Broken, cluttered, or bland | Usable but uneven | Intentional, polished, responsive |
| State handling | No meaningful state | Basic state | Edge, empty, error, and update states |
| Engineering quality | Brittle or chaotic | Acceptable | Coherent, scoped, maintainable |
| Verification honesty | Claims without checking | Some checking | Clear checks and honest limits |

## Cross-Audit Workflow

Use the same prompt for every model. After each run, save the final app, demo, or patch plus the model's final summary.

For cross-audit, give another model the finished output and this instruction:

```text
Review this model run against the original prompt. Judge the final working result, not the confidence of the explanation. Identify missed requirements, broken interactions, visual or UX issues, verification gaps, unnecessary complexity, and the three highest-leverage improvements. Do not rewrite the project unless asked; produce a scored audit.
```

Suggested cross-audit dimensions:

- Prompt coverage
- First-screen quality
- Interaction correctness
- Visual and responsive quality
- Engineering maintainability
- Verification honesty
- Regression or hallucination risk

Each prompt asks the builder model to leave an audit packet at the end of its response. That packet makes it easier to compare runs and easier for a second model to review the result.

## Prompts

## Complete Product Builds

<a id="prompt-01"></a>

<details>
<summary><strong>01. Photo Meal Coach - From Camera Moment To Weekly Nutrition Loop</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition mobile-first web app called Photo Meal Coach: a nutrition assistant that turns a single meal photo moment into a weekly coaching loop.

This must not be a generic calorie tracker, a static landing page, a diet blog layout, or a dashboard full of disconnected cards. It should feel like a product someone could open at lunch, log a meal in under a minute, correct the estimate, and understand how today's choices affect the week.

#### FIRST SCREEN - TODAY'S FOOD DECISION, NOT A MARKETING PAGE
- Open directly on today's nutrition screen. The user should immediately see a camera/photo entry area, today's macro progress, the latest meal estimate, and one clear next action.
- Include a believable sample day with at least three meals already logged, each with calories, protein, carbs, fat, confidence level, and a correction state.
- The first interaction should be obvious: add a meal, adjust an estimate, or ask for advice. Do not hide the product behind onboarding.

#### CORE PRODUCT SYSTEM
- Meal capture flow: photo placeholder, meal name, portion confidence, estimated calories/macros, and an editable correction panel.
- Daily coaching: show remaining targets, one practical suggestion for the next meal, and a warning when the estimate is uncertain.
- Weekly loop: include a seven-day trend for calories, protein, and consistency, with a short plain-language interpretation.
- Food memory: repeated meals should appear as reusable suggestions, with a "last time you corrected this" hint.
- Advice layer: include an AI advice panel that explains the next best action without sounding like medical diagnosis.

#### INTERACTION AND STATE
- The app must be operable with local state. A user should be able to add a sample meal, edit macros, mark confidence as low/medium/high, and see the daily totals update.
- Include states for no photo selected, estimating, estimate needs review, corrected, and saved.
- Include at least one deliberate uncertainty moment: a mixed meal where the app asks the user to confirm portion size.
- The mobile layout is primary, but the desktop layout should use the extra width intelligently rather than stretching phone cards.

#### VISUAL AND UX QUALITY
- The interface should feel calm, trustworthy, and practical, not like a neon fitness game or a medical records system.
- Use restrained color to distinguish protein, carbs, fat, uncertainty, and progress. Avoid a one-color dashboard.
- Make the meal cards scannable. Numbers should be readable, but the product should not feel like a spreadsheet.
- No overlapping text, no clipped buttons, no tiny tap targets, and no giant hero typography inside app panels.

#### DEPTH CHECKPOINTS
- Include at least one low-confidence estimate and one corrected meal so reviewers can judge uncertainty handling.
- Daily totals must visibly recalculate after a macro edit.
- Advice should reference the current day/week data, not generic nutrition tips.

#### TECHNICAL REQUIREMENTS
- Build the full implementation in the current project using the existing stack if one exists. If starting from a blank folder, create the simplest appropriate browser app.
- Use real interactive state rather than only static mock data.
- Keep the implementation self-contained. Do not require paid external APIs.
- If image analysis is represented, simulate it clearly with realistic local sample outputs.
- Run the app or otherwise verify that the main screen renders and the primary interaction works.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize what was created, how to open it, what interactions work, and what you verified.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: completed requirements, interactive behaviors, verification performed, known shortcuts, and top three places another model should inspect.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

## Complex Interactive Tools

<a id="prompt-07"></a>

<details>
<summary><strong>07. Timeline Surgery - Edit A Podcast Without Playing Video</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser tool called Timeline Surgery: an editing workspace for turning a long podcast or interview into short clips without needing to play the source video.

This must not be a static transcript viewer, a generic media dashboard, or a pretty mockup with fake controls. It should feel like a working editor where transcript, timeline, clip candidates, speaker turns, and export decisions stay synchronized.

#### FIRST SCREEN - THE EDITING TABLE IS ALREADY ALIVE
- Open on a dense but readable editing workspace with a loaded sample podcast.
- The user should immediately see a transcript, a multi-segment timeline, detected highlight moments, speaker labels, clip duration targets, and an export queue.
- The first screen must make the core promise obvious: select words or moments, turn them into clips, and assemble a publishable queue.

#### CORE PRODUCT SYSTEM
- Transcript panel with speaker turns, timestamps, searchable text, and highlight markers.
- Timeline panel with segments for intro, topic blocks, high-energy moments, silence, and selected clips.
- Clip builder with start/end handles, title suggestion, hook line, platform target, and duration warning.
- Export queue for TikTok, YouTube Shorts, LinkedIn, and newsletter snippets, each with different length and copy requirements.
- Insight layer that identifies why a segment might work: conflict, clear advice, surprising stat, emotional beat, or strong quote.

#### INTERACTION AND STATE
- Selecting a transcript sentence should create or update a clip candidate.
- Dragging or editing start/end values should update clip duration and platform fit.
- Include filters for speaker, clip type, platform, and confidence.
- Include states for too short, too long, missing hook, ready to export, and needs review.
- Keyboard-style flow matters: include a command/search affordance for jumping to a timestamp or action.

#### VISUAL AND UX QUALITY
- This is a professional creator tool. It should feel compact, information-rich, and controlled.
- Use tabs, segmented controls, handles, status chips, and timeline tracks where appropriate.
- Avoid a landing page, oversized cards, decorative blobs, or generic SaaS marketing composition.
- The timeline must have stable dimensions; selecting clips should not cause layout jumps.
- The mobile view should degrade into a useful review mode rather than a broken mini desktop.

#### DEPTH CHECKPOINTS
- Transcript selection, timeline highlight, and clip queue must stay synchronized.
- Duration warnings should change when start/end values change.
- Export targets should enforce different constraints for at least three platforms.

#### TECHNICAL REQUIREMENTS
- Build the full implementation in the current project using the existing stack if one exists.
- Use local sample transcript data with at least 12 speaker turns and 5 detected highlight candidates.
- Implement real state synchronization between transcript selection, timeline selection, and export queue.
- Do not rely on external media files or paid APIs.
- Verify the page renders and at least one clip can be created or edited.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize the working editor flow, the sample data included, and what you verified.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: completed requirements, synchronized interactions, verification performed, known shortcuts, and top three places another model should inspect.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-08"></a>

<details>
<summary><strong>08. Spatial Kanban - Projects As A Living Risk Map</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition interactive tool called Spatial Kanban: a project board where work is arranged on a two-axis map instead of columns, with x-axis progress and y-axis risk.

This must not be a normal kanban with a novelty background. The spatial position must matter and must help users see blocked, risky, nearly-done, and neglected work.

#### FIRST SCREEN - THE MAP TELLS THE STORY
- Open on a populated project risk map with at least 18 cards, axis labels, clusters, filters, and a selected card detail panel.
- A user should immediately see which work is dangerous, which work is close to shipping, and which work lacks ownership.
- The first interaction should be dragging a card or changing a filter.

#### CORE SYSTEMS
- Cards with owner, progress, risk, deadline, dependencies, and status.
- Spatial axes for progress and risk with meaningful quadrants.
- Detail panel with blockers, dependency chain, history, and recommended next action.
- Views for map, list, and owner workload.
- Saved filters for "at risk", "unowned", "shipping soon", and "blocked by dependency".

#### INTERACTION AND STATE
- Drag cards and update progress/risk values.
- Filters, search, and owner selection should update the map.
- Dependencies should visibly affect the selected card's risk.
- Include undo or recent changes list.

#### VISUAL AND UX QUALITY
- Dense but readable. The map should not become a confetti field.
- Use stable card sizing, hover/selected states, and clear axes.
- Mobile should become a prioritized list plus mini map.

#### DEPTH CHECKPOINTS
- Dragging or editing a card must alter both map position and risk/progress data.
- Quadrants should have practical meaning and visible labels.
- Dependencies should change the interpretation of at least one card.

#### TECHNICAL REQUIREMENTS
- Use local sample data and real drag or controlled position updates.
- Keep state synchronized between map, detail, and list.
- Verify drag/update, filter, and card selection.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: spatial behaviors implemented, state synchronization, verification performed, and tradeoffs.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-09"></a>

<details>
<summary><strong>09. Logic Form Builder - Conditional Fields, Validation And Live Preview</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition working app called Logic Form Builder: a form-building workspace with conditional fields, validation rules, live preview, and submission review.

This must not be a static form mockup or a settings page full of fake controls. The user must be able to build or modify a form and see logic affect the preview.

#### FIRST SCREEN - BUILDER AND PREVIEW SIDE BY SIDE
- Open with a sample onboarding form loaded.
- Show field list, selected field settings, conditional logic, live preview, and recent submissions.
- The first interaction should be adding a field, toggling a condition, or editing a validation rule.

#### CORE SYSTEMS
- Field types: text, email, select, checkbox, number, date, textarea.
- Conditional display rules based on previous answers.
- Validation rules for required, min/max, format, and custom helper text.
- Live preview that reflects builder changes.
- Submission table showing valid, invalid, and incomplete attempts.

#### INTERACTION AND STATE
- Add, reorder, delete, and edit fields.
- Configure at least one conditional field and see it appear/disappear in preview.
- Validate preview input and show inline errors.
- Include reset and duplicate field actions.

#### VISUAL AND UX QUALITY
- Tool surface should feel precise and predictable.
- Use compact controls, tabs or panels, and clear selected states.
- Avoid huge empty builder areas and decorative app-builder marketing.

#### DEPTH CHECKPOINTS
- Conditional logic must be demonstrable in the preview using real answers.
- Validation errors should appear inline and prevent or flag bad submissions.
- Schema edits should persist during the session and affect submissions.

#### TECHNICAL REQUIREMENTS
- Use local state for schema and preview answers.
- Do not require a backend.
- Verify that schema changes update the preview and validation works.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: builder features implemented, logic examples, verification performed, and missing production pieces.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-10"></a>

<details>
<summary><strong>10. Command Palette File Explorer - Search, Actions And Keyboard Flow</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser app called Command Palette File Explorer: a file-navigation workspace optimized for keyboard search, actions, and fast project orientation.

This must not be a simple file tree or static command palette. Search results, selected file context, commands, and recent actions should work together.

#### FIRST SCREEN - KEYBOARD-FIRST PROJECT CONTROL
- Open on a project explorer with file tree, command palette open, recent files, selected file preview, and available actions.
- The first interaction should be typing to filter commands/files or pressing a visible shortcut-style action.
- Include realistic sample project files across app, components, tests, docs, and config.

#### CORE SYSTEMS
- Fuzzy search across file names, paths, symbols, and commands.
- Commands for open file, rename, duplicate, create file, reveal tests, copy path, and pin.
- File preview with metadata, related files, and quick actions.
- Recent actions log and pinned files.
- Empty and no-results states with recovery suggestions.

#### INTERACTION AND STATE
- Search should update results live.
- Selecting a result should update preview and active path.
- Commands should mutate local state where practical.
- Include keyboard hint UI even if full keyboard handling is limited.

#### VISUAL AND UX QUALITY
- Crisp developer-tool feel with excellent spacing and contrast.
- Avoid fake terminal decoration and generic IDE screenshots.
- Mobile should support search-first file access.

#### DEPTH CHECKPOINTS
- Search should cover files and commands, not just one list.
- At least one command must change local state.
- Preview should show related files or metadata that changes with selection.

#### TECHNICAL REQUIREMENTS
- Use local sample file data and real filtering.
- No filesystem access required.
- Verify search, selection, and at least one state-changing command.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: commands implemented, keyboard/search behavior, verification performed, and limitations.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-11"></a>

<details>
<summary><strong>11. Visual Workflow Builder - Nodes, Edges, Runs And Failure States</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser tool called Visual Workflow Builder: a node-based automation canvas with triggers, transforms, approvals, outputs, run history, and failure states.

This must not be a static flowchart. The user should be able to edit the workflow and simulate a run with visible node states.

#### FIRST SCREEN - A WORKFLOW MID-RUN
- Open on a populated workflow canvas with nodes, edges, run status, selected node settings, and event log.
- The first screen should show one failed node and one waiting approval node.
- The first action should let the user retry, edit a node, approve a step, or add a connection.

#### CORE SYSTEMS
- Node types: trigger, filter, transform, AI draft, human approval, webhook, database write, notification.
- Edge connections with labels and branch conditions.
- Run simulator with queued, running, success, failed, skipped, and waiting states.
- Node detail panel with inputs, outputs, settings, and logs.
- Version or change history for workflow edits.

#### INTERACTION AND STATE
- Add nodes, select nodes, edit settings, connect or disconnect edges if practical.
- Simulate run and update node states over time or step-by-step.
- Retry failed node and show changed result.
- Include validation for disconnected or misconfigured nodes.

#### VISUAL AND UX QUALITY
- Canvas should be legible and stable, with meaningful node colors and edge styling.
- Avoid tiny unreadable labels and random decorative graph layouts.
- Mobile can become run-monitor and node-detail mode.

#### DEPTH CHECKPOINTS
- A workflow run must show several node states, not only success.
- Retry or approval should visibly alter the run history.
- Misconfigured or disconnected nodes should produce validation feedback.

#### TECHNICAL REQUIREMENTS
- Use local workflow data and state.
- Use a graph/canvas library if already available; otherwise implement a simple robust layout.
- Verify node selection, simulated run, and retry/approval flow.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: workflow features implemented, simulation behavior, verification performed, and simplifications.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-12"></a>

<details>
<summary><strong>12. Design Review Board - Pin Comments Directly Onto Screens</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition web app called Design Review Board: a visual review workspace where users pin comments directly onto uploaded screen mockups and resolve design feedback.

This must not be a comment list beside an image. The spatial pinning, threaded feedback, status, and screen navigation must be central to the experience.

#### FIRST SCREEN - FEEDBACK ON THE ARTIFACT
- Open on a selected screen mockup with visible pinned comments, zoom controls, sidebar threads, reviewer filters, and status summary.
- Include at least three screens in the project and at least eight comments across open, resolved, and needs-decision states.
- The first interaction should be adding a pin, selecting a comment, or resolving feedback.

#### CORE SYSTEMS
- Screen gallery with versions and review status.
- Pin comments with x/y positions, author, priority, status, and replies.
- Filters by reviewer, priority, status, and screen.
- Compare mode or version notes for before/after design changes.
- Summary of unresolved decisions.

#### INTERACTION AND STATE
- Clicking on the mockup should add a draft pin.
- Selecting a pin should focus the matching thread.
- Resolve/reopen comments and add replies.
- Zoom or fit controls should keep pins aligned.

#### VISUAL AND UX QUALITY
- Should feel like a design tool, not a blog comment section.
- Pins need clear states without covering the whole mockup.
- Desktop is primary; mobile should support review and resolution.

#### DEPTH CHECKPOINTS
- Pins must stay aligned with the mockup during selection and zoom/fit changes where implemented.
- Thread status changes should update project summary counts.
- Screen switching should preserve and show screen-specific comments.

#### TECHNICAL REQUIREMENTS
- Use local placeholder mockups built with HTML/CSS or lightweight inline assets.
- Store comments in local state.
- Verify pin selection, add/reply, resolve, and screen switching.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: review interactions implemented, spatial pin behavior, verification performed, and known gaps.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

## Data-To-Decision Workspaces

<a id="prompt-13"></a>

<details>
<summary><strong>13. Ad Spend War Room - Campaigns That Explain Themselves</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition analytics workspace called Ad Spend War Room: a self-serve tool where a growth lead can understand campaign performance, spot waste, and decide what to change today.

This must not be a generic chart dashboard, a table dump, or a fake analytics page with vague metrics. It should feel like a decision room: every chart, table, alert, and recommendation should help answer what to pause, scale, inspect, or fix.

#### FIRST SCREEN - WHAT SHOULD CHANGE TODAY?
- Open on an action-oriented overview. The first screen should show total spend, revenue, ROAS, wasted spend, strongest campaign, weakest campaign, and three recommended actions.
- Include a comparison period so the user can see what changed from last week.
- The first visible table should rank campaigns by decision urgency, not alphabetically.

#### CORE PRODUCT SYSTEM
- Campaign data: include at least 12 sample campaigns across Search, Social, Display, and Retargeting.
- Metrics: spend, impressions, clicks, CPC, conversions, CPA, revenue, ROAS, status, budget, and owner.
- Decision flags: scale, pause, investigate, creative fatigue, tracking issue, budget capped, learning phase.
- Drilldown: selecting a campaign should reveal trend, audience/device breakdown, search terms or creative notes, and recommended next action.
- Scenario controls: let the user simulate budget shifts and see projected effect.

#### INTERACTION AND STATE
- Filters for channel, status, owner, decision flag, and date range.
- Sorting by spend, ROAS, CPA, wasted spend, and urgency.
- Search by campaign name.
- A recommendation panel should update when filters or selected campaign change.
- Include empty state when filters return no campaigns and a warning state for suspicious tracking data.

#### VISUAL AND UX QUALITY
- The UI should be dense, crisp, and operational. Avoid marketing-style hero sections.
- Use visual hierarchy to separate executive summary, action queue, trend analysis, and raw campaign table.
- Charts should be readable and purposeful. Do not include decorative charts that do not support a decision.
- Use color carefully for risk and opportunity. Avoid red/green overload without labels.
- The desktop view should feel like a command center; the mobile view should prioritize alerts and campaign drilldown.

#### DEPTH CHECKPOINTS
- Top recommendations must be traceable to campaign metrics.
- Budget simulation should recalculate projected impact.
- Suspicious tracking data should be represented as a warning, not silently included.

#### TECHNICAL REQUIREMENTS
- Build the full implementation in the current project using the existing stack if one exists.
- Use local sample data and real computed metrics; do not hard-code every displayed number independently.
- Implement interactive filtering, sorting, campaign selection, and at least one budget simulation control.
- Do not require external analytics APIs.
- Verify the main dashboard renders and at least one filter, one sort, and one campaign drilldown work.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize what decisions the tool supports, what interactions work, and what you verified.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: completed requirements, computed metrics, verification performed, known shortcuts, and top three places another model should inspect.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-14"></a>

<details>
<summary><strong>14. CSV Forensics - Find The Story In A Messy Export</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition data app called CSV Forensics: a browser workspace that helps a user inspect a messy CSV export, clean it, find anomalies, and produce a short decision brief.

This must not be a static dashboard or a file-upload facade. The app should include a built-in messy sample dataset and real interactions for cleaning, filtering, inspecting, and summarizing.

#### FIRST SCREEN - THE DATA IS MESSY AND THE TOOL KNOWS IT
- Open with a sample CSV already loaded.
- Show detected columns, row count, missing values, duplicate rows, suspicious outliers, and a preview table.
- The first interaction should let the user apply a cleaning step or inspect an anomaly.

#### CORE SYSTEMS
- Built-in dataset with missing values, inconsistent categories, duplicate IDs, date issues, and numeric outliers.
- Cleaning checklist with preview of impact.
- Profiling for column types, distributions, nulls, uniques, and anomalies.
- Insight board with automatically generated findings.
- Export preview for cleaned data and summary brief.

#### INTERACTION AND STATE
- Toggle cleaning steps and update table/metrics.
- Filter anomalies by type.
- Select a row or column to inspect.
- Mark findings as accepted/rejected and update the brief.

#### VISUAL AND UX QUALITY
- Data-professional, dense, and readable.
- Use tables, histograms, badges, and side panels purposefully.
- Avoid decorative analytics graphics that do not help diagnose data quality.

#### DEPTH CHECKPOINTS
- Cleaning toggles must change row counts, issue counts, or preview values.
- Accepted/rejected findings should alter the generated brief.
- At least three distinct data-quality issue types must be visible.

#### TECHNICAL REQUIREMENTS
- Use local sample data and real computed stats.
- Do not require file upload to prove functionality, though optional upload is welcome.
- Verify cleaning toggle, anomaly filter, and finding-to-brief flow.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: data issues represented, computations implemented, verification performed, and shortcuts.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-15"></a>

<details>
<summary><strong>15. Subscription Leak Detector - Where The Money Quietly Leaves</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition working app called Subscription Leak Detector: a personal or small-business tool that finds waste, duplicate tools, renewal risk, and quiet price increases across recurring subscriptions.

This must not be a generic expense dashboard. The product should help a user decide what to cancel, renegotiate, consolidate, or keep.

#### FIRST SCREEN - MONEY LEAKS FIRST
- Open with monthly recurring spend, annualized cost, upcoming renewals, suspected waste, duplicate categories, and top recommended actions.
- Show a prioritized list of subscriptions by decision urgency.
- The first interaction should let the user mark a subscription as keep/cancel/review.

#### CORE SYSTEMS
- At least 18 sample subscriptions with vendor, category, owner, cost, billing cycle, renewal date, usage level, and contract notes.
- Detection for duplicates, unused tools, annual renewal cliffs, price increases, and orphaned owner.
- Scenario panel showing savings if selected actions are taken.
- Renewal calendar and category breakdown.
- Decision log with reason and expected savings.

#### INTERACTION AND STATE
- Filter by category, owner, renewal window, and recommendation.
- Change decision status and update savings scenario.
- Select subscription for usage, billing history, and cancellation notes.
- Include empty and all-reviewed states.

#### VISUAL AND UX QUALITY
- Financially clear without feeling like a bank app.
- Risk and savings should be visible, labeled, and not dependent on color alone.
- Mobile should prioritize upcoming renewals and decisions.

#### DEPTH CHECKPOINTS
- Savings scenario must update from real keep/cancel/review decisions.
- Duplicate subscriptions should be grouped or explained.
- Renewal timing should affect urgency.

#### TECHNICAL REQUIREMENTS
- Use local sample data and computed totals.
- No banking APIs.
- Verify filtering, decision update, and savings calculation.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: detection logic implemented, interactive decisions, verification performed, and simulated assumptions.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-16"></a>

<details>
<summary><strong>16. Support Inbox Intelligence - Turn Tickets Into Product Signals</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser app called Support Inbox Intelligence: a workspace that clusters customer support tickets into product signals, urgency, themes, and recommended next actions.

This must not be a generic inbox UI. It should help product and support teams understand what customers are really asking for and what to fix first.

#### FIRST SCREEN - THE PATTERNS ARE VISIBLE
- Open with a ticket inbox, theme clusters, urgency summary, affected customer segments, and recommended product actions.
- Include at least 24 sample tickets with varied sentiment, plan, topic, and status.
- The first interaction should let the user select a theme, triage a ticket, or create an action item.

#### CORE SYSTEMS
- Ticket list with customer, plan, sentiment, topic, age, status, and summary.
- Theme clustering such as billing confusion, onboarding friction, missing integration, performance, bug, feature request.
- Product signal panel with frequency, revenue affected, severity, and suggested owner.
- Triage states: new, needs reply, escalated, product backlog, resolved.
- Draft response or internal note for selected tickets.

#### INTERACTION AND STATE
- Filter by theme, plan, sentiment, status, and severity.
- Change ticket status and watch counts update.
- Promote a cluster into a product action.
- Search ticket text and show no-results state.

#### VISUAL AND UX QUALITY
- Operational and text-heavy without becoming cramped.
- Clear distinction between individual tickets and aggregate product signals.
- Mobile should support triage and theme review.

#### DEPTH CHECKPOINTS
- Theme clusters must update counts when ticket filters/statuses change.
- Promoting a cluster should create a visible product action.
- Ticket-level and aggregate views must remain connected.

#### TECHNICAL REQUIREMENTS
- Use local sample ticket data and deterministic clustering metadata.
- Do not require AI APIs.
- Verify filters, status updates, and action creation.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: ticket intelligence features, state updates, verification performed, and simulated AI pieces.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-17"></a>

<details>
<summary><strong>17. Workout Progress Lab - Training Load, Recovery And Plateaus</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition web app called Workout Progress Lab: a training analysis workspace that helps an athlete understand load, recovery, strength progress, plateaus, and next-week adjustments.

This must not be a generic fitness dashboard. It should turn workout history into coaching decisions while avoiding medical claims.

#### FIRST SCREEN - SHOULD I PUSH OR RECOVER?
- Open with weekly training load, recovery risk, recent PRs, plateau warnings, and recommended next workout adjustment.
- Show a selected lift or activity with trend, volume, intensity, and notes.
- The first interaction should let the user log a workout or change next week's plan.

#### CORE SYSTEMS
- Sample workout history for strength and conditioning across at least six weeks.
- Metrics: volume, intensity, estimated max, consistency, rest days, soreness, and readiness.
- Plateau detection for stagnant lifts or overreaching.
- Plan adjustment suggestions with rationale.
- Exercise detail view with history and notes.

#### INTERACTION AND STATE
- Add workout set, update readiness, switch exercise, and adjust plan.
- Charts and recommendations should update from state.
- Include deload, missed week, and high-fatigue states.

#### VISUAL AND UX QUALITY
- Athletic but not gimmicky.
- Charts should be readable and tied to decisions.
- Mobile should support logging and quick readiness review.

#### DEPTH CHECKPOINTS
- Workout logging must update at least one trend or recommendation.
- Plateau/fatigue signals should be tied to sample history.
- Advice must stay coaching-oriented and avoid medical certainty.

#### TECHNICAL REQUIREMENTS
- Use local data and computed trends.
- No wearables or health APIs required.
- Verify workout logging and recommendation update.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: computed metrics, interactive flows, verification performed, and health-related limitations.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-18"></a>

<details>
<summary><strong>18. Revenue Cohort Explorer - Retention, Expansion And Churn In One View</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition analytics app called Revenue Cohort Explorer: a SaaS workspace for understanding retention, expansion, churn, and cohort behavior.

This must not be a generic revenue dashboard. It should let a user compare cohorts, inspect accounts, and decide where growth or churn risk is coming from.

#### FIRST SCREEN - COHORTS BEFORE VANITY METRICS
- Open with a cohort heatmap, MRR movement summary, churn alerts, expansion wins, and selected cohort detail.
- Include sample cohorts across at least 12 months.
- The first interaction should let the user select a cohort cell or filter by segment.

#### CORE SYSTEMS
- Cohort table by signup month and months since signup.
- Account list with plan, segment, MRR, expansion, contraction, churn risk, and health notes.
- MRR bridge for new, expansion, contraction, churn, and reactivation.
- Filters by segment, plan, acquisition source, and account owner.
- Insight panel explaining why selected cohort changed.

#### INTERACTION AND STATE
- Select heatmap cells and update account detail.
- Filter and recompute summary metrics.
- Mark account risk and update churn watchlist.
- Include empty and low-data states.

#### VISUAL AND UX QUALITY
- Executive-readable but analyst-useful.
- Heatmap colors need labels and accessible contrast.
- Avoid decorative charts and vague "AI insights".

#### DEPTH CHECKPOINTS
- Heatmap cell selection must drive the account list and insight panel.
- MRR bridge values should be computed from account movements.
- Filters should recompute summary and cohort views.

#### TECHNICAL REQUIREMENTS
- Use local sample data and computed cohort metrics.
- Do not hard-code every displayed number.
- Verify cohort selection, filtering, and risk update.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: cohort computations, interactions, verification performed, and caveats.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

## Playable Browser Worlds

<a id="prompt-19"></a>

<details>
<summary><strong>19. Desert Evacuation Drive - Sandstorm, Signal Truck, Playable Escape</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser-based 3D demo called Desert Evacuation Drive: a cinematic emergency driving scene at a desert music festival as a sandstorm rolls in and the player must reach a signal truck.

This must not be a static 3D scene, a car on an empty plane, a generic driving toy, or a dark foggy demo that hides missing detail. It should open with cinematic impact, then become immediately playable with clear goals and stable controls.

#### FIRST MOMENT - 12 SECONDS OF CINEMA, THEN CONTROL
- Open with a 12-15 second intro camera sequence: festival lights in dusty air, tents whipping in wind, people moving toward evacuation lanes, a distant signal truck blinking through sand, and the player's vehicle waiting in the foreground.
- After the intro, control should transfer clearly to the player with an objective: reach the signal truck before visibility collapses.
- The first playable view must show road direction, obstacles, distance to target, speed, and storm intensity.

#### WORLD AND GAME SYSTEM
- Environment: desert festival grounds with stage structures, tents, barricades, parked vans, light towers, dust plumes, flags, generator carts, and evacuation signs.
- Driving: forward/reverse, steering, acceleration, braking, collision feedback, and reset.
- Objective: reach multiple checkpoint beacons leading to the signal truck.
- Storm system: visibility, wind streaks, dust color, and light bloom should intensify over time.
- Feedback: checkpoint reached, collision warning, wrong direction hint, final arrival state.

#### INTERACTION AND STATE
- Include keyboard controls and visible control hints.
- Include a restart button and a camera toggle if appropriate.
- Vehicle movement should be stable and understandable, not twitchy or impossible to steer.
- Collision should be forgiving enough to keep playing but visible enough to judge implementation.
- Include win/fail or at least success/timeout states.

#### VISUAL AND UX QUALITY
- The scene must have depth, landmarks, and readable navigation despite the sandstorm.
- Use cinematic lighting: amber dust, emergency strobes, stage glow, headlights, and beacon pulses.
- The UI overlay should be compact and game-like, not a web form pasted over a canvas.
- Avoid clipping through major objects during the intro and normal driving.
- The demo should feel alive through motion: flags, dust, lights, moving silhouettes, or animated props.

#### DEPTH CHECKPOINTS
- The intro must transition into player control clearly.
- Vehicle movement, checkpoints, and storm intensity should all be visible.
- Performance choices should preserve scene density without going blank or muddy.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an appropriate existing 3D library if available in the project.
- If using Three.js from a CDN, pin a stable version and import consistently.
- Keep performance smooth on a modern laptop: use instancing or simple geometry where appropriate, clamp pixel ratio if needed, and avoid excessive object counts.
- Do not require external models, paid APIs, or large downloads.
- Verify that the canvas renders, the intro completes, controls work, and the scene is not blank.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize the controls, the objective, performance choices, and what you verified.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: completed requirements, controls and game states, verification performed, known shortcuts, and top three places another model should inspect.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-20"></a>

<details>
<summary><strong>20. Tiny Factory That Teaches Itself - Belts, Bottlenecks And Upgrades</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition playable browser simulation called Tiny Factory That Teaches Itself: a compact factory where belts, machines, buffers, bottlenecks, and upgrades form a visible production loop.

This must not be a static factory illustration or a clicker with numbers only. The player should see materials move, understand bottlenecks, and improve throughput.

#### FIRST MOMENT - THE LOOP IS ALREADY RUNNING
- Open on a small animated factory with resources moving from input to machines to output.
- Show throughput, bottleneck, backlog, money, and upgrade options.
- The first interaction should upgrade, reroute, pause, or inspect a machine.

#### WORLD AND GAME SYSTEM
- At least four machine types with different speeds and outputs.
- Belts or paths that visibly move items.
- Bottleneck detection and highlighted slow points.
- Upgrades for speed, capacity, reliability, or routing.
- Goals such as hit target output before time runs out.

#### INTERACTION AND STATE
- Let the player upgrade machines and see throughput change.
- Include pause/play, speed control, reset, and selected-machine details.
- Include jam/failure or maintenance state.

#### VISUAL AND UX QUALITY
- Clear toy-like simulation with readable motion and labels.
- Avoid tiny unreadable sprites and chaotic animations.
- UI overlay should be compact and game-like.

#### DEPTH CHECKPOINTS
- Items must visibly move through the factory loop.
- Upgrades must change throughput, bottleneck, or goal progress.
- The simulation should have enough rules that reviewers can improve or break it.

#### TECHNICAL REQUIREMENTS
- Use canvas/SVG/HTML or a game library appropriate to the stack.
- Use local simulation state and a real update loop.
- Verify animation, upgrade, reset, and goal state.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: simulation rules, controls, verification performed, and simplifications.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-21"></a>

<details>
<summary><strong>21. Rooftop Drone Rescue - Wind, Battery And Path Planning</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition playable browser game called Rooftop Drone Rescue: the player pilots a rescue drone across rooftops while managing wind, battery, payload, and safe landing zones.

This must not be a generic top-down square moving around. The drone constraints should create meaningful decisions.

#### FIRST MOMENT - RESCUE ROUTE UNDER PRESSURE
- Open on a city rooftop map with drone, survivor beacon, wind direction, battery, payload status, and landing zones.
- The first interaction should be flying or plotting a route.
- The goal must be obvious: reach the survivor, pick up supplies or payload, and return safely.

#### WORLD AND GAME SYSTEM
- Rooftop obstacles, no-fly zones, wind corridors, charging pads, and rescue targets.
- Drone movement affected by wind or battery drain.
- Battery, altitude or payload limits.
- Checkpoints, rescue completion, fail/retry states.
- Optional route preview or path planning mode.

#### INTERACTION AND STATE
- Keyboard or pointer controls.
- Battery and wind should visibly affect play.
- Include restart, pause, and difficulty toggle.
- Show feedback for collision, low battery, rescue success, and unsafe landing.

#### VISUAL AND UX QUALITY
- Clear city layout with readable hazards and route options.
- Avoid visual clutter that makes the objective unclear.
- UI should feel like a mission HUD, not a dashboard pasted onto a game.

#### DEPTH CHECKPOINTS
- Wind or battery must meaningfully affect route choices.
- Rescue success/failure should be visible and recoverable.
- The HUD must explain objective, constraints, and current risk at a glance.

#### TECHNICAL REQUIREMENTS
- Use local game state and a real loop.
- No external assets required.
- Verify controls, battery drain, rescue success/failure, and restart.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: game mechanics, controls, verification performed, and known limitations.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-22"></a>

<details>
<summary><strong>22. Ecosystem Sandbox - Water, Plants, Weather And Balance</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition interactive browser sandbox called Ecosystem Sandbox: a living system where water, plants, weather, soil, and small organisms affect each other over time.

This must not be a static nature animation. User choices should change the balance of the system and create visible consequences.

#### FIRST MOMENT - A LIVING SYSTEM, NOT A SCREENSAVER
- Open on a visible ecosystem with moving weather, water level, plant growth, organism activity, and balance indicators.
- The first interaction should change rain, add plants, adjust temperature, or introduce organisms.
- The user should immediately see cause and effect.

#### WORLD AND SYSTEM
- Variables: water, sunlight, temperature, soil nutrients, plant density, organism population, biodiversity.
- Weather cycles with rain/drought/sun.
- Growth and decay over time.
- Balance states such as thriving, stressed, flooded, drought, overgrazed.
- Timeline or event log explaining major changes.

#### INTERACTION AND STATE
- Controls for weather, planting, watering, speed, reset, and scenario presets.
- Visual changes must match state changes.
- Include warnings and recovery suggestions.

#### VISUAL AND UX QUALITY
- Organic and readable, not a dashboard with a nature wallpaper.
- Use motion and color to show health and change.
- Mobile should support scenario controls and overview.

#### DEPTH CHECKPOINTS
- At least two user controls must produce different ecosystem outcomes.
- Balance states should emerge from variables, not only button labels.
- The event log or explanation should connect cause to visible effect.

#### TECHNICAL REQUIREMENTS
- Use a real simulation loop with local state.
- Canvas/SVG/HTML are all acceptable.
- Verify controls, simulation progression, reset, and at least two ecosystem states.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: simulation variables, user controls, verification performed, and model simplifications.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-23"></a>

<details>
<summary><strong>23. Cyber Train Dispatch - Prevent Delays Across A Living Network</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition playable dispatch simulation called Cyber Train Dispatch: the user manages trains across a busy network, preventing delays, route conflicts, and station overload.

This must not be a static subway map or a decorative animation. The dispatch choices must affect train movement and network health.

#### FIRST MOMENT - THE NETWORK IS ABOUT TO JAM
- Open on an animated rail network with moving trains, stations, route switches, delay warnings, and a dispatch queue.
- The first interaction should reroute, hold, prioritize, or clear a train.
- Include at least one visible conflict that the user can solve.

#### WORLD AND GAME SYSTEM
- Multiple train lines, stations, switches, and passenger-load indicators.
- Trains with destinations, speed, delay, priority, and capacity.
- Conflict detection for shared track segments.
- Scoring based on on-time arrivals, passenger wait, and safety.
- Random events such as signal issue, crowd surge, or disabled train.

#### INTERACTION AND STATE
- Select trains and stations.
- Change route or hold/release trains.
- Simulate time with pause/speed controls.
- Include success, overload, and collision-prevention feedback.

#### VISUAL AND UX QUALITY
- Network should be readable at a glance.
- Use color, line thickness, motion, and labels without overwhelming the map.
- UI should feel like an operations console.

#### DEPTH CHECKPOINTS
- At least one route conflict must be solvable by user action.
- Train movement and delay/score changes should be visible over time.
- Random or scripted events should alter dispatch decisions.

#### TECHNICAL REQUIREMENTS
- Use local simulation data and real movement.
- No external transit APIs required.
- Verify train movement, conflict resolution, and event handling.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: dispatch mechanics, interactions, verification performed, and simplifications.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-24"></a>

<details>
<summary><strong>24. Particle Music Sequencer - Soundless Visual Rhythm Machine</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition interactive browser toy called Particle Music Sequencer: a soundless visual rhythm machine where particles, lanes, beats, patterns, and effects create an understandable composition.

This must not be a static particle background. It should behave like an instrument even if it does not play audio.

#### FIRST MOMENT - A PATTERN IS ALREADY PLAYING
- Open with a running sequencer, visible beat grid, moving particles, active lanes, pattern controls, and playback state.
- The first interaction should toggle a step, change tempo, switch pattern, or adjust an effect.
- The visual rhythm should be obvious without sound.

#### SYSTEM
- Sequencer grid with at least four lanes and sixteen steps.
- Particles triggered by active steps with distinct visual behavior per lane.
- Controls for tempo, density, color mode, pattern, play/pause, clear, randomize.
- Pattern memory or preset slots.
- Visual effects such as trail, gravity, burst size, or lane style.

#### INTERACTION AND STATE
- Toggling steps changes the animation.
- Tempo affects playback speed.
- Randomize and clear should work.
- Include selected-lane details.

#### VISUAL AND UX QUALITY
- Precise, playful, and legible.
- Avoid overwhelming bloom or unreadable controls.
- Layout should keep grid, controls, and canvas stable.

#### DEPTH CHECKPOINTS
- Step toggles must change the visual rhythm immediately.
- Tempo and pattern controls should alter animation timing/state.
- Presets or randomization should create noticeably different compositions.

#### TECHNICAL REQUIREMENTS
- Use a real animation loop.
- No audio dependency required.
- Verify play/pause, step toggle, tempo, randomize, and clear.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: sequencer behavior, controls, verification performed, and limitations.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

## Repair, Rescue, And Refactor

<a id="prompt-25"></a>

<details>
<summary><strong>25. Save This Half-Built App - From Static Mockup To Working Product</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

You are working in an existing project that contains a half-built product UI. Turn it from a static or brittle mockup into a working product slice without changing the product's core concept.

This must not become a rewrite for rewrite's sake, a new unrelated app, or a cosmetic-only pass. The goal is to preserve what is promising, identify what is fake or broken, and make the smallest set of changes that turns the app into something a user can actually try.

#### FIRST STEP - INSPECT BEFORE EDITING
- Inspect the project structure, main screens, component patterns, styling approach, and available scripts before changing files.
- Identify the intended product and the main user flow from the existing code.
- Briefly note the top three gaps that prevent the app from feeling real: state, interaction, layout, data, routing, errors, or performance.

#### CORE RESCUE GOAL
- Pick one primary flow and make it work end to end.
- Replace purely decorative mock elements with local interactive state or coherent sample data.
- Keep the existing visual direction unless it is actively broken.
- Add missing empty, loading, error, or success states only where they support the primary flow.
- Fix obvious responsive layout issues that would make the app unusable on a phone or common laptop size.

#### ENGINEERING DISCIPLINE
- Prefer small, targeted changes over broad rewrites.
- Reuse existing components, helpers, and styling conventions where practical.
- Do not introduce a new framework, state library, router, database, or build tool unless the project already points that way.
- Do not delete large sections of existing functionality just to simplify the task.
- If something is ambiguous, make a reasonable assumption and state it in the final summary.

#### DEPTH CHECKPOINTS
- The chosen primary flow must become actually usable, not merely prettier.
- Changes should preserve the original product identity.
- The summary must separate implemented work from assumptions and shortcuts.

#### VERIFICATION REQUIREMENTS
- Run the relevant install/build/test/dev command if available and practical.
- If a dev server or preview is available, inspect the actual rendered result.
- Verify the primary flow manually or through tests.
- If verification is blocked, explain exactly what prevented it and what you checked instead.

#### QUALITY BAR
- The finished result should feel like a rescued product slice: still recognizably the original app, but now operable.
- The user should be able to open it, understand the main flow, interact with it, and see state changes persist during the session.
- The final answer should focus on what changed, what works now, what was verified, and what risk remains.

#### FINAL OUTPUT INSTRUCTION
Make the rescue changes now. When finished, summarize the primary flow you chose, the files changed, the verification performed, and any remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: primary flow rescued, changes made, verification performed, known shortcuts, and top three places another model should inspect.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-26"></a>

<details>
<summary><strong>26. Performance Rescue - Keep The Spectacle, Remove The Jank</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

You are working in an existing app or demo that looks ambitious but performs poorly. Improve runtime performance while preserving the core visual or product experience.

This must not become a visual downgrade disguised as optimization. The goal is to identify the actual sources of jank, make targeted improvements, and keep the experience impressive.

#### FIRST STEP - MEASURE OR OBSERVE BEFORE EDITING
- Inspect the project structure, rendering path, data flow, and performance-sensitive areas.
- Run or preview the app if practical.
- Identify likely causes such as too many re-renders, expensive loops, layout thrash, unbounded animations, large data operations, or heavy 3D objects.

#### CORE RESCUE GOAL
- Preserve the main visual/product promise.
- Reduce unnecessary work through memoization, batching, throttling, instancing, virtualization, simplified geometry, or smarter state boundaries as appropriate.
- Keep behavior and controls intact.
- Add a lightweight performance note or debug indicator if useful.

#### ENGINEERING DISCIPLINE
- Make small, explainable changes.
- Do not swap frameworks, rewrite the whole app, or remove major features to hide the problem.
- Avoid premature optimization unrelated to the observed issue.
- Keep code readable.

#### DEPTH CHECKPOINTS
- Optimization must name a plausible bottleneck and the specific mitigation used.
- The main spectacle or product promise should remain visible.
- Before/after evidence can be qualitative, but must be honest.

#### VERIFICATION REQUIREMENTS
- Verify the app still renders and the primary interaction still works.
- Compare before/after behavior using available signals: frame feel, render count, console, build output, or profiler if practical.
- Note what could not be measured.

#### QUALITY BAR
- The final result should feel smoother while still recognizably being the same ambitious app.
- The final summary should explain the bottleneck, changes, tradeoffs, and remaining risk.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: suspected bottlenecks, optimizations made, verification performed, and any visual compromises.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-27"></a>

<details>
<summary><strong>27. Mobile Overflow Cleanup - Make The Desktop Beauty Survive A Phone</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

You are working in an existing web app that looks good on desktop but breaks on mobile. Make the core experience responsive and usable without redesigning the product from scratch.

This must not be a superficial media-query pass. The goal is to fix real layout, text, control, and navigation issues so the app works on common phone widths.

#### FIRST STEP - FIND THE BREAKS
- Inspect the main screens and styling approach.
- Run or preview the app if practical.
- Identify likely mobile failures: overflow, clipped text, unusable controls, stacked panels, fixed widths, hidden actions, or impossible tables.

#### CORE RESCUE GOAL
- Preserve the desktop design direction.
- Make the primary flow usable on mobile.
- Fix text wrapping, button sizing, panel stacking, tables/lists, navigation, and sticky controls.
- Add mobile-specific hierarchy where needed, such as summary-first panels, tabs, accordions, or horizontal scroll only when appropriate.

#### ENGINEERING DISCIPLINE
- Reuse existing classes/components where possible.
- Avoid deleting desktop functionality.
- Do not hide core actions on mobile.
- Keep responsive rules understandable.

#### DEPTH CHECKPOINTS
- Mobile fixes must address actual overflow/clipping/unreachable controls.
- Desktop behavior should be checked after responsive changes.
- The primary user flow must remain complete on phone width.

#### VERIFICATION REQUIREMENTS
- Verify at desktop and mobile viewport sizes.
- Check for horizontal page overflow, clipped labels, overlapping text, and unreachable actions.
- If browser verification is blocked, explain what static checks were performed.

#### QUALITY BAR
- The mobile result should feel intentionally designed, not squeezed.
- The desktop should remain intact.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: mobile issues fixed, viewports checked, verification performed, and remaining responsive risk.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-28"></a>

<details>
<summary><strong>28. Design System Migration - Tokens, Components And No Regressions</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

You are working in an existing app with repeated UI patterns, inconsistent spacing, color, typography, and component variants. Migrate the visible surface toward a small design system without changing product behavior.

This must not become an abstract design-system project detached from the app. The user should see a more consistent product, and the code should become easier to extend.

#### FIRST STEP - AUDIT THE SURFACE
- Inspect repeated buttons, cards, panels, forms, tables, status labels, spacing, and colors.
- Identify the smallest set of tokens/components that will reduce meaningful inconsistency.
- Avoid touching unrelated logic.

#### CORE MIGRATION GOAL
- Introduce or consolidate tokens for color, spacing, radius, typography, and states.
- Extract or standardize core components such as button, input, panel, badge, table row, empty state, or toolbar.
- Apply the system to one or more real screens.
- Preserve existing interactions and data behavior.

#### ENGINEERING DISCIPLINE
- Keep the migration incremental.
- Do not rename everything for aesthetics.
- Do not introduce a large UI library unless the project already uses it.
- Keep compatibility with existing styles.

#### DEPTH CHECKPOINTS
- Tokens/components should replace real repeated patterns, not create unused abstractions.
- At least one visible screen should use the migrated system.
- Behavioral changes should be avoided or explicitly justified.

#### VERIFICATION REQUIREMENTS
- Run available checks.
- Preview the affected screen if practical.
- Verify that core interactions still work after component consolidation.

#### QUALITY BAR
- The app should look more coherent immediately.
- The design system should be small, visible, and justified by repeated usage.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: components/tokens created, screens migrated, verification performed, and regression risks.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-29"></a>

<details>
<summary><strong>29. Test The Untested Flow - Add Confidence Without Rewriting The App</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

You are working in an existing project with an important user flow that has little or no test coverage. Add practical confidence around that flow without rewriting the app.

This must not become a testing-theater exercise. The tests should cover behavior that would matter to a user or maintainer.

#### FIRST STEP - DISCOVER TEST PATTERNS
- Inspect the project structure, test framework, scripts, and existing tests.
- Identify one important flow that is currently weakly covered.
- Understand how the app expects tests to be written before adding new tools.

#### CORE TESTING GOAL
- Add focused tests for the chosen flow.
- Cover at least one success path and one failure, empty, validation, or edge state.
- If the flow requires minor testability improvements, make the smallest safe changes.
- Keep implementation behavior unchanged unless you uncover a bug, then fix it narrowly.

#### ENGINEERING DISCIPLINE
- Do not introduce a new test framework if one exists.
- Do not snapshot-test everything just to claim coverage.
- Do not mock away the behavior being tested.
- Keep tests readable and maintainable.

#### DEPTH CHECKPOINTS
- Tests should cover user-observable behavior, not only implementation details.
- At least one negative or edge state should be tested.
- The chosen test style should match existing project conventions.

#### VERIFICATION REQUIREMENTS
- Run the relevant test command.
- If tests cannot run, explain exactly why and still provide static confidence.
- Note any existing failing tests separately from your changes.

#### QUALITY BAR
- A future maintainer should understand what behavior is protected and why.
- The final summary should be honest about coverage boundaries.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: flow chosen, tests added, command run, result, and residual risk.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-30"></a>

<details>
<summary><strong>30. Bug Triage Gauntlet - Five Reports, Three Real Bugs, One Clean Patch Set</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

You are working in an existing project with five user bug reports. Triage them, identify which are real and actionable, fix the highest-value issues, and avoid changing behavior for reports that are not bugs.

Bug reports:
1. "Search loses my query when I switch tabs."
2. "The export button is broken because it does not download anything in the demo account."
3. "On mobile, the details drawer covers the save button."
4. "The app is slow after I import 500 rows."
5. "The status says synced even after I edit a field offline."

This must not become five rushed patches. The goal is to reason carefully, reproduce or inspect the likely paths, and produce a clean patch set for the real issues you can verify.

#### FIRST STEP - TRIAGE BEFORE FIXING
- Inspect the codebase and identify relevant areas for each report.
- Classify each report as likely bug, expected behavior, unclear, or needs product decision.
- Pick the most valuable real bugs to fix within the current scope.

#### CORE REPAIR GOAL
- Fix at least two real issues if the codebase supports them.
- Keep changes isolated and explain why any report was not fixed.
- Add or update tests where the project has a relevant pattern.
- Preserve intended behavior, especially around demo restrictions and offline/sync semantics.

#### ENGINEERING DISCIPLINE
- Do not rewrite major systems to solve small bugs.
- Do not mark every report as fixed without evidence.
- Do not remove constraints such as demo mode just to satisfy a report.
- Keep commits or changes logically grouped in the final explanation.

#### DEPTH CHECKPOINTS
- Each bug report must be classified before fixing.
- Fixed items need individual verification notes.
- Reports that are expected behavior or unclear must not be force-fit into code changes.

#### VERIFICATION REQUIREMENTS
- Run relevant tests or manual verification.
- Verify each fixed report individually.
- For unfixed reports, state what evidence is missing or what product decision is needed.

#### QUALITY BAR
- The result should look like senior bug triage: calm, scoped, evidence-based, and honest.
- The final answer should separate fixed, not-a-bug, unclear, and deferred items.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: triage table, fixes made, verification performed per report, and unresolved risks.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>
## Global Landmark Architecture Modeling

<a id="prompt-31"></a>

<details>
<summary><strong>31. Asia - Taj Mahal Architectural Model, Marble Symmetry And Garden Axis</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page.
- Use local geometry, procedural materials, and local state. Do not require paid assets, external 3D models, or large downloads.
- Make the result comparable across model runs: preserve the landmark, continent, core geometry, and inspection controls.
- Before finishing, verify that the 3D scene renders, the camera controls work, and the main architectural features are visible.
- In the final response, report only what matters for evaluation: what was built, how to open it, what can be inspected, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser-based 3D architectural model of the Taj Mahal in Agra, India, representing Asia in a global landmark modeling series.

This must not be a generic white palace, a single dome on a box, or a flat postcard scene. The model should make the Taj Mahal recognizable through symmetry, central marble mausoleum massing, onion dome, four minarets, iwans, garden axis, reflecting pool, plinth, and river-facing context.

#### FIRST VIEW - THE SYMMETRY MUST READ IMMEDIATELY
- Open with a cinematic camera view aligned to the long Charbagh garden axis, looking across the reflecting pool toward the central mausoleum.
- The first frame should show the main dome, four minarets, central arch, side wings, garden paths, water reflection, and warm marble light.
- Include a compact overlay naming the landmark, continent, location, and the architectural features currently visible.

#### ARCHITECTURAL MODELING REQUIREMENTS
- Central mausoleum: square plinth, large central iwan arch, smaller side arches, four corner chhatri-like kiosks, onion dome, finial, and layered base.
- Dome system: large central onion dome plus smaller domes/kiosks with different scale and height.
- Minarets: four slender towers on the plinth corners, each with stacked balconies, tapered vertical shape, small domed cap, and slight outward placement.
- Facade detail: use procedural inlay patterns, arch outlines, dark recessed openings, repeated panels, and subtle marble veining.
- Garden axis: long water channel, reflecting pool, stone walkways, cypress-like trees, geometric lawns, and axial symmetry.
- Context: Yamuna river suggestion behind the mausoleum, low horizon haze, visitor-scale figures or markers for scale.

#### INTERACTION AND INSPECTION
- Orbit/pan/zoom camera controls.
- Feature toggles for garden, facade detail, minarets, water reflection, and annotation labels.
- At least four guided camera buttons: Front Axis, Dome Closeup, Minaret Detail, Garden Overview.
- Hover or click labels should identify key features without blocking the model.

#### VISUAL AND MATERIAL QUALITY
- Marble should feel luminous and slightly varied, not pure flat white.
- Water should reflect the silhouette enough to sell the axis.
- Lighting should emphasize dawn or late-afternoon warmth, soft shadows, and the contrast between marble, water, green garden, and sandy stone.
- Avoid excessive bloom, tiny unreadable ornaments, and noisy textures that hide the form.

#### DEPTH CHECKPOINTS
- From the opening view, a reviewer should recognize the Taj Mahal without reading the label.
- The four minarets, main dome, central arch, reflecting pool, and garden axis must all be spatially correct and visible.
- Camera presets and toggles must help inspect the architecture, not just move around a decorative scene.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an equivalent browser 3D approach.
- Build with procedural geometry where possible: boxes, cylinders, spheres, lathed shapes, curves, instancing, or custom meshes.
- Keep the scene performant by reusing geometry/materials and limiting decorative object counts.
- Verify scene rendering, controls, toggles, camera presets, and nonblank canvas.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what architectural features are modeled, what interactions work, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simplified, approximate, fragile, or worth rechecking.
- Cross-audit focus: Taj Mahal recognizability, architectural proportions, symmetry, inspection controls, and performance.
- Self-score from 1-5 for landmark accuracy, first-view impact, modeling detail, interaction depth, visual quality, and verification honesty.
```

</details>

<a id="prompt-32"></a>

<details>
<summary><strong>32. Europe - Sagrada Familia Procedural Facades, Towers And Interior Light</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page.
- Use local geometry, procedural materials, and local state. Do not require paid assets, external 3D models, or large downloads.
- Make the result comparable across model runs: preserve the landmark, continent, core geometry, and inspection controls.
- Before finishing, verify that the 3D scene renders, the camera controls work, and the main architectural features are visible.
- In the final response, report only what matters for evaluation: what was built, how to open it, what can be inspected, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser-based 3D architectural model of La Sagrada Familia in Barcelona, Spain, representing Europe in a global landmark modeling series.

This must not be a generic cathedral, a few cones on a rectangle, or a dark silhouette that hides missing detail. The model should communicate the Sagrada Familia through vertical towers, branching organic structure, dense facades, sculptural portals, stained-glass interior light, and Barcelona urban context.

#### FIRST VIEW - VERTICAL COMPLEXITY AND SACRED LIGHT
- Open with a low street-level camera looking up at the basilica, emphasizing height, clustered towers, carved facade rhythm, and warm city light.
- The first frame should include multiple towers with different heights, portal depth, organic ribs, facade texture, and surrounding urban scale.
- Include a compact overlay naming the landmark, continent, location, and modeled feature groups.

#### ARCHITECTURAL MODELING REQUIREMENTS
- Towers: model multiple tapering towers with perforated or ribbed surfaces, spires, cross/finial suggestions, and varied heights.
- Facades: create at least two visually distinct sides: a denser sculptural facade and a cleaner geometric facade.
- Nave/interior suggestion: include a cutaway, toggle, or visible interior zone with branching columns and stained-glass color shafts.
- Organic structure: use branching columns, angled supports, rib-like geometry, and repeated vertical modules to avoid plain Gothic boxes.
- Surface detail: procedural relief panels, small extrusions, recessed portals, window slots, and clustered ornament density.
- Context: Barcelona street edge, people/trees/cars as scale markers, warm stone palette, and construction-era cranes or scaffolding as optional detail.

#### INTERACTION AND INSPECTION
- Orbit/pan/zoom camera controls.
- Toggle between Exterior, Interior Light, Facade Detail, and Structural Ribs.
- Guided camera buttons: Street Approach, Tower Crown, Portal Detail, Interior Columns.
- Annotation labels should identify towers, portals, branching columns, stained glass, and facade zones.

#### VISUAL AND MATERIAL QUALITY
- Stone should have warm variation, depth, and shadow, not a flat beige tower.
- Stained-glass light should cast recognizable color zones or visible translucent panels.
- The model should balance dense detail with readable massing.
- Avoid noisy micro-ornament that kills performance or hides the silhouette.

#### DEPTH CHECKPOINTS
- A reviewer should see that this is specifically Sagrada Familia, not a generic European church.
- Tower clustering, organic verticality, facade depth, and stained-glass/interior light must all be represented.
- Detail should be procedural and inspectable from more than one camera angle.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an equivalent browser 3D approach.
- Use instancing/repeated modules for tower ribs, windows, facade relief, or columns.
- Provide performance-friendly geometry and clamp pixel ratio if needed.
- Verify scene rendering, controls, toggles, camera presets, and nonblank canvas.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what architectural features are modeled, what interactions work, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simplified, approximate, fragile, or worth rechecking.
- Cross-audit focus: Sagrada Familia recognizability, tower/facade complexity, interior light, procedural detail, and performance.
- Self-score from 1-5 for landmark accuracy, first-view impact, modeling detail, interaction depth, visual quality, and verification honesty.
```

</details>

<a id="prompt-33"></a>

<details>
<summary><strong>33. Africa - Great Pyramid Complex, Limestone Massing And Desert Context</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page.
- Use local geometry, procedural materials, and local state. Do not require paid assets, external 3D models, or large downloads.
- Make the result comparable across model runs: preserve the landmark, continent, core geometry, and inspection controls.
- Before finishing, verify that the 3D scene renders, the camera controls work, and the main architectural features are visible.
- In the final response, report only what matters for evaluation: what was built, how to open it, what can be inspected, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser-based 3D architectural model of the Giza Pyramid Complex in Egypt, representing Africa in a global landmark modeling series.

This must not be one smooth pyramid on a flat sand plane. The model should show monumental scale, pyramid geometry, limestone block layers, multiple pyramids, causeway/tomb context, desert atmosphere, and human-scale comparison.

#### FIRST VIEW - SCALE BEFORE DETAIL
- Open with a wide desert camera view at low sun angle, showing the Great Pyramid, neighboring pyramids, foreground stone blocks, long shadows, and small human/vehicle scale markers.
- The first frame should make the mass and geometry unmistakable, with desert haze and a sense of distance.
- Include a compact overlay naming the landmark, continent, location, and modeled scale features.

#### ARCHITECTURAL MODELING REQUIREMENTS
- Great Pyramid: accurate square base, triangular faces, slight stepped/block surface, optional missing casing stones, and top cap suggestion.
- Complex: include at least three pyramids with different sizes, smaller queen pyramids or mastaba-like structures, and a causeway/ceremonial path.
- Surface detail: layered limestone blocks, edge wear, color variation, and shadow-catching seams.
- Desert terrain: dunes, sand ripples, scattered stones, sun-baked material, and atmospheric dust.
- Scale context: visitor markers, camel/vehicle silhouettes or measurement posts, and labels showing height/base relationships.
- Optional Sphinx silhouette or distant plateau elements, but do not let it steal focus from the pyramid complex.

#### INTERACTION AND INSPECTION
- Orbit/pan/zoom camera controls.
- Toggle block layers, smooth casing reconstruction, scale markers, and site labels.
- Guided camera buttons: Plateau Wide, Great Pyramid Base, Block Detail, Complex Overview.
- Include a measurement/annotation overlay for base, height, slope, and alignment.

#### VISUAL AND MATERIAL QUALITY
- Stone should feel heavy, weathered, and sunlit, not plastic yellow.
- Use strong shadows and warm desert color, with enough contrast to read block layers.
- The environment should support scale without becoming empty.
- Avoid overpopulating the scene with decorative props.

#### DEPTH CHECKPOINTS
- The scene must include more than one pyramid and communicate the complex, not only a single icon.
- Block/step texture, human scale, and desert lighting must make the monument's size legible.
- Toggles should reveal modeling differences such as block layers versus smoother reconstruction.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an equivalent browser 3D approach.
- Use procedural geometry/materials for pyramids, block layers, dunes, and labels.
- Keep performance smooth by reusing geometry and limiting high-poly terrain.
- Verify scene rendering, controls, toggles, camera presets, and nonblank canvas.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what architectural features are modeled, what interactions work, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simplified, approximate, fragile, or worth rechecking.
- Cross-audit focus: pyramid complex scale, block layering, desert context, inspection controls, and performance.
- Self-score from 1-5 for landmark accuracy, first-view impact, modeling detail, interaction depth, visual quality, and verification honesty.
```

</details>

<a id="prompt-34"></a>

<details>
<summary><strong>34. North America - Empire State Building, Art Deco Vertical City Model</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page.
- Use local geometry, procedural materials, and local state. Do not require paid assets, external 3D models, or large downloads.
- Make the result comparable across model runs: preserve the landmark, continent, core geometry, and inspection controls.
- Before finishing, verify that the 3D scene renders, the camera controls work, and the main architectural features are visible.
- In the final response, report only what matters for evaluation: what was built, how to open it, what can be inspected, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser-based 3D architectural model of the Empire State Building in New York City, representing North America in a global landmark modeling series.

This must not be a plain skyscraper box, a generic skyline, or a flat silhouette. The model should communicate Art Deco verticality, stepped setbacks, window grid density, spire/mast, limestone/metal material contrast, and Manhattan street context.

#### FIRST VIEW - VERTICAL CITY ICON
- Open with a street-canyon camera looking upward from a Manhattan avenue, showing the tower rising through setbacks to the spire.
- The first frame should show base massing, vertical ribs, window rhythm, stepped crown, mast, surrounding smaller buildings, traffic/light scale, and evening or dawn atmosphere.
- Include a compact overlay naming the landmark, continent, location, and modeled feature groups.

#### ARCHITECTURAL MODELING REQUIREMENTS
- Massing: stacked rectangular volumes with accurate Art Deco setbacks and a strong vertical central shaft.
- Facade: dense window grid, vertical piers/ribs, darker recessed window bands, and warmer stone cladding.
- Crown: stepped top, observation deck suggestion, antenna/mast/spire, beacon light, and metal cap contrast.
- Base/street: sidewalk, neighboring buildings, street lanes, small vehicles/people, and entry canopy suggestion.
- Lighting: day/night toggle or animated city lights to reveal windows and crown.
- Scale: include height markers or camera presets that show base-to-spire proportion.

#### INTERACTION AND INSPECTION
- Orbit/pan/zoom camera controls.
- Toggle facade grid, night lights, surrounding city blocks, and annotation labels.
- Guided camera buttons: Street Canyon, Crown And Spire, Facade Grid, Skyline View.
- Include a simple section/height indicator or floor band overlay.

#### VISUAL AND MATERIAL QUALITY
- The building should feel tall through camera, proportions, shadows, and surrounding scale.
- Windows should be patterned and varied enough to read as a facade system.
- Art Deco geometry should be clean and vertical, not a glass office tower.
- Avoid making surrounding buildings more detailed than the landmark.

#### DEPTH CHECKPOINTS
- A reviewer should recognize the Empire State Building from massing and crown, not only from a label.
- Setbacks, window rhythm, vertical ribs, and spire must all be modeled.
- Night/day or facade toggles should reveal meaningful architectural layers.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an equivalent browser 3D approach.
- Use instancing or repeated geometry for window grids and city blocks.
- Keep draw calls reasonable and avoid excessive individual window meshes if performance suffers.
- Verify scene rendering, controls, toggles, camera presets, and nonblank canvas.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what architectural features are modeled, what interactions work, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simplified, approximate, fragile, or worth rechecking.
- Cross-audit focus: Art Deco recognizability, vertical proportion, facade repetition, city context, and performance.
- Self-score from 1-5 for landmark accuracy, first-view impact, modeling detail, interaction depth, visual quality, and verification honesty.
```

</details>

<a id="prompt-35"></a>

<details>
<summary><strong>35. South America - Machu Picchu Citadel, Terraces And Mountain Topography</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page.
- Use local geometry, procedural materials, and local state. Do not require paid assets, external 3D models, or large downloads.
- Make the result comparable across model runs: preserve the landmark, continent, core geometry, and inspection controls.
- Before finishing, verify that the 3D scene renders, the camera controls work, and the main architectural features are visible.
- In the final response, report only what matters for evaluation: what was built, how to open it, what can be inspected, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser-based 3D architectural and landscape model of Machu Picchu in Peru, representing South America in a global landmark modeling series.

This must not be a random stone village on a hill. The model should communicate the mountain citadel through terraces, dry-stone walls, roofless structures, sacred plaza organization, steep topography, Huayna Picchu-like backdrop, paths, clouds, and altitude.

#### FIRST VIEW - CITADEL ABOVE THE CLOUDS
- Open with a high oblique camera showing the terraces stepping down the ridge, central stone building clusters, mountain backdrop, mist, and dramatic drop-offs.
- The first frame should show the relationship between architecture and terrain, not only isolated buildings.
- Include a compact overlay naming the landmark, continent, location, and modeled feature groups.

#### ARCHITECTURAL AND LANDSCAPE MODELING REQUIREMENTS
- Terraces: many stepped agricultural terraces following terrain contours, with retaining walls and grass/stone material contrast.
- Building clusters: roofless stone rooms, walls, door openings, plazas, stair paths, and different precincts.
- Sacred/urban layout: central plaza, temple-like zone, residential-like zone, and path network.
- Terrain: steep ridge, surrounding mountain peaks, valley depth, cloud layers, and vegetation patches.
- Stone detail: irregular masonry suggestion, wall thickness, weathering, and scale markers.
- Atmosphere: moving mist/clouds, high-altitude light, soft shadows, and depth haze.

#### INTERACTION AND INSPECTION
- Orbit/pan/zoom camera controls.
- Toggle terrain contours, terrace labels, building zones, paths, and mist.
- Guided camera buttons: Classic Overlook, Terrace Detail, Plaza Walkthrough, Mountain Context.
- Include annotation labels for terraces, plaza, temple zone, residential zone, and mountain backdrop.

#### VISUAL AND MATERIAL QUALITY
- The site should feel integrated with the mountain, not placed on a flat platform.
- Stone walls should read as constructed masonry even if simplified.
- Clouds/mist should add altitude without hiding the model.
- Avoid making the scene too green and smooth; the geometry should show hard terraces and rugged topography.

#### DEPTH CHECKPOINTS
- The terrain/architecture relationship must be visible from the first view.
- Terraces, stone structures, paths, and mountain backdrop must all be separately inspectable.
- Camera presets should reveal both macro site planning and close masonry detail.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an equivalent browser 3D approach.
- Use procedural terrain, stepped geometry, instancing, or repeated wall modules.
- Keep performance smooth by simplifying terrain mesh and reusing terrace components.
- Verify scene rendering, controls, toggles, camera presets, and nonblank canvas.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what architectural features are modeled, what interactions work, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simplified, approximate, fragile, or worth rechecking.
- Cross-audit focus: Machu Picchu recognizability, terrace/terrain integration, stone detail, guided inspection, and performance.
- Self-score from 1-5 for landmark accuracy, first-view impact, modeling detail, interaction depth, visual quality, and verification honesty.
```

</details>

<a id="prompt-36"></a>

<details>
<summary><strong>36. Oceania - Sydney Opera House, Shell Roofs And Harbor Setting</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page.
- Use local geometry, procedural materials, and local state. Do not require paid assets, external 3D models, or large downloads.
- Make the result comparable across model runs: preserve the landmark, continent, core geometry, and inspection controls.
- Before finishing, verify that the 3D scene renders, the camera controls work, and the main architectural features are visible.
- In the final response, report only what matters for evaluation: what was built, how to open it, what can be inspected, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser-based 3D architectural model of the Sydney Opera House in Sydney, Australia, representing Oceania in a global landmark modeling series.

This must not be a few white triangles on a platform or a generic harbor scene. The model should communicate the Opera House through grouped shell roofs, tile-like surface segmentation, podium/base, glass walls, harbor water, promenade, and Sydney context.

#### FIRST VIEW - SHELLS OVER THE HARBOR
- Open with a harbor-side camera showing the shell roof groups rising from the podium, water reflections, promenade, and distant bridge/city context.
- The first frame should make the silhouette instantly recognizable while preserving enough detail to inspect.
- Include a compact overlay naming the landmark, continent, location, and modeled feature groups.

#### ARCHITECTURAL MODELING REQUIREMENTS
- Shell roofs: multiple overlapping sail/shell forms with different sizes, orientations, and heights.
- Surface detail: tile panel lines or segmented ceramic pattern across shells.
- Podium: broad stepped base, promenade edges, stairs, and terrace levels.
- Facade: glass wall suggestions under shells, dark interior voids, entry areas, and structural rhythm.
- Harbor context: water plane with reflection, quay edge, boats or ferry scale markers, distant skyline, optional Harbour Bridge silhouette.
- Lighting: day/sunset toggle or animated light direction to show shell curvature.

#### INTERACTION AND INSPECTION
- Orbit/pan/zoom camera controls.
- Toggle shell tile lines, harbor reflection, city context, and annotation labels.
- Guided camera buttons: Harbor Icon View, Shell Closeup, Podium Walk, Skyline Context.
- Include a simple diagram overlay showing shell groups and orientation.

#### VISUAL AND MATERIAL QUALITY
- Shells should feel curved and layered, not flat triangles.
- Tile segmentation should enhance scale without becoming noisy.
- Water should support the silhouette and scene context.
- Avoid over-detailing the skyline at the expense of the Opera House.

#### DEPTH CHECKPOINTS
- The shell roof system must be recognizable from the opening view.
- Multiple shell groups, podium, glass walls, and harbor context must all be represented.
- Camera presets and toggles should make the roof geometry inspectable from different angles.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an equivalent browser 3D approach.
- Use parametric or approximated curved geometry for shells; if exact curves are too hard, explain the approximation in the final summary.
- Reuse shell materials and keep reflection effects performant.
- Verify scene rendering, controls, toggles, camera presets, and nonblank canvas.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what architectural features are modeled, what interactions work, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simplified, approximate, fragile, or worth rechecking.
- Cross-audit focus: Opera House recognizability, shell curvature, harbor context, inspection controls, and performance.
- Self-score from 1-5 for landmark accuracy, first-view impact, modeling detail, interaction depth, visual quality, and verification honesty.
```

</details>

<a id="prompt-37"></a>

<details>
<summary><strong>37. Antarctica - South Pole Research Station, Extreme-Climate Modular Architecture</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page.
- Use local geometry, procedural materials, and local state. Do not require paid assets, external 3D models, or large downloads.
- Make the result comparable across model runs: preserve the continent, extreme-climate architecture theme, core geometry, and inspection controls.
- Before finishing, verify that the 3D scene renders, the camera controls work, and the main architectural features are visible.
- In the final response, report only what matters for evaluation: what was built, how to open it, what can be inspected, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition browser-based 3D architectural model of an Antarctic research station inspired by real South Pole extreme-climate architecture, representing Antarctica in a global landmark modeling series.

This must not be a generic sci-fi base or a few boxes on snow. Antarctica has fewer public monumental buildings than other continents, so the test is to model iconic extreme-environment architecture: elevated modular buildings, support stilts, enclosed connectors, scientific equipment, snow management, wind, darkness/light, and survival infrastructure.

#### FIRST VIEW - ARCHITECTURE AGAINST EXTREME WEATHER
- Open with a low polar camera view showing an elevated research station above wind-scoured snow, modular wings, connector tunnels, antennas, fuel/storage modules, flags, and blowing snow.
- The first frame should communicate that architecture is responding to climate: elevation, wind, snow drift, logistics, and isolation.
- Include a compact overlay naming the continent, architectural theme, and modeled feature groups.

#### ARCHITECTURAL MODELING REQUIREMENTS
- Main station: long elevated modular building, insulated panels, small windows, service doors, and structural stilts.
- Connectors: enclosed passageways linking modules, stairs/ramps, and utility corridors.
- Climate systems: wind baffles, snowdrift berms, raised foundation logic, vents, exhaust, satellite dishes, antennas, and weather instruments.
- Support zone: fuel tanks, cargo containers, tracked vehicle, generator hut, storage sleds, and marked safe paths.
- Environment: snow terrain, wind streaks, low sun or polar twilight, aurora/night toggle, flags or poles showing wind direction.
- Human scale: small figures or markers, safety lights, and path ropes to show distance and harshness.

#### INTERACTION AND INSPECTION
- Orbit/pan/zoom camera controls.
- Toggle storm intensity, aurora/night mode, infrastructure labels, interior cutaway, and safe-path visibility.
- Guided camera buttons: Station Wide, Elevated Structure, Science Equipment, Logistics Yard, Storm Mode.
- Include annotations explaining why modules are elevated, how snow/wind affects layout, and what systems keep the station operating.

#### VISUAL AND MATERIAL QUALITY
- Snow should have shape, wind streaks, and shadow, not a flat white plane.
- Materials should distinguish insulated panels, metal supports, glass, lights, and equipment.
- Weather effects should create atmosphere without hiding the model.
- Avoid overly futuristic styling; keep it grounded, functional, and harsh.

#### DEPTH CHECKPOINTS
- The architecture must clearly respond to Antarctic conditions, not merely sit in a snowy scene.
- Elevated modules, connectors, scientific equipment, logistics zone, and weather effects must all be inspectable.
- Storm/night toggles should change the feeling and reveal infrastructure, not just tint the screen.

#### TECHNICAL REQUIREMENTS
- Use Three.js or an equivalent browser 3D approach.
- Use procedural geometry, particles or simple billboards for blowing snow, and reusable module components.
- Keep weather effects performant and avoid a blank white scene.
- Verify scene rendering, controls, toggles, camera presets, and nonblank canvas.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what architectural features are modeled, what interactions work, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simplified, approximate, fragile, or worth rechecking.
- Cross-audit focus: Antarctic architectural logic, modular detail, weather readability, inspection controls, and performance.
- Self-score from 1-5 for architectural accuracy, first-view impact, modeling detail, interaction depth, visual quality, and verification honesty.
```

</details>

<a id="prompt-02"></a>

<details>
<summary><strong>02. Founder Operating Room - One Screen To Run A Tiny Startup</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition web app called Founder Operating Room: one operational screen for a solo founder to run a tiny startup across customers, cash, product, launches, and risks.

This must not be a generic CRM, a decorative startup dashboard, or a pile of unrelated widgets. It should feel like the founder can open it in the morning and decide what to do next.

#### FIRST SCREEN - TODAY'S COMPANY, AT A GLANCE
- Open directly on the operating room, not a landing page.
- Show runway, revenue pipeline, product progress, launch checklist, customer conversations, and urgent risks in one coherent workspace.
- The first visible action should be operational: follow up with a customer, ship a feature, fix a blocker, or adjust runway.

#### CORE SYSTEMS
- Pipeline: leads, trials, active customers, expansion opportunities, churn risk.
- Cash: current balance, monthly burn, expected invoices, runway, and scenario toggle.
- Product: roadmap items, status, owner, user impact, and release confidence.
- Daily focus: automatically derive the top three actions from sample data.
- Decision log: record what the founder chose and why.

#### INTERACTION AND STATE
- Let the user update a deal stage, mark a product task shipped, log a customer note, and change a burn-rate scenario.
- The priority list should update when state changes.
- Include empty states, overdue states, and risk warnings.
- Desktop should feel like a command center; mobile should become a tight daily action view.

#### VISUAL AND UX QUALITY
- Use a calm operating-system feel, not venture-capital theater.
- Make dense information scannable through tables, compact cards, tabs, and clear hierarchy.
- Avoid oversized hero type, decorative gradients, and generic SaaS fluff.

#### DEPTH CHECKPOINTS
- The top-three action list must be derived from sample company data, not hard-coded as decorative text.
- Runway scenario changes should affect at least two visible values.
- At least one customer/product/risk item should be linked across panels.

#### TECHNICAL REQUIREMENTS
- Use local sample data and computed values.
- Build the full implementation with the existing stack if one exists.
- Verify at least one pipeline update, one scenario change, and one decision-log entry.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: completed requirements, known shortcuts, verification performed, and top three places another model should inspect.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-03"></a>

<details>
<summary><strong>03. Solo Consultant Command Center - Clients, Invoices, Scope And Next Actions</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition working app called Solo Consultant Command Center: a practical workspace for a one-person consultant managing clients, projects, invoices, scope changes, and next actions.

This must not be a generic project tracker or invoice mockup. It should expose the tension of consulting: billable work, scope creep, client responsiveness, unpaid invoices, and delivery commitments.

#### FIRST SCREEN - WHO NEEDS ATTENTION TODAY?
- Open on a prioritized client list with money at risk, next milestone, unpaid amount, response status, and scope health.
- Show one selected client with project timeline, open decisions, recent notes, invoice state, and next action.
- The first interaction should let the user resolve a practical issue: send reminder, mark invoice paid, log scope change, or move a milestone.

#### CORE SYSTEMS
- Client portfolio with at least six clients and varied risk states.
- Project scope tracker with original scope, added requests, estimate impact, and approval state.
- Invoice tracker with sent, viewed, overdue, partial, and paid states.
- Weekly capacity view showing booked hours, delivery load, and unallocated time.
- Next-action engine that derives priorities from deadlines, money, and blocked decisions.

#### INTERACTION AND STATE
- Update invoice status, add a scope-change request, move a milestone, and filter by risk.
- Show how one change affects client health or weekly capacity.
- Include empty, overdue, over-capacity, and all-clear states.

#### VISUAL AND UX QUALITY
- Professional, compact, and service-business specific.
- Avoid generic admin templates; every visible element should connect to consultant decision-making.
- Mobile should support quick client triage and invoice follow-up.

#### DEPTH CHECKPOINTS
- Scope creep must have a visible cost or capacity consequence.
- Invoice state changes should affect client priority or money-at-risk totals.
- At least one client should be healthy, one blocked, and one financially urgent.

#### TECHNICAL REQUIREMENTS
- Use local sample data and real derived status calculations.
- Keep it self-contained and interactive.
- Verify the primary client triage flow.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: what can be changed by the user, which values are computed, verification performed, and likely weak spots.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-04"></a>

<details>
<summary><strong>04. Family Logistics Console - The Week, The Fridge, The Budget And The Ride</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition mobile-first web app called Family Logistics Console: a shared weekly operations board for meals, groceries, school pickups, household tasks, budget pressure, and schedule conflicts.

This must not be a simple calendar, a todo list, or a recipe app. It should show how household decisions collide and help the family choose what to do next.

#### FIRST SCREEN - THE WEEK IS ALREADY IN MOTION
- Open on the current week with today's schedule, dinner plan, grocery gaps, budget warning, pickup conflicts, and top household tasks.
- The first screen should include at least one conflict that can be resolved.
- The first interaction should be concrete: swap dinner, assign pickup, mark pantry item used, or move a task.

#### CORE SYSTEMS
- Weekly calendar with family members, locations, conflicts, and shared commitments.
- Meal plan linked to pantry and grocery list.
- Budget meter for grocery and household spending.
- Chore/task board with ownership and overdue states.
- Conflict resolver that suggests realistic changes.

#### INTERACTION AND STATE
- Let the user assign a task, resolve a pickup conflict, update pantry quantity, and swap a meal.
- Updating meals should affect groceries and budget.
- Include states for conflict, missing ingredient, over budget, and quiet day.

#### VISUAL AND UX QUALITY
- Warm but practical; avoid childish styling or generic productivity layout.
- Use color to separate people, urgency, and categories without overwhelming the screen.
- Mobile must be excellent; desktop can show the full week and detail panel.

#### DEPTH CHECKPOINTS
- At least one meal decision must update pantry, grocery, and budget views.
- At least one scheduling conflict must show cause and resolution.
- Family members should have distinguishable responsibilities without relying only on color.

#### TECHNICAL REQUIREMENTS
- Build with local sample data and computed conflicts.
- No external APIs required.
- Verify at least one cross-system update, such as meal swap changing grocery needs.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: cross-system interactions implemented, responsive behavior, verification performed, and unresolved limitations.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-05"></a>

<details>
<summary><strong>05. Creator Launch Studio - From Idea Backlog To Scheduled Release</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition app called Creator Launch Studio: a workspace that turns a creator's rough content ideas into a scheduled multi-platform release plan.

This must not be a generic content calendar or social media dashboard. It should support the messy path from idea, angle, asset, draft, review, schedule, and postmortem.

#### FIRST SCREEN - WHAT CAN SHIP NEXT?
- Open on a launch board with idea backlog, active drafts, scheduled posts, asset gaps, and platform readiness.
- Show one selected idea expanded into hook, outline, assets needed, platforms, and launch checklist.
- The first action should move a piece of content closer to shipping.

#### CORE SYSTEMS
- Idea backlog with score for novelty, effort, audience fit, and urgency.
- Content pipeline with statuses from raw idea to scheduled.
- Platform adapters for YouTube, X, LinkedIn, newsletter, and short video.
- Asset checklist and blocker tracking.
- Lightweight postmortem area for results and learning.

#### INTERACTION AND STATE
- Let users promote an idea to draft, edit the hook, assign platforms, mark assets ready, and schedule a date.
- Filters by platform, status, and blocker.
- Readiness score should update from real state.

#### VISUAL AND UX QUALITY
- Creator-professional, not influencer glitter.
- Clear pipeline, compact cards, readable platform differences, and obvious blockers.
- Mobile should support idea capture and today's publishing tasks.

#### DEPTH CHECKPOINTS
- Readiness score must come from checklist/platform/asset state.
- At least one idea should move through multiple pipeline stages during interaction.
- Platform outputs should differ in real requirements, not just labels.

#### TECHNICAL REQUIREMENTS
- Use local sample content and real state updates.
- Do not require social platform APIs.
- Verify idea-to-scheduled flow.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: implemented workflow, state updates, verification performed, and what is simulated.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>

<a id="prompt-06"></a>

<details>
<summary><strong>06. Local Knowledge Garden - Notes That Turn Into Tasks And Briefs</strong></summary>

```text
#### MODEL TEST MODE
- Build the working result now; do not stop at a plan, explanation, or static mockup.
- Use the existing project stack when one exists; if the folder is blank, choose the simplest practical browser implementation.
- The first screen or first playable moment must prove the concept immediately. Do not create a marketing landing page unless the prompt explicitly asks for one.
- Use local sample data and local state when external services would otherwise be needed. Simulate AI/API behavior transparently and make it interactive.
- Make the result comparable across model runs: preserve the requested name, core workflow, and constraints instead of substituting an easier product.
- Before finishing, verify the main screen renders and the primary interaction works. If verification is blocked, say exactly what blocked it and what you checked instead.
- In the final response, report only what matters for evaluation: what was built, how to open it, what works, what was verified, known shortcuts, and remaining risk.

Create a maximum-ambition local-first web app called Local Knowledge Garden: a notes workspace where research notes, highlights, tasks, and briefs grow from the same material.

This must not be a generic notes app, markdown editor, or static knowledge graph. It should help a user find source material, connect it, and turn it into an actionable brief.

#### FIRST SCREEN - KNOWLEDGE READY TO USE
- Open on a workspace with recent notes, topic clusters, open questions, extracted tasks, and a draft brief.
- Show one selected topic with source notes, linked claims, evidence strength, and next actions.
- The first interaction should let the user connect notes, extract a task, or add a claim to the brief.

#### CORE SYSTEMS
- Notes with tags, source type, confidence, and linked topics.
- Search and filter by topic, source, confidence, and task status.
- Brief builder that collects claims with citations to local sample notes.
- Task extraction from notes with ownership and due dates.
- Knowledge graph or relationship view that is useful, not decorative.

#### INTERACTION AND STATE
- Add a note, link two notes, promote a highlight into a task, and add evidence to the brief.
- Show empty search, weak evidence, and unresolved question states.
- Updates should be reflected across note list, topic view, and brief.

#### VISUAL AND UX QUALITY
- Quiet, editorial, and tool-like.
- Avoid mystical garden visuals unless they directly clarify the knowledge structure.
- Desktop should support tri-pane work; mobile should support capture and review.

#### DEPTH CHECKPOINTS
- Claims in the brief should link back to source notes.
- Weak evidence and unresolved questions must be visually distinct.
- A note action should update both task/brief output and the topic view.

#### TECHNICAL REQUIREMENTS
- Use local data and state only.
- Do not require AI APIs; simulate extraction with clear local actions if needed.
- Verify note-to-brief and note-to-task flows.

#### FINAL OUTPUT INSTRUCTION
Build the full implementation now. When finished, summarize how to open it, what the reviewer can try, what you verified, known shortcuts, and remaining risks.

#### AUDIT PACKET
End with a compact audit packet containing:
- Requirements covered: 3-6 bullets tied to the prompt.
- Working interactions: what a reviewer can actually try.
- Verification performed: commands, preview, viewport checks, or manual flow checks.
- Known shortcuts and risks: what is simulated, incomplete, fragile, or worth rechecking.
- Cross-audit focus: working knowledge flows, simulated parts, verification performed, and likely edge cases.
- Self-score from 1-5 for completion, first-screen quality, interaction depth, visual/UX quality, engineering quality, and verification honesty.
```

</details>
