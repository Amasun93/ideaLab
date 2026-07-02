# 校情蓝皮书资料卡使用说明

Use this reference when the user asks about 校情蓝皮书、学校校情、小升初校情、科创校情、三公/特色校/名校的科创规划、特殊招生学校、科创特色学校名单、丘班/H8/L6/市北理/钱班/特色班、某城市或某学校的科创关注度、学校是否重视科创、以及适合怎样做 ideaLab 产品规划。

## Routing

Read in this order:

1. `README.md`
2. `城市校情/<城市>.md`
3. `学校资料卡/<城市>_<学校名>.md` when a specific school is named
4. `学校索引/` and `data/school_indices_20260702.json` when the user asks about special admission schools, district school lists, or science-innovation school lists
5. `班型资料卡/` and `data/school_indices_20260702.json` when the user asks about 丘班、H8、L6、市北理、钱班、特色班
6. `data/school_intelligence_20260702.json` when structured full-card fields are needed
7. `data/school_bluebook_sources_20260702.json` when source-batch confirmation is needed

## Answering Rules

- Distinguish 校情 from 区域赛事学情.
- Give the practical planning judgment first.
- Use school signals as internal planning indicators, not official claims.
- Distinguish full school cards from school index entries and class-track cards. Do not pretend an index row is a complete school profile.
- Ask for city, district, target school, current grade, child profile, goal and time budget when the planning question lacks context.
- Match product recommendations to the child's stage and school signal.
- Do not promise admission, better school outcome, award, direct admission, class placement, self-recruitment or comprehensive-evaluation result.
- Do not use bluebook table award counts as public official statistics.
- For parent-facing simulation, do not mention “知识库”, “当前口径” or source IDs. Say “目前资料看” or “这类学校通常更看重”.

## Default Output Shape

1. 先给判断：这座城市/这所学校是否值得重视科创，以及重视哪类科创。
2. 拆信号：学校属性、课程/班型、科创课程/社团/实验室、升学/考试材料信号。
3. 给规划：低龄、四五年级、初中分别怎么走。
4. 匹配产品：智造万物/MYO、启航、雏鹰杯专项营、寒(暑)假竞赛营、领航等。
5. 补边界：以当年官方通知为准，不承诺录取、获奖或升学结果。
