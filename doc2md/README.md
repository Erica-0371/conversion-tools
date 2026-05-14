# Doc2MD

纯浏览器端的文档转 Markdown 工具。不上传、不存储、零服务器依赖。

## 使用方式

双击 `doc2md.html` 即可打开，支持拖拽或点击选择文件（支持多选）。

## 支持格式

| 格式 | 说明 |
|------|------|
| `.docx` | Word 文档，通过 mammoth.js 解析 |
| `.html` / `.htm` | 网页文件，通过 turndown.js 转换 |
| `.txt` | 纯文本，直接保留 |
| `.csv` | 逗号分隔，转为 Markdown 表格 |
| `.rtf` | 富文本，提取纯文本内容 |
| `.json` | 格式化为代码块 |
| `.xml` | 结构化提取或代码块 |
| `.md` | Markdown，直接预览 |

> 不支持旧版 `.doc` 格式（二进制格式无法在浏览器端可靠解析），建议先用 WPS/Word 另存为 `.docx`。

## 功能

- 多文件批量转换，文件列表管理
- 源码编辑 + 实时预览（marked.js 渲染）
- 下载时可自定义文件名
- 复制到剪贴板 / 单个下载 / 全部下载
- docx 中文防乱码：自动清理转义字符、零宽字符

## 目录结构

```
doc2md/
├── doc2md.html                  主文件，双击打开
└── libs/                        本地依赖库
    ├── mammoth.browser.min.js   docx 解析
    ├── turndown.js              HTML → Markdown
    ├── turndown-plugin-gfm.js   GFM 扩展（表格、删除线等）
    └── marked.min.js            Markdown 预览渲染
```

## 离线使用

所有依赖已下载到 `libs/` 目录，完全离线可用。如果 `libs/` 目录丢失，工具会自动尝试从 CDN 加载（需联网）。

## 技术栈

- [mammoth.js](https://github.com/mwilliamson/mammoth.js) v1.6.0 — docx 转 HTML
- [turndown](https://github.com/mixmark-io/turndown) v7.2.0 — HTML 转 Markdown
- [turndown-plugin-gfm](https://github.com/mixmark-io/turndown-plugin-gfm) v1.0.2 — GFM 表格/任务列表支持
- [marked](https://github.com/markedjs/marked) v12.0.2 — Markdown 渲染预览
