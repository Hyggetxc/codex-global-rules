# Global Rules (Persistent)

适用范围：当前账号下的所有 Codex 项目
最后更新：2026-03-06

## 默认协作规则
- 默认使用中文沟通；代码标识、变量名、API、库名保持原样。
- 涉及代码时，优先补充必要注释，帮助理解逻辑与用途。
- 不管是什么项目，优先使用 `Get Shit Done (GSD)` 方法推进需求。
- 计划、执行、复盘尽量按 GSD 结构输出，并提供中文版说明。
- 面向非技术背景说明时，默认按以下结构输出：目标、操作、预期结果、风险与回退。
- 如项目目录内存在更具体的 `AGENTS.md`，项目规则优先；未覆盖部分继续沿用本文件。

## 安全与确认机制
- 对任何可能影响安全或数据的操作，必须先说明将执行的动作与风险，再等待你明确同意。
- 未收到“确认执行”或同等明确授权前，不执行高风险步骤。
- 以下场景必须先确认：删除或清理文件、批量移动、覆盖写入、系统级修改、修改权限或安全策略、联网下载或安装、上传数据、调用外部服务、其他不可逆操作。
- 涉及系统盘、用户目录或大范围文件操作时，默认视为高风险。

## 技能触发与使用规则
- 当用户用 `$SkillName` 或技能名点名某个技能时，必须优先使用该技能。
- 当任务与某个技能的职责明显匹配时，即使用户没有点名，也应优先使用对应技能。
- 使用技能前，先检查对应 `SKILL.md` 是否存在。检查顺序如下：
  1. `<当前项目>\.codex\skills\<skill-name>\SKILL.md`
  2. `C:\Users\tanxi\.codex\skills\<skill-name>\SKILL.md`
  3. `C:\Users\tanxi\.codex\skills\.system\<skill-name>\SKILL.md`
- 如果技能缺失、路径不可读或指令不完整，要简要说明问题，并继续采用最佳可行回退方案。
- 多个技能同时适用时，只选择覆盖任务所需的最小技能集合，并说明使用顺序。
- 读技能时遵循渐进展开：先读 `SKILL.md`，只在必要时再读其引用的脚本、模板、素材或参考文件。
- 技能文件中的相对路径，优先相对技能目录解析。
- 如果技能目录下存在 `scripts/`、`assets/`、模板或现成工作流，优先复用，不要无意义重写。
- 当任务是创建或更新技能时，优先使用 `skill-creator`；当任务是安装技能时，优先使用 `skill-installer`。

## 默认技能优先级
- UI/UX 相关任务，优先使用 `ui-ux-pro-max`。
- 产品相关任务（需求分析、PRD、路线图、用户研究、优先级、增长等），优先使用产品经理技能。
- 办公文档任务（`docx`、`xlsx`、`pptx`、`pdf`），优先使用官方文档技能。
- 测试、CI、部署、监控、安全相关任务，优先使用工程交付技能。
- 技能创建、整理、封装、发布相关任务，优先使用 `skill-creator` 与 `skill-authoring-workflow`。

## 技能来源与更新元信息
- `ui-ux-pro-max`
  - 来源：`https://github.com/nextlevelbuilder/ui-ux-pro-max-skill`
  - 当前检测：项目级安装，已在 `C:\Users\tanxi\Documents\New project\.codex\skills\ui-ux-pro-max\SKILL.md` 发现
  - 更新方式：`npx --yes uipro-cli init --ai codex`
  - 最后验证：`2026-03-06`
- `Product-Manager-Skills`
  - 来源：`https://github.com/deanpeters/Product-Manager-Skills`
  - 当前检测：用户级 `C:\Users\tanxi\.codex\skills` 未发现对应业务技能；默认按项目级技能目录优先检查，缺失时走回退方案
  - 更新方式：从上游仓库同步并按需安装到项目级或用户级技能目录
  - 最后验证：`2026-03-06`
- 文档四件套 `docx`、`xlsx`、`pptx`、`pdf`
  - 来源：`https://github.com/anthropics/skills`
  - 当前检测：当前用户级技能目录未检测到安装；如项目级存在则按项目级优先
  - 更新方式：从官方仓库同步对应技能并安装到目标技能目录
  - 最后验证：`2026-03-06`
- 工程交付技能 `playwright`、`gh-fix-ci`、`sentry`、`vercel-deploy`、`render-deploy`、`cloudflare-deploy`、`security-best-practices`、`security-threat-model`
  - 来源：`https://github.com/openai/skills`
  - 当前检测：当前用户级技能目录未检测到安装；如项目级存在则按项目级优先
  - 更新方式：从上游仓库同步对应技能并安装到目标技能目录
  - 最后验证：`2026-03-06`
- 系统技能 `skill-creator`、`skill-installer`
  - 来源：Codex 系统技能目录
  - 当前检测：已在 `C:\Users\tanxi\.codex\skills\.system` 发现
  - 更新方式：随 Codex 系统技能更新；使用前仍按路径检查 `SKILL.md`
  - 最后验证：`2026-03-06`

## 默认候选技能清单
- UI/UX：`ui-ux-pro-max`
- 产品策略与研究：`acquisition-channel-advisor`、`ai-shaped-readiness-advisor`、`altitude-horizon-framework`、`business-health-diagnostic`、`company-research`、`context-engineering-advisor`、`customer-journey-map`、`customer-journey-mapping-workshop`、`director-readiness-advisor`、`discovery-interview-prep`、`discovery-process`、`eol-message`、`feature-investment-advisor`、`finance-based-pricing-advisor`、`finance-metrics-quickref`、`jobs-to-be-done`、`lean-ux-canvas`、`opportunity-solution-tree`、`pestel-analysis`、`pol-probe`、`pol-probe-advisor`、`positioning-statement`、`positioning-workshop`、`press-release`、`prioritization-advisor`、`problem-framing-canvas`、`problem-statement`、`product-strategy-session`、`proto-persona`、`recommendation-canvas`、`roadmap-planning`、`saas-economics-efficiency-metrics`、`saas-revenue-growth-metrics`、`storyboard`、`tam-sam-som-calculator`、`workshop-facilitation`
- 需求定义与交付：`prd-development`、`user-story`、`user-story-mapping`、`user-story-mapping-workshop`、`user-story-splitting`、`epic-hypothesis`、`epic-breakdown-advisor`
- 组织与职业发展：`executive-onboarding-playbook`、`director-readiness-advisor`、`vp-cpo-readiness-advisor`
- 办公文档：`docx`、`xlsx`、`pptx`、`pdf`
- 工程交付：`playwright`、`gh-fix-ci`、`sentry`、`vercel-deploy`、`render-deploy`、`cloudflare-deploy`、`security-best-practices`、`security-threat-model`
- 技能构建：`skill-authoring-workflow`
- 系统技能：`skill-creator`、`skill-installer`

## 重复功能的默认主用规则
- `customer-journey-mapping-workshop` -> `customer-journey-map`：先工作坊式引导，再产出标准旅程图。
- `positioning-workshop` -> `positioning-statement`：先澄清定位要素，再沉淀一句话定位陈述。
- `user-story-mapping-workshop` -> `user-story-mapping`：先互动梳理流程，再形成结构化故事地图。
- `pol-probe-advisor` -> `pol-probe`：先选验证方法，再定义具体 Proof of Life 探针。
- `discovery-process` -> `discovery-interview-prep`：整体发现流程优先；需要访谈细节时再调用访谈准备。
- `user-story-splitting` -> `epic-breakdown-advisor`：默认先做通用拆分；当明确使用 Humanizing Work 方法时切到 `epic-breakdown-advisor`。
- `saas-revenue-growth-metrics` / `saas-economics-efficiency-metrics` -> `finance-metrics-quickref`：两个专项指标技能用于深挖；`finance-metrics-quickref` 作为快速查表入口。
- `director-readiness-advisor` / `vp-cpo-readiness-advisor` -> `executive-onboarding-playbook`：晋升评估用前两者；已入职后的 30-60-90 落地优先用 onboarding playbook。
- `skill-creator` -> `skill-authoring-workflow`：前者用于方法与规范；后者用于把素材落地成可发布 skill。

## 默认任务路由
- 产品策略与路线图：`product-strategy-session`、`roadmap-planning`、`prioritization-advisor`
- 需求定义与 PRD：`problem-framing-canvas`、`problem-statement`、`prd-development`
- 用户研究与增长：`discovery-process`、`jobs-to-be-done`、`acquisition-channel-advisor`
- 需求拆分与交付：`user-story`、`user-story-splitting`、`epic-hypothesis`
- UI 设计：`ui-ux-pro-max`
- 办公文档：`docx`、`xlsx`、`pptx`、`pdf`
- 工程交付：`playwright`、`gh-fix-ci`、`vercel-deploy`、`render-deploy`、`cloudflare-deploy`、`sentry`、`security-best-practices`、`security-threat-model`
- 技能创建与安装：`skill-creator`、`skill-installer`、`skill-authoring-workflow`

## 维护规则
- 这份文件是默认全局规则，应该保持自包含，不依赖项目级 `AGENTS.md` 才能理解核心协作方式。
- 新增技能时，必须同时补充适用场景、与现有技能的关系（主用、备选、替代）、来源、安装位置、更新方式、最后验证日期，以及默认触发优先级。
- 当技能版本、命名或结构发生变化时，优先更新本文件，避免全局规则与实际技能库脱节。
