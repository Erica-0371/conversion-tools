# Doc Convert

纯浏览器端的文档格式转换工具。不上传、不存储、零服务器依赖。

## 使用方式

双击 `doc2md.html` 即可打开，拖拽或选择文件（支持多选）。

## 支持输入

| 格式 | 说明 |
|------|------|
| `.docx` | Word 文档（mammoth.js 解析） |
| `.html` / `.htm` | 网页文件 |
| `.txt` | 纯文本 |
| `.csv` | 逗号分隔值，转为表格 |
| `.rtf` | 富文本，提取纯文本 |
| `.json` | 格式化为代码块 |
| `.xml` | 结构化提取 |

> 不支持旧版 `.doc`，建议先用 WPS/Word 另存为 `.docx`。

## 支持输出

| 输出格式 | 说明 |
|----------|------|
| **Markdown** | 复制到剪贴板 / 下载 .md 文件 |
| **PDF** | 可选纸张（A3/A4/A5/Letter/Legal）、方向、边距、质量 |

## 功能

- 多文件批量转换，文件列表管理
- Markdown 源码编辑 + 实时渲染预览
- 下载时可自定义文件名
- PDF 导出：基于渲染预览生成，可调纸张/方向/边距/质量
- docx 中文防乱码：自动清理转义字符、零宽字符

## 目录结构

```
doc2md/
├── doc2md.html                  主文件，双击打开
└── libs/
    ├── mammoth.browser.min.js   docx 解析
    ├── turndown.js              HTML → Markdown
    ├── turndown-plugin-gfm.js   GFM 扩展（表格、删除线等）
    ├── marked.min.js            Markdown 渲染预览
    └── html2pdf.bundle.min.js   PDF 导出（html2canvas + jsPDF）
```

## 离线使用

所有依赖已下载到 `libs/`，完全离线可用。

## 技术栈

- [mammoth.js](https://github.com/mwilliamson/mammoth.js) v1.6.0
- [turndown](https://github.com/mixmark-io/turndown) v7.2.0
- [turndown-plugin-gfm](https://github.com/mixmark-io/turndown-plugin-gfm) v1.0.2
- [marked](https://github.com/markedjs/marked) v12.0.2
- [html2pdf.js](https://github.com/eKoopmans/html2pdf.js) v0.10.2
