# Production-Ready Product Development Skill

[English](README.md) | 简体中文

这是一个面向 Codex 和其他 Agent 工作流的产品工程 Skill，用来把 demo、原型、PRD、早期功能想法和已有代码库，整理成可上线、可测试、可维护的产品开发方案。

它的目标不是让 AI 只做出“能跑一次”的 demo，而是帮助 AI 按真实产品标准检查产品流程、发布等级、风险等级、用户角色、权限、页面状态、数据模型、API 契约、安全、测试、部署、运维和验收标准。

## 这个 Skill 能做什么

- 先识别产品类型，再应用对应的专项检查清单。
- 将目标发布等级划分为 Demo、MVP、Beta 或 Production。
- 将风险等级划分为 Low、Medium、High 或 Critical。
- 对小型低风险改动启用 Lightweight Mode。
- 对真实用户、高风险、上线前或长期维护项目启用 Full Production Review。
- 生成可以直接交给 Codex 或其他编码 Agent 执行的实施提示词。
- 生成适合产品、测试和交付验收使用的 checklist。

## 仓库结构

```text
production-ready-product-development/
|-- README.md
|-- README.zh-CN.md
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
`-- references/
    |-- acceptance-checklists.md
    |-- ai-product-evaluation-loop.md
    |-- analysis-modes.md
    |-- output-format.md
    |-- product-type-checklists.md
    `-- universal-production-checklist.md
```

## 什么时候使用

当你想做下面这些事情时，可以使用这个 skill：

- 把 vibe-coded demo 变成真实产品方案。
- 检查 MVP 是否已经达到 Beta 或 Production 标准。
- 梳理上线前还缺哪些能力。
- 把 PRD 或原型转成可执行的开发任务。
- 评估后台系统、SaaS、数据大屏、小程序、AI 工具或数据系统。
- 为另一个编码 Agent 生成生产级实施提示词。

## 示例提示词

```text
Use $production-ready-product-development to review whether this mini program is ready for real users.
```

```text
Use $production-ready-product-development to turn this admin dashboard prototype into a beta-ready development plan.
```

```text
Use $production-ready-product-development to assess whether this AI QA system can go online safely.
```

## 说明

这个 skill 故意拆成了一个较短的 `SKILL.md` 和多个聚焦的 reference 文件。主文件负责触发、分流和工作流程，详细检查清单只在需要时加载，这样更符合 Codex Skills 的渐进式上下文加载方式。
