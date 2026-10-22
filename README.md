# 朝阳热点 SunriseHOT

**一个自己找热点、自己写日报的网站。**

朝阳热点从一批信源里收资料，用大模型先筛一遍、再独立打两次分，挑出真正值得看的，写成中文标题和摘要；把不同来源说的同一件事聚成一个事件，按有多少人在说排出热点；每天早上出一份日报。

把信源换成你的，把精选标准换成你的 KnowHow，它就能变成任何一个行业的热点站。

## 功能

- **采集**：RSS、网页列表、JSON 接口、X 账号、公众号等多种信源，自动判重
- **精选**：预筛 + 两次独立评分，分数过门槛才入选，提示词全部可改
- **写作**：入选资料自动生成中文标题、摘要和推荐理由
- **聚簇与热点**：同一事件的多篇报道归并成一个事件，按覆盖来源和讨论热度排行
- **成刊**：日报、周报、月报自动编排
- **出口**：网站、后台、RSS、公开 API 与 MCP，一套引擎全包

## 跑起来

需要 [Docker](https://docs.docker.com/get-started/get-docker/)、[Node.js 24](https://nodejs.org/en/download)，和一个 OpenAI 兼容的模型 API Key（DeepSeek、千问、智谱都可以）。

```bash
git clone https://github.com/tibo128728-rgb/sunrise-hot.git
cd sunrise-hot
node scripts/init-env.ts --llm-key <你的模型 API Key>
docker compose up -d --build
```

打开 <http://localhost:3000>。后台在 `/admin`，管理员密码在 `.env` 的 `ADMIN_PASSWORD` 里。

部署、改成你的行业等更多说明见 [`docs/`](docs/)。

## 技术栈

Node.js 24 · TypeScript · PostgreSQL 17 · Docker Compose

## 许可证

MIT。本项目基于 [AIHOT](https://github.com/KKKKhazix/AIHOT) 开源框架（MIT）二次开发，原始版权声明见 [`LICENSE`](LICENSE) 与 [`NOTICE`](NOTICE)。
