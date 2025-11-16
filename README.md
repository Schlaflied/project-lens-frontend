# 🔬 Project Lens / 职场透镜 - 前端

An AI-driven web application that provides deep insights into a company's culture, operations, and public perception, helping job seekers avoid pitfalls and identify legitimate opportunities.

一个由 AI 驱动的在线应用，旨在深度分析公司的文化、运营状况及公众舆论，帮助求职者“排雷”，识别并避开不靠谱的企业。

## 功能亮点 / Features

* **全方位公司分析 / Comprehensive Company Analysis:** 只需输入公司名称，AI 便会自动进行全网调查，生成一份关于该公司文化、稳定性和潜在风险的详细报告。/ Enter a company name, and the AI will conduct a thorough investigation, generating a detailed report on its culture, stability, and potential red flags.
* **简历职位匹配度分析 / Resume-to-Job Matching:** 您可以选择性地粘贴简历，以获得您的个人背景与目标公司特定职位的精准匹配度分析。/ Optionally, paste your resume to get a precise analysis of how well your profile matches a specific job title at the target company.
* **数据驱动洞察 / Data-Driven Insights:** 分析过程基于真实的招聘市场数据，通过检索和参考领英（LinkedIn）、Indeed、Glassdoor 等主流平台，提供有据可依的见解。/ The analysis is grounded in real-world data by searching and referencing major job portals and professional networks like LinkedIn, Indeed, and Glassdoor.
* **引用来源 / Source Citation:** 为分析结果提供清晰的数据来源链接，确保信息透明，并方便用户进行更深入的核实。/ Provides direct links to the articles, reviews, and postings used for the analysis, ensuring transparency and allowing for deeper verification.
* **完全双语界面 / Fully Bilingual Interface:** 支持简体中文、繁体中文和英文，满足不同语言用户的需求。/ Supports Simplified Chinese, Traditional Chinese, and English, making it accessible to a global user base.
* **优雅且人性化的设计 / Sleek & User-Friendly Design:** 采用简洁、响应式的双栏布局，并提供深色/浅色模式切换功能，带来舒适的视觉体验。/ Features a clean, responsive two-panel layout with a light/dark mode theme switcher for an optimal user experience.

## 技术栈 / Tech Stack

本部分仅列出前端技术栈。/ This section only lists the frontend tech stack.

| 模块 / Module | 组件 / Component | 描述 / Description |
| :--- | :--- | :--- |
| **基础 / Core** | HTML5, CSS3, Vanilla JavaScript | 负责构建界面和核心交互逻辑。/ Responsible for building the interface and core interaction logic. |
| **Markdown 渲染 / Markdown Rendering** | Marked.js | 用于解析和渲染后端返回的 Markdown 报告内容。/ For parsing and rendering Markdown in the results returned by the backend. |
| **安全 / Security** | DOMPurify | 用于清理 HTML 输出，防止 XSS 攻击。/ For sanitizing HTML output to prevent XSS attacks. |
| **部署环境 / Deployment** | Single-Page Application (SPA) | 可直接在浏览器中打开运行的单页面应用。/ A single-page application that can be opened directly in a web browser. |

## 工作原理 / How It Works

* **用户输入 / User Input:** 用户在前端界面输入公司名称、职位（可选）以及简历文本（可选）。/ The user enters a company name, an optional job title, and optional resume text into the web interface.
* **API 请求 / API Request:** 前端将这些信息打包成 JSON 格式，发送到部署在 Google Cloud Run 上的后端 API。/ The frontend sends this information as a JSON payload to the secure backend API hosted on Google Cloud Run.
* **后端分析 / Backend Analysis:** 后端服务接收到请求，进行数据检索和 AI 分析（详情见后端 README）。/ The backend service receives the request, performs data retrieval and AI analysis (see Backend README for details).
* **结果展示 / Display Results:** 最终生成的报告（结构化数据和引用来源链接）被传回前端，前端使用 Marked.js 和 DOMPurify 进行解析和安全渲染。/ The final generated report (structured data and source links) is sent back to the frontend, which uses Marked.js and DOMPurify for parsing and secure rendering.

## 如何使用（前端）/ How to Use (Frontend)

本项目是一个单页面的 Web 应用，部署极其简单。/ This project is a single-page web application, making deployment extremely simple.

1.  **下载 / Download:** 将 `index.html` 文件保存到你的本地机器。/ Save the `index.html` file to your local machine.
2.  **在浏览器中打开 / Open in Browser:** 直接用任何现代浏览器（如 Chrome, Firefox, Edge）打开 `index.html` 文件即可。/ Simply open the `index.html` file with any modern web browser (like Chrome, Firefox, or Edge).
3.  **功能运行 / Functionality:** 前端界面交互功能完整。请注意，**分析功能需要连接到已部署的后端 API** 才能正常工作，请确保您有网络连接。/ The frontend is fully functional for UI interactions. Please note that **the analysis feature requires connection to the deployed backend API** to work, ensure you have an active internet connection.
