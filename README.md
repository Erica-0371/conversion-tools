# conversion-tools

一组轻量级的纯浏览器端格式转换工具集合。所有工具均为单 HTML 文件，不上传、不存储、零服务器依赖，双击即可使用。

## 工具列表

| 工具 | 说明 | 使用方式 |
|------|------|----------|
| [doc2md](doc2md/) | 文档转 Markdown（支持 docx/html/txt/csv/rtf/json/xml） | 双击 `doc2md/doc2md.html` |
| [chat-viewer](chat-viewer/) | 对话记录查看器（JSON/JSONL 转可读 HTML） | 双击 `chat-viewer/index.html` |

## 设计原则

- **纯本地运行** — 文件不离开浏览器，无需后端服务
- **单文件交付** — 每个工具一个 HTML 文件（+ 可选本地依赖）
- **离线可用** — 依赖库已内置，不需要网络
