# ideaLab 关键字段规范

更新时间：2026-06-29

## 使用原则

当前不做全量结构化重构。新增字段采用“轻量追加”方式，优先补在 JSON 数据和新资料卡模板中；旧 Markdown 不强制立刻全部迁移。

字段分两类：

1. 业务事实字段：方便小芮稳定回答。
2. 治理字段：方便判断是否可外发、是否过期、是否需要核验。

## 通用治理字段

| 字段 | 含义 | 示例 |
|---|---|---|
| `status` | 当前状态 | active / paused / deprecated / draft |
| `public_safe` | 是否适合对外表达 | true / false / conditional |
| `risk_level` | 口径风险等级 | low / medium / high |
| `source_ids` | 对应来源 ID | ["S01"] |
| `last_verified` | 最近核验日期 | 2026-06-29 |
| `next_review` | 建议下次复核日期 | 2026-09-01 |
| `owner` | 业务负责人或默认归口 | 大卫 / 教研 / 销售SOP / 赛事负责人 |
| `update_policy` | 更新策略 | auto_low_risk / pending_review / manual_only |
| `notes` | 补充说明 | 以当期 SOP 为准 |

## 产品数据建议字段

适用于 `product_knowledge/data/products.json` 及后续产品卡片。

| 字段 | 含义 |
|---|---|
| `id` | 产品唯一 ID |
| `name` | 当前标准名称 |
| `aliases` | 旧称、俗称、群内常用称呼 |
| `type` | regular_course / competition_service / project_camp / brand |
| `category` | 产品类别 |
| `status` | active / paused / deprecated |
| `positioning` | 一句话定位 |
| `target_students` | 适合学生 |
| `pricing` | 价格口径，必要时写“以 SOP 为准” |
| `course_hours` | 课时口径 |
| `contract_type` | 合同类型 |
| `core_outputs` | 交付物 |
| `best_for` | 适合场景 |
| `not_for` | 不适合场景 |
| `sales_risk_level` | 销售风险等级 |
| `public_safe` | 是否适合对外直接表达 |
| `source_ids` | 来源 ID |
| `last_verified` | 最近核验日期 |
| `next_review` | 下次复核日期 |
| `update_policy` | 更新策略 |

## 赛事数据建议字段

适用于 `event_knowledge/data/events.json` 及后续赛事资料卡。

| 字段 | 含义 |
|---|---|
| `id` | 赛事唯一 ID |
| `name` | 官方/标准名称 |
| `short_name` | 简称 |
| `aliases` | 俗称或常见简称 |
| `event_tier` | core / supplemental / historical |
| `business_role` | research_validation / creative_incubation / competition_service 等 |
| `lab_package_role` | core_event / supplemental_event / not_included |
| `positioning` | 赛事定位 |
| `agent_summary` | 小芮内部摘要 |
| `audience` | 参赛对象 |
| `evaluation` | 评审方式 |
| `product_mapping` | 可关联产品 |
| `public_safe` | 是否可公开表达 |
| `risk_level` | 表达风险等级 |
| `source_ids` | 来源 ID |
| `last_verified` | 最近核验日期 |
| `next_review` | 下次复核日期 |
| `update_policy` | 更新策略 |

## 话术/Claim 建议字段

适用于 `claim_bank.json`、口播句、FAQ。

| 字段 | 含义 |
|---|---|
| `id` | 话术唯一 ID |
| `scope` | 适用范围 |
| `claim` | 具体表达 |
| `use_context` | 使用场景 |
| `public_safe` | 是否可外发 |
| `risk_level` | 风险等级 |
| `source_ids` | 来源 ID |
| `rewrite_guardrail` | 改写边界 |
| `forbidden_rewrites` | 禁止改写方向 |
| `last_verified` | 最近核验日期 |

## 更新策略定义

| 策略 | 含义 |
|---|---|
| `auto_low_risk` | 低风险内容可自动更新，如错别字、别名、表达优化 |
| `pending_review` | 可记录待核验，不直接作为正式口径 |
| `manual_only` | 必须由正式 SOP、合同、官方通知或大卫老师确认后更新 |

## 推荐默认值

- 产品价格、退费、合同：`update_policy = manual_only`，`risk_level = high`
- 产品定位、适合人群：`update_policy = pending_review`，`risk_level = medium`
- 错别字、别名、格式：`update_policy = auto_low_risk`，`risk_level = low`
- 赛事时间节点：`update_policy = pending_review`，当年节点建议 `risk_level = medium/high`
- 官方公开来源：可新增来源，但仍需标注 `source_confidence`
