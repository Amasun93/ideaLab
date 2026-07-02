# 资料卡轻量模板

更新时间：2026-07-02

## 使用原则

新增资料卡时优先补齐关键字段，但不要求旧资料一次性全部重构。字段用于帮助小芮判断：能不能对外说、有没有来源、是否需要复核、是否属于高风险口径。

`SKILL.md` 只保存路由。新事实、新话术、新价格、新校情、新赛情应写入资料卡或数据文件。

---

## 产品资料卡模板

```markdown
# 产品名：资料卡

## 元信息

|字段|内容|
|---|---|
|标准名称||
|常见别名||
|产品类型|regular_course / competition_service / project_camp / brand|
|当前状态|active / paused / deprecated / draft|
|适用学生||
|业务负责人/归口||
|最近核验|YYYY-MM-DD|
|下次复核|YYYY-MM-DD|
|更新策略|auto_low_risk / pending_review / manual_only|
|风险等级|low / medium / high|
|是否可外发|true / false / conditional|
|主要来源ID||

## 一句话定位

## 适合谁

## 不适合谁

## 核心交付

## 价格/课时边界

> 涉及价格、课时、合同、退费时，必须写明：最新执行以当期 SOP、正式合同和校区签约为准。

## 顾问表达建议

## 禁用表达
```

---

## 赛事资料卡模板

```markdown
# 赛事名：资料卡

## 元信息

|字段|内容|
|---|---|
|标准名称||
|简称/别名||
|赛事层级|core / supplemental / historical|
|业务角色|research_validation / creative_incubation / competition_service / regional_event|
|Lab赛事包角色|core_event / supplemental_event / not_included|
|适用产品映射||
|当前状态|active / paused / deprecated / draft|
|最近核验|YYYY-MM-DD|
|下次复核|YYYY-MM-DD|
|更新策略|auto_low_risk / pending_review / manual_only|
|风险等级|low / medium / high|
|是否可外发|true / false / conditional|
|主要来源ID||

## 赛事定位

## 参赛对象

## 评审/筛选方式

## 近年时间线

## 可公开引用数据

## 顾问表达建议

## 禁用表达

> 不得承诺获奖、升学、综评结果；当年节点以官方通知为准。
```

---

## 口播/话术资料卡模板

```markdown
# 话术主题

## 元信息

|字段|内容|
|---|---|
|适用场景|家长咨询 / 顾问训练 / 小红书 / 社群答疑 / 内部规划|
|是否可外发|true / false / conditional|
|风险等级|low / medium / high|
|来源ID||
|最近核验|YYYY-MM-DD|
|更新策略|auto_low_risk / pending_review / manual_only|

## 可用表达

## 不能这么说

## 改写边界
```

---

## 区域赛事赛情资料卡模板

```markdown
# 区域名赛事赛情资料卡

## 元信息

|字段|内容|
|---|---|
|区域||
|覆盖年份||
|主要赛事||
|本地证据强度|strong / medium / weak|
|是否可外发|true / false / conditional|
|风险等级|low / medium / high|
|主要来源ID||
|最近核验|YYYY-MM-DD|
|使用边界||

## 结论摘要

## 申报与赛事机制

## 竞争强度判断

## 重点关注学校属性

## 校区规划建议

## 已确认信息

## 推断信息

## 待补事项

## 来源索引
```

---

## 学校资料卡模板

```markdown
# 学校名

## 元信息

|字段|内容|
|---|---|
|城市||
|区||
|学校名称||
|学段||
|学校性质||
|内部参考标签||
|科创信号强度|strong / medium / weak / unknown|
|来源批次||
|最近核验|YYYY-MM-DD|
|置信度||
|是否可外发|conditional|

## 学校定位

## 课程/班型特色

## 科创信号

## 升学/考试信号

## 赛事/材料提示

## 对 ideaLab 规划的意义

## 顾问追问

## 使用边界

> 不承诺录取、优录、自招、综评、分班、直升或获奖结果。学校属性、招生细则、班型和赛事规则均需以当年官方通知复核。
```

---

## 图片/附件 manifest 模板

```json
{
  "asset_id": "",
  "path": "",
  "asset_type": "official_logo / poster / screenshot / reference_image / internal_attachment",
  "source_id": "",
  "can_send_to_user": false,
  "usage_context": "",
  "rights_note": "",
  "risk_level": "low / medium / high",
  "last_verified": "YYYY-MM-DD"
}
```
