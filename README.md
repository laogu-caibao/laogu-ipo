# 打新日历

`laogu-ipo`

打新日历 skill：每周生成本周新股申购与上市日历。

## 一键安装

```bash
npx skills add laogu-caibao/laogu-ipo
```

仓库地址（点击复制）：

`https://github.com/laogu-caibao/laogu-ipo`

**方式一：克隆**

```bash
git clone https://github.com/laogu-caibao/laogu-ipo.git
```

**方式二：下载 ZIP**

https://github.com/laogu-caibao/laogu-ipo/archive/refs/heads/main.zip

**导入使用**

- Claude Code / Muse：把仓库中的 `SKILL.md` 放到 `~/.claude/skills/laogu-ipo/` 下即可调用。
- 豆包智能体 / Workbuddy 等：按各平台的 skill 上传流程导入 `SKILL.md`。
- 扣子 Coze：扣子编程 → 技能面板 → 创建技能 → 本地上传，上传本仓库打包的 zip（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；如页面要求 `.skill` 后缀，由扣子导入后自动生成，不要只改扩展名。
- Trae：设置 → 技能 → 上传技能，上传同上 zip；或手动放到 `~/.trae/skills/laogu-ipo/`（项目级用 `.trae/skills/laogu-ipo/`）。Trae 也支持 MCP：把 `uvx laogu-mcp` 配进 MCP 设置即可获得 16 个工具（skill 负责流程指导、MCP 负责工具调用）。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
## 文件结构

- `SKILL.md` — 主流程（平台中立，定时能力由宿主平台提供）
- `references/sources.md` — 数据源：网页搜索模板、媒体来源优先级、东财数据中心备选

## 输出结构

- 本周申购：申购日期、代码、名称、发行价、申购上限、市盈率
- 本周上市：上市日期、代码、名称
- 节假日提醒：节前最后交易日、节后首个交易日（临近长假时）

## 定时建议

- 每周一早上 8:30 前推送（遇长假调为节后首个交易日）
- 可与 `laogu-morning` 联动，自动带入今日新股申购看点

---
## English

**laogu-ipo — IPO calendar.** This week's A-share subscriptions and listings: codes, names, subscription dates, offer prices, P/E ratios. When there are none, it says so plainly instead of making things up. Install: `npx skills add laogu-caibao/laogu-ipo`.

## FAQ

**Q：laogu-ipo 有什么用？**
适合的场景：想知道本周有哪些新股申购和上市，代码、发行价、市盈率、日期一张表看清。

**Q：数据可靠吗？会荐股吗？**
数字必须来自可核验的公开来源（上市公司公告、交易所公开数据、公开网页），取不到就标「未核验」，绝不编造；只做结构化整理与解读，不构成投资建议。

**Q：怎么安装？支持哪些 AI 平台？**
```bash
npx skills add laogu-caibao/laogu-ipo
```
平台中立 Markdown，Claude Code、Codex、豆包智能体、Workbuddy、扣子 Coze、Trae 等环境均可用；数据能力可用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)（`uvx laogu-mcp`）一次装齐。更多 skill 见[老谷拆财报组织主页](https://github.com/laogu-caibao)。
---

## 出品

**老谷拆财报** —— 以数据为刃，剖市场真相

- 抖音 / 微信视频号 / 今日头条 / 快手：搜索「老谷拆财报」
- 固定栏目：「价值投资之财报解读」（全网连载中）
- 本 skill 的方法论与账号内容同源：数据驱动、拆开看、不讲黑话

### 扫码关注

| 微信视频号 | 抖音 |
|---|---|
| ![视频号二维码](docs/qrcode-shipinhao.jpg) | ![抖音二维码](docs/qrcode-douyin.png) |
| 扫一扫，关注视频号 | 抖音号：gubaobao22 |

> 作者声明：个人观点，仅供参考，不构成投资建议。
