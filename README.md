# conversion-tools

**一键把文档转成 Markdown 或 PDF —— 把 Word 转 md、把 HTML 转 PDF、把对话记录转成网页。**

打开网页就能用，不用安装、不用联网、不上传服务器，文件全程留在你自己电脑里。

---

## 这个仓库能帮你做什么

### 📄 文档转换（`doc2md.html`）

把文档一键转成 **Markdown** 或 **PDF**。

**能转入的格式（输入）：**

| 输入 | 例子 |
|------|------|
| Word 文档 | `.docx` |
| 网页 | `.html` / `.htm` |
| 纯文本 | `.txt` |
| 表格 | `.csv` |
| 富文本 | `.rtf` |
| 数据 | `.json` / `.xml` |

**能转出的格式（输出）：**

| 输出 | 说明 |
|------|------|
| **Markdown (`.md`)** | 一键复制，或下载文件 |
| **PDF** | 可选 A4 / A3 / A5 / Letter / Legal 纸张、方向、边距 |

常见用法：
- **Word → Markdown**：把 `.docx` 拖进去，直接出 md
- **HTML → PDF**：把网页文件拖进去，导出成 PDF（保留原排版）
- 支持一次拖入多个文件批量转换

### 💬 对话查看器（`chat-viewer-index.html`）

把 Claude Code 导出的杂乱 JSON 对话变成排版清晰、可搜索、可筛选的阅读页面——思考与工具调用默认折叠、按需展开，还能单独导出某条对话，方便随时复盘和分享自己的 AI 协作记录。

---

## 怎么用

1. 下载对应的 HTML 文件（文档转换还需连同 `libs/` 文件夹一起下载）
2. 双击，用浏览器打开
3. 把文件拖进去，选择要转成什么格式，下载

就这么简单。没有安装步骤，断网也能用。

---

## 为什么放心用

- **不上传** —— 所有转换都在你浏览器里完成，文件不发往任何服务器
- **不存储** —— 关掉网页，啥都不留
- **离线可用** —— 依赖库已经打包在 `libs/` 里，没网照样转

## 目录结构

```
conversion-tools/
├── doc2md.html              文档转换（→ Markdown / PDF）
├── chat-viewer-index.html   对话记录查看器
└── libs/                    文档转换用到的本地库
    ├── mammoth.browser.min.js   解析 Word
    ├── turndown.js              HTML → Markdown
    ├── turndown-plugin-gfm.js   表格 / 任务列表支持
    └── marked.min.js            Markdown 预览渲染
```
