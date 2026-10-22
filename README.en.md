# SunriseHOT

**A website that finds hot topics and writes its own daily report.**

SunriseHOT collects material from a set of sources, screens it with an LLM, scores candidates twice independently, writes Chinese titles and summaries for the picks, clusters coverage of the same event, ranks hot topics, and publishes a daily report every morning.

Swap in your own sources and your own editorial standards, and it becomes a hot-topic site for any industry.

## Run it

You need [Docker](https://docs.docker.com/get-started/get-docker/), [Node.js 24](https://nodejs.org/en/download), and an OpenAI-compatible LLM API key.

```bash
git clone https://github.com/tibo128728-rgb/sunrise-hot.git
cd sunrise-hot
node scripts/init-env.ts --llm-key <your LLM API key>
docker compose up -d --build
```

Open <http://localhost:3000>. The admin panel is at `/admin`.

## License

MIT. Built on the open-source [AIHOT](https://github.com/KKKKhazix/AIHOT) framework (MIT); see [`LICENSE`](LICENSE) and [`NOTICE`](NOTICE).
