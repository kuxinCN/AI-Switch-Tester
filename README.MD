**# 赛博试轴器 (AI Switch Tester)**



**> 像试轴器一样，插上去测测 AI 接口能不能用。**



**\[!\[Made by kuxin](https://img.shields.io/badge/Made%20by-kuxin-d46a4a)](https://mykuxin.com)**

**\[!\[GitHub](https://img.shields.io/badge/GitHub-kuxinCN-181717?logo=github)](https://github.com/kuxinCN)**



**🔗 \*\*在线试用\*\*：\[ast.mykuxin.com](https://ast.mykuxin.com)**



**一个纯前端的 AI 接口可用性测试工具。无需后端，无需构建，单文件即用。**



**---**



**## ✨ 功能特性**



**- \*\*对话型 AI 测试\*\***

&#x20; **- 支持 \*\*OpenAI 协议\*\* 与 \*\*Anthropic 协议\*\***

&#x20; **- 自动发送「你好」测试连通性**

&#x20; **- 实时展示响应内容、原始返回与请求耗时（ms）**



**- \*\*TTS 语音合成测试\*\***

&#x20; **- 支持 \*\*OpenAI 协议\*\*、\*\*小米 MiMo\*\*、\*\*阿里云\*\***

&#x20; **- 可自由输入音色（Voice）、倍速（仅 OpenAI）、朗读风格指令（仅小米）**

&#x20; **- 输入文本即刻合成并试听**

&#x20; **- 自动识别二进制音频或 JSON 内嵌 base64 音频**



**- \*\*本地存储\*\***

&#x20; **- 所有配置仅保存在浏览器 `localStorage`**

&#x20; **- 无保存按钮，输入即存，刷新不丢**



**- \*\*单文件零依赖\*\***

&#x20; **- 只有 `index.html`，复制即用，可部署在任何静态托管平台**



**---**



**## 🚀 快速开始**



**### 1. 下载项目**



**```bash**

**git clone https://github.com/kuxinCN/ai-switch-tester.git**

**```**



**### 2. 部署方式**



**\*\*方式 A：直接在浏览器打开\*\***



**双击 `index.html` 即可。但部分 API 可能受浏览器 CORS 跨域限制，建议使用方法 B。**



**\*\*方式 B：部署到静态托管平台（推荐）\*\***



**将 `index.html` 放在网站根目录即可，例如：**



**- \*\*Cloudflare Pages\*\*：上传 ZIP 包（确保解压后根目录是 `index.html`）**

**- \*\*Vercel / Netlify\*\*：直接拖拽部署**

**- \*\*GitHub Pages\*\*：推送到仓库并开启 Pages**



**### 3. 开始测试**



**打开页面后，选择 \*\*对话型 AI\*\* 或 \*\*TTS 语音合成\*\*，填入接口地址、API Key、模型名等参数，点击测试按钮即可。**



**---**



**## 📖 使用说明**



**### 对话型 AI**



**| 协议 | 接口地址格式 | 请求路径 |**

**|------|-------------|----------|**

**| OpenAI | `https://api.openai.com/v1` | `/chat/completions` |**

**| Anthropic | `https://api.anthropic.com` | `/v1/messages` |**



**- 程序会自动补全路径，填到版本目录即可。**

**- 本地接口可留空 API Key。**



**### TTS 语音合成**



**| 协议 | 接口地址 | 特殊参数 |**

**|------|---------|----------|**

**| OpenAI | `https://api.openai.com/v1` | 倍速（0.5 - 2） |**

**| 小米 MiMo | `https://api.xiaomimimo.com/v1` | 朗读风格指令 |**

**| 阿里云 | `https://dashscope.aliyuncs.com/compatible-mode/v1` | — |**



**- 音色输入框支持手动填写，切换协议时会自动填入推荐默认值。**

**- 若音频返回在 JSON 中（如小米 MiMo），程序会自动解析 base64 并播放。**



**---**



**## 🛠️ 技术栈**



**- 原生 HTML / CSS / JavaScript**

**- 无框架、无构建工具、无外部依赖**

**- 使用 `localStorage` 持久化配置**

**- 使用 `fetch` 调用接口**

**- 使用 `Blob` + `URL.createObjectURL` 播放合成音频**



**---**



**## 📁 项目结构**



**```**

**.**

**└── index.html   # 全部代码都在这里**

**```**



**---**



**## ⚠️ 注意事项**



**- \*\*API Key 安全\*\*：所有配置仅存储在浏览器本地，不会上传到任何服务器。但请勿在公共电脑上保存敏感 Key。**

**- \*\*CORS 跨域\*\*：部分 AI 服务商可能不允许浏览器直接调用，需确认接口支持跨域或自行配置代理。**

**- \*\*音频格式\*\*：TTS 返回的音频格式需为浏览器可播放的类型（如 mp3、wav），程序会自动嗅探 MIME 类型。**



**---**



**## 👤 作者**



**\*\*kuxin\*\***



**- 个人网站：\[mykuxin.com](https://mykuxin.com)**

**- GitHub：\[github.com/kuxinCN](https://github.com/kuxinCN)**



**---**



**## 📄 许可**



**本项目采用 \[PolyForm Noncommercial License 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/) 协议。**



**- ✅ 允许个人学习、研究、修改和非营利性分享。**

**- ⚠️ 修改或分发时，\*\*必须保留原作者署名\*\*（kuxin）及原项目链接。**

**- ❌ \*\*禁止任何形式的商业用途\*\*（包括出售、按次收费、作为商业产品的一部分等）。**



**详见 \[LICENSE](./LICENSE) 文件。**

