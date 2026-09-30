# ideaLab Knowledge 知识地图

> 版本：2026-09-30。图中 `S21` 是本次新增的钉钉销售 SOP 清洗批次；它已经接入工作台只读索引，但高风险事实仍需回查当期原文。

```mermaid
flowchart LR
  K["ideaLab Knowledge\n知识库"]

  subgraph SRC["来源层：材料从哪里来"]
    D["钉钉文档与关联材料\nSOP / PPT / PDF / DOCX / XLSX / HTML"]
    O["官方赛事与区域通知\n赛事规则 / 时间节点 / 申报入口"]
    U["已确认的用户口径\n产品体系 / 费用拆分 / 方案更新"]
    A["历史案例与素材索引\n课程资料 / 图片 / 视频 / 附件"]
  end

  subgraph DOM["知识域：整理后回答什么"]
    P["产品与课程\n启航 · 领航 · 智造万物\nMYO · 竞赛营 · 专项营"]
    E["赛事与赛情\n青创赛 · 雏鹰杯 · 宋庆龄\nLab赛事包 · 区域赛情"]
    S["学校与区域校情\n城市校情 · 学校资料卡\n学校索引与获奖数据"]
    C["顾问训练与销售\nFAQ · 规划逻辑 · 回复剧本\n内部培训方法"]
    M["多媒体与附件\n图片 · 视频 · PPT · Logo\n可外发边界"]
    CI["竞品与规划案例\n竞品卡片 · 历史规划案例"]
    G["治理与来源追踪\nsource registry · 更新策略\n待确认队列 · 字段规范"]
  end

  subgraph S21["S21：本次新增的 8 条清洗知识"]
    S21A["SOP总览与材料索引"]
    S21B["产品到宣传物料映射"]
    S21C["启航 / 领航 / 竞赛营续费方法"]
    S21D["合同条款与退费边界"]
    S21E["内部激励政策与奖金榜单"]
    S21F["竞赛营与专项营占座材料"]
    S21G["竞品与外部文章索引"]
    S21H["知识使用边界与回查规则"]
  end

  subgraph OUT["使用层：知识如何被使用"]
    X["小芮 / ideaLab Skill\n回答、规划、顾问培训"]
    W["工作台材料知识库\n检索、来源、风险、文件链接"]
    L["钉钉原文链接\n需具备对应访问权限"]
    F["本地归档文件\nPDF / DOCX / XLSX / 图片 / 页面快照"]
  end

  D --> K
  O --> K
  U --> K
  A --> K
  K --> DOM
  K --> S21
  P --> X
  E --> X
  S --> X
  C --> X
  M --> X
  CI --> X
  G --> X
  G --> W
  S21 --> C
  S21 --> M
  S21 --> W
  S21A --> L
  S21B --> F
  S21C --> L
  W --> F
  W --> L

  classDef root fill:#16324f,stroke:#0b1f33,color:#fff,stroke-width:2px;
  classDef domain fill:#e8f1fb,stroke:#4f81bd,color:#17324d;
  classDef source fill:#f5f5f5,stroke:#8a8a8a,color:#333;
  classDef batch fill:#fff1dc,stroke:#e08a36,color:#6b3a00;
  classDef output fill:#e8f7ef,stroke:#4b9b6a,color:#164a2b;
  class K root;
  class P,E,S,C,M,CI domain;
  class D,O,U,A source;
  class S21A,S21B,S21C,S21D,S21E,S21F,S21G,S21H batch;
  class X,W,L,F output;
```

## 读图要点

| 层 | 作用 | 当前代表内容 |
|---|---|---|
| 来源层 | 保留材料出处和证据形态 | 钉钉 SOP、赛事通知、用户确认口径、课程与素材原件 |
| 知识域 | 把原材料整理成可检索的主题 | 产品课程、赛事赛情、校情、顾问训练、素材、竞品与案例 |
| S21 批次 | 补齐近期销售 SOP 的方法和材料入口 | 产品物料、续费逻辑、合同/奖金/占座/竞品边界 |
| 使用层 | 让人或系统调用知识 | 小芮回答、工作台检索、钉钉原文链接、本地文件链接 |

## 风险颜色和使用边界

- 蓝色：稳定的知识域入口，可以作为检索和回答的主题。
- 橙色：S21 新增内容。它包含“8 月在售”等历史时间口径，不能直接当成当前价格或政策。
- 灰色：原始来源，回答时应保留来源和核验时间。
- 绿色：使用出口。文件链接可以提供，但钉钉链接受权限控制，本地文件不应直接发给外部家长。
- 合同、退费、奖金、占座、当月在售和竞品判断，都必须回查当期 SOP、正式合同或官方来源。
