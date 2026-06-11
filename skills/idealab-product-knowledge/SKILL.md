---
name: idealab-product-knowledge
description: Use when answering or producing content about ideaLab/斯坦星球 course products, Lab赛事包, 青创赛, 雏鹰杯, 宋庆龄少年儿童发明奖, course recommendations, sales positioning, official event data, parent-facing explanations, consultant scripts, award/result claims, refund boundaries, or competition-service guardrails.
---

# ideaLab Product Knowledge

Use this skill to answer with the local knowledge base, not memory or guesswork. Treat the bundled references as the source of truth for product structure, recommendation logic, official event data, and expression guardrails.

## First Decision

Classify the task before reading details:

- Product explanation: read `references/product_knowledge/产品总览.md` and `references/product_knowledge/产品关系图.md`.
- Product recommendation: also read `references/product_knowledge/推荐逻辑.md` and `references/product_knowledge/data/recommendation_rules.json`.
- Specific product: read the relevant file in `references/product_knowledge/产品卡片/`.
- Price, hours, contract, refund, promise, or sales risk: read `references/product_knowledge/销售与合同边界.md` and `references/product_knowledge/口径冲突与待确认.md`.
- Lab赛事包 or competition content: read `references/event_knowledge/README.md`, `references/event_knowledge/三赛联动_Lab赛事包/02_Lab赛事包叙事卡.md`, and the relevant event folder.
- Official figures or citation-backed copy: read `references/event_knowledge/data/data_points.json`, `references/event_knowledge/data/source_registry.json`, and `references/event_knowledge/data/claim_bank.json`.
- Visual or logo use: read `references/event_knowledge/data/visual_manifest.json`; only `asset_type=official_logo` can be treated as an official logo.
- Broader preparation, examples, parent FAQ, or product-to-event mapping: read `references/event_knowledge/90_长期素材预备/README.md`.

## Core Product Logic

Explain ideaLab as a pathway:

1. 基础兴趣与动手能力：智造万物、MYO系列。
2. 长期原创能力：科创启航计划。
3. 深度科研与综评：科创领航计划、高中课题营。
4. 赛事申报与专项备赛：竞赛集训营、未来工程师专项营、雏鹰杯专项营、科创发明营。

When recommending, state why the selected product fits and why nearby alternatives are less suitable.

## Core Event Logic

Explain Lab赛事包 as a three-event matrix, not a single-event guarantee:

> Lab赛事包不是押单场，而是通过青创赛、雏鹰杯、宋庆龄少年儿童发明奖三赛联动，把学生上岸机会变成一套可管理、可交付的系统。

Use the events this way:

- 青创赛: project research, originality, inquiry/defense, comprehensive innovation literacy.
- 雏鹰杯: large participation, layered selection, research process and student expression, 小院士 path.
- 宋庆龄少年儿童发明奖: national invention context, AI/programming, creative works, finalist and final defense.

## Answer Shape

For parent-facing or consultant-facing answers:

1. Start with the practical judgment.
2. Explain the product or event position.
3. Give the matched student profile and deliverables.
4. Use official/public data only when it helps the point.
5. Add a short boundary note for prices, contracts, refunds, awards, or privacy.

For internal planning:

1. Separate public claims from internal claims.
2. Mark source IDs when using numbers.
3. Identify missing authorization, stale dates, or conflicting price/hour terms.

## Guardrails

- Do not say 保奖, 保证获奖, or 100%拿奖.
- Do not turn refund commitments into result guarantees.
- Do not state `92%+` as official competition data.
- Do not expose lowest-score removal, teacher-level result comparisons, or internal calculation details.
- Do not compute a public combined probability across 青创赛、雏鹰杯、宋庆龄少年儿童发明奖.
- Do not quote internal-only material directly to parents.
- Do not publish student photos, certificates, names, schools, or case media without authorization.
- If price, hours, contract, or refund terms conflict, say the knowledge base has conflicting versions and defer to the latest signed contract or sales SOP.

## Key Reference Map

- Product overview: `references/product_knowledge/产品总览.md`
- Product cards: `references/product_knowledge/产品卡片/`
- Product data: `references/product_knowledge/data/`
- Event overview: `references/event_knowledge/README.md`
- Three-event story: `references/event_knowledge/三赛联动_Lab赛事包/`
- Event data: `references/event_knowledge/data/`
- Long-term event prep: `references/event_knowledge/90_长期素材预备/`
- Official attachments: `references/event_knowledge/source_attachments/`
