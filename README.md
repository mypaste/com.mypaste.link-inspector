# 链接类型

MyPaste extension `com.mypaste.link-inspector` (version `1.0.2`).

打开一条链接时自动调用「链接类型识别」能力，展示推断出的 MIME、类别、置信度与判断依据，并直接用合适的渲染器显示图片、音视频、JSON 与文本；渲染前先读服务器响应头的实际类型，路径没有扩展名时也不会被当成网页；抓不到内容时说明原因。可复制 MIME、链接或完整结果；没有安装识别能力时说明原因。

This repository is an independent copy extracted from the former `mypaste-code-extensions` monorepo at commit `2af6675ab1473c9e38146ea0b6da68256a293440`. It contains only this extension's tracked source files. The published `.mypaste-plugin` archives and marketplace index live in [`mypaste-extensions-catalog`](https://github.com/mypaste/mypaste-extensions-catalog).

The manifest speaks MyPaste plugin protocol v3. Installation, capability mediation, and content-digest verification are performed by the MyPaste desktop host.

## Files

- `mypaste.plugin.json`: package identity and capability declaration.
- `run.sh`, `src/`, `panel.html`, or `run`: package implementation.

## Build

```bash
bun install
bun run build
```

The generated `preview.html` is intentionally ignored; edit `src/preview.html` and `src/main.ts` instead.

## License

MIT. See [LICENSE](LICENSE).
