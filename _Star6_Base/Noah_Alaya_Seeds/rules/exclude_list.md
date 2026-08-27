# Noah Anchor · 排除字典 (Exclude List)

> 用于中东猎手、经销商扫描、竞品追踪等 cron job 的筛选过滤。匹配任一条目即丢弃该线索。

## 规则

- **company_name_match**: 公司名中包含任一关键词 → 排除
- **url_domain_match**: URL 域名精确或子域匹配 → 排除
- **industry_tag**: 行业标签不在目标范围 → 排除
- **note**: 定期更新，保持精简。每次新增需本贵确认。

## 🔴 Company Name (公司名黑名单)

| 关键词 | 原因 | 添加日期 |
|--------|------|---------|
| `Appalachian Sustainable Development` | 非营利机构/农业转产，与地板无关 | 2026-07-13 |
|| `AS Develop` / `asdevelop` | 同上（域名别名） | 2026-07-13 |
|| `Bostik` / `Gerflor` / `Vinifloor` | 塑料地板 (PVB/SPC)，我们与塑料地板无业务关系 | 2026-07-28 |
|| `Indus Floors` / `Indus Arabia` | 工业混凝土地坪，不同赛道 | 2026-07-28 |
| `FloorWorld LLC` / `floorworld.com` | 中东最大地板公司+Parador/Kahrs代理。渠道封闭，非NOAH客开对象 | 2026-07-13 |
| `Wood Floors Middle East LLC` / `woodfloors.ae` | Kahrs授权高端拼花商。渠道封闭，非NOAH客开对象 | 2026-07-13 |

## 🔵 URL Domain (域名黑名单)

| 域名 | 原因 | 添加日期 |
|------|------|---------|
| `asdevelop.org` | 非营利/农业，与地板无关 | 2026-07-13 |
| `asdevelop.com` | 同上（重定向域名） | 2026-07-13 |

## 🟢 Industry Tag (行业排除标签)

以下行业标签出现在公司描述中 → 丢弃：

- nonprofit / NGO / charity foundation
- tobacco farming support
- agricultural development
- humanitarian aid
- religious organization
