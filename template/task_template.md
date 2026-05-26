# Agent Task Template

## 0. Task Header

| Field | Value |
| --- | --- |
| Task ID | `T-000` |
| Task Name | `<简短任务名>` |
| Owner Agent | `<agent-name>` |
| Status | `todo / doing / blocked / review / done` |
| Priority | `P0 / P1 / P2` |
| Created At | `YYYY-MM-DD` |
| Updated At | `YYYY-MM-DD` |
| Depends On | `T-xxx, T-yyy` |
| Blocks | `T-zzz` |

## 1. Goal

一句话说明这个任务要交付什么。

```text
完成 <模块/能力>，使系统能够 <用户可观察的结果>。
```

## 2. Source Context

只放完成任务必需的上下文，不复制整份 design doc。

- Design Doc: `<path/to/design-doc.md>`
- Relevant Sections:
  - `<section title / anchor>`
  - `<section title / anchor>`
- Related Files:
  - `<path/to/file>`
  - `<path/to/file>`
- Related Tasks:
  - `T-xxx: <关系说明>`

## 3. Scope

### In Scope

- `<必须实现的功能点 1>`
- `<必须实现的功能点 2>`
- `<必须修改/新增的文件或模块>`

### Out of Scope

- `<明确不做的事情 1>`
- `<容易误做但本任务不负责的事情 2>`

## 4. Contract

定义这个任务和其他任务之间的稳定边界。subagent 必须优先保证 contract，而不是自由发挥。

### Inputs

| Name | Type | Source | Notes |
| --- | --- | --- | --- |
| `<input>` | `<type>` | `<caller/file/api>` | `<约束>` |

### Outputs

| Name | Type | Consumer | Notes |
| --- | --- | --- | --- |
| `<output>` | `<type>` | `<caller/file/api>` | `<约束>` |

### Public Interfaces

```ts
// 若有 API、函数、事件、schema、CLI 参数，在这里写稳定签名
```

### Data / State Changes

- `<新增/修改的数据结构、状态字段、配置项>`
- `<迁移、兼容性或默认值要求>`

## 5. Harness

这里定义 agent 开发和验证时必须使用的“工程护栏”。

### Execution Commands

```bash
# install/build/test/lint/dev 等，只保留本任务相关命令
<command>
```

### Test Harness

- Unit Tests: `<需要新增/更新哪些测试>`
- Integration Tests: `<需要覆盖哪些跨模块路径>`
- Manual Checks: `<必要的手工验证步骤>`
- Fixtures / Mocks: `<测试数据、mock、stub 的位置和约束>`

### Observability
