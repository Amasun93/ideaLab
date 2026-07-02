# ideaLab 关键字段规范

更新时间：2026-07-02

## 使用原则

当前不做全量结构化重构。新增字段采用“轻量追加”方式，优先补在 JSON 数据和新资料卡模板中；旧 Markdown 不强制立刻全部迁移。

`SKILL.md` 只保存路由和硬边界，事实字段应写入资料卡或结构化数据。

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

## 最小必填字段

新增资料卡至少补齐以下字段：

| 字段 | 含义 |
|---|---|
| `source_ids` / `source_batch` | 来源 ID 或材料批次 |
| `public_safe` | 是否适合对外表达 |
| `risk_level` | 风险等级 |
| `last_verified` | 最近核验日期 |
| `confidence` | 置信度或证据强度 |
| `use_boundary` | 使用边界 |

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

建议追加字段：

| 字段 | 含义 |
|---|---|
| `standard_name` | 对外标准名称 |
| `active_status` | 在售/暂停/历史/待确认 |
| `target_grade_stage` | 适用年级或学段 |
| `entry_requirements` | 入门测、身份、年级、国籍等报名门槛 |
| `delivery_boundary` | 交付物边界 |
| `refund_boundary` | 退费边界 |
| `adjacent_products` | 相邻产品及区别 |
| `asset_ids` | 可用图片或附件 ID |

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

建议追加字段：

| 字段 | 含义 |
|---|---|
| `current_year_status` | 当年赛事状态 |
| `timeline_year` | 时间线对应年份 |
| `application_entry` | 报名或申报入口 |
| `materials_required` | 材料要求 |
| `review_stages` | 初评/复评/终评/答辩等阶段 |
| `source_confidence` | 来源置信度 |
| `public_quote_ready` | 是否可直接作为公开引用 |
| `forbidden_claims` | 禁用表达 |

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

## 区域赛事赛情建议字段

适用于 `event_knowledge/区域赛事赛情/` 和 `regional_event_intelligence_*.json`。

| 字段 | 含义 |
|---|---|
| `district` | 区 |
| `years_covered` | 覆盖年份 |
| `primary_events` | 主要赛事 |
| `application_windows` | 申报窗口 |
| `entry_path` | 学校推荐/个人申报/区级入口 |
| `school_recommendation_mechanism` | 学校推荐机制 |
| `material_limits` | 材料限制 |
| `competition_intensity` | 竞争强度 |
| `key_school_attributes` | 重点关注学校属性 |
| `confirmed_vs_inferred` | 已确认信息和推断信息 |
| `needs_followup` | 待补事项 |

## 学校资料卡建议字段

适用于 `school_knowledge/学校资料卡/` 和 `school_intelligence_*.json`。

| 字段 | 含义 |
|---|---|
| `city` | 城市 |
| `district` | 区 |
| `school_name` | 学校名称 |
| `school_stage` | 小学/初中/高中/一贯制/待复核 |
| `school_nature` | 公办/民办/国际/待复核 |
| `school_tier_label` | 内部参考标签，不对外包装成官方排名 |
| `science_innovation_strength` | 科创信号强/中/弱 |
| `science_innovation_evidence` | 科创证据 |
| `competition_signals` | 赛事或材料信号 |
| `admission_or_selection_signals` | 招生/筛选/升学信号 |
| `best_product_fit_by_stage` | 分阶段产品适配 |
| `consultant_questions` | 顾问追问 |
| `verification_needed` | 待复核事项 |

学校索引中的 `bluebook_40th_qingchuang_award_count` 对外展示名为 `第40届青创赛获奖数`。该字段来源于官方获奖数据，可用于判断学校在第40届青创赛中的科创活跃度和成果表现，不得泛化为学校综合排名或长期趋势。

## 图片与附件 manifest 建议字段

| 字段 | 含义 |
|---|---|
| `asset_id` | 附件唯一 ID |
| `path` | 相对路径 |
| `asset_type` | official_logo / poster / screenshot / reference_image / internal_attachment |
| `source_id` | 来源 ID |
| `can_send_to_user` | 是否可发送给用户 |
| `usage_context` | 使用场景 |
| `rights_note` | 授权或来源说明 |
| `risk_level` | 风险等级 |
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
