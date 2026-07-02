# 校情蓝皮书知识库

本目录沉淀 `2026-07-02` 批次的斯坦星球科创蓝皮书清洗结果，用于回答城市校情、单校科创信号、小升初规划和产品适配问题。

## 使用边界

- 这是内部校情规划资料，不是学校官方招生简章。
- 不包含原始 PDF、完整抽取文本、学生名单、证书、个人案例或学籍信息。
- 不承诺录取、优录、自招、综评、分班、直升或获奖结果。
- 学校属性、招生方式、班型设置、测评方式、赛事规则和当年节点均需以教育局、学校或赛事官方最新通知复核。
- 对家长表达时，应说“从目前资料看，这类学校更重视……”，不要说“这所学校一定看……”“报了就有用”。

## 校情与学情的区别

- `校情`：围绕城市和学校，回答学校属性、课程/班型、科创信号、升学/考试信号、产品适配和顾问追问。
- `区域赛事学情`：围绕区级赛事通知，回答年份、区、赛事、申报窗口、入口、学校推荐机制、材料限制和评审节点。

用户问“浦东雏鹰杯什么时候申报”时，走区域赛事学情；用户问“上海三公/深圳深中/无锡大桥怎么看科创规划”时，走本目录。

## 字段设计

城市卡字段：

- `bluebook_focus`：该城市蓝皮书的核心主题。
- `planning_summary`：城市层面的规划判断。
- `school_selection_signals`：择校/升学材料相关信号。
- `recommended_events`：可衔接的赛事或成果方向。
- `product_implications`：对应 ideaLab 产品规划意义。
- `known_limitations`：当前资料缺口和使用限制。

单校卡字段：

- `city`
- `school_name`
- `source_section`
- `school_type_or_attribute`
- `recommendation_index`
- `tags`
- `school_positioning`
- `course_or_class_features`
- `science_innovation_signal`
- `admission_or_exam_signal`
- `competition_or_portfolio_signals`
- `product_fit`
- `consultant_questions`
- `parent_planning_note`
- `privacy_level`
- `confidence`

## 读取顺序

1. 先读本文件，明确边界。
2. 按城市读取 `城市校情/<城市>.md`。
3. 如果用户问到具体学校，再读 `学校资料卡/<城市>_<学校名>.md`。
4. 需要结构化检索时读取 `data/school_intelligence_20260702.json`。
5. 需要确认来源批次时读取 `data/school_bluebook_sources_20260702.json`。

## 后续清洗流程

处理新版校情 PDF 时，优先使用 MinerU 做版式提取，尽量保留章节、表格和层级结构；再人工/AI 清洗成城市卡、学校资料卡和结构化 JSON。发布包只保留脱敏后的结构化摘要，不放原始 PDF、完整抽取文本或学生/案例明细。

## 当前覆盖

- 城市卡：上海、南京、无锡、杭州、深圳。
- 单校卡：上海 3 所、无锡 8 所、深圳 5 所。
- 南京、杭州当前批次以城市级判断为主，未形成稳定单校卡。
