🔬 Project Lens / 职场透镜
An AI-driven web application that provides deep insights into a company's culture, operations, and public perception, helping job seekers avoid pitfalls and identify legitimate opportunities.

一个由 AI 驱动的在线应用，旨在深度分析公司的文化、运营状况及公众舆论，帮助求职者“排雷”，识别并避开不靠谱的企业。

Features / 功能亮点
Comprehensive Company Analysis: Enter a company name, and the AI will conduct a thorough investigation, generating a detailed report on its culture, stability, and potential red flags.

Resume-to-Job Matching: Optionally, paste your resume to get a precise analysis of how well your profile matches a specific job title at the target company.

Data-Driven Insights: The analysis is grounded in real-world data by searching and referencing major job portals and professional networks like LinkedIn, Indeed, and Glassdoor.

Source Citation: Provides direct links to the articles, reviews, and postings used for the analysis, ensuring transparency and allowing for deeper verification.

Fully Bilingual Interface: Supports Simplified Chinese, Traditional Chinese, and English, making it accessible to a global user base.

Sleek & User-Friendly Design: Features a clean, responsive two-panel layout with a light/dark mode theme switcher for an optimal user experience.

全方位公司分析: 只需输入公司名称，AI 便会自动进行全网调查，生成一份关于该公司文化、稳定性和潜在风险的详细报告。

简历职位匹配度分析: 您可以选择性地粘贴简历，以获得您的个人背景与目标公司特定职位的精准匹配度分析。

数据驱动洞察: 分析过程基于真实的招聘市场数据，通过检索和参考领英（LinkedIn）、Indeed、Glassdoor 等主流平台，提供有据可依的见解。

引用来源: 为分析结果提供清晰的数据来源链接，确保信息透明，并方便用户进行更深入的核实。

完全双语界面: 支持简体中文、繁体中文和英文，满足不同语言用户的需求。

优雅且人性化的设计: 采用简洁、响应式的双栏布局，并提供深色/浅色模式切换功能，带来舒适的视觉体验。

Tech Stack / 技术栈
Frontend:

HTML5

CSS3 (with responsive design)

Vanilla JavaScript

Marked.js: For parsing and rendering Markdown in the results.

DOMPurify: For sanitizing HTML output to prevent XSS attacks.

Backend (Inferred from Frontend Code):

Cloud Platform: Google Cloud Run

Core AI: Google Gemini API

Architecture: A serverless function that likely performs web searches, aggregates data, and uses an LLM to synthesize the results into a coherent report.

How It Works / 工作原理
User Input / 用户输入: The user enters a company name, an optional job title, and optional resume text into the web interface.
/ 用户在前端界面输入公司名称、职位（可选）以及简历文本（可选）。

API Request / API 请求: The frontend sends this information as a JSON payload to the secure backend API hosted on Google Cloud Run.
/ 前端将这些信息打包成 JSON 格式，发送到部署在 Google Cloud Run 上的后端 API。

Backend Analysis / 后端分析: The backend service receives the request. It uses the user's input as queries to search job portals, news sites, and review platforms.
/ 后端服务接收到请求，并使用用户输入的信息作为关键词，来检索各大招聘网站、新闻站点和公司点评平台。

AI Generation / AI 生成: The retrieved data, along with the user's original profile, is fed into the Gemini model. The AI analyzes this context and generates a structured, multi-faceted report on the company.
/ 检索到的数据和用户的个人资料，会一同被送入 Gemini 模型。AI 会对这些信息进行综合分析，并生成一份结构化、多维度的公司分析报告。

Display Results / 结果展示: The generated report (in Markdown format) and a list of source links are sent back to the frontend, which then parses and securely renders them for the user.
/ 最终生成的报告（Markdown格式）和引用来源链接被传回前端，经过解析和安全处理后，清晰地展示给用户。

How to Use (Frontend) / 如何使用（前端）
This project is a single-page web application.

本项目是一个单页面的 Web 应用。

Download: Save the index.html file to your local machine.
/ 下载: 将 index.html 文件保存到你的电脑上。

Open in Browser: Simply open the index.html file with any modern web browser (like Chrome, Firefox, or Edge).
/ 在浏览器中打开: 直接用任何现代浏览器（如 Chrome, Firefox, Edge）打开 index.html 文件即可。

Functionality: The frontend is fully functional for UI interactions. For the analysis feature to work, it needs to be able to connect to the live backend API. Ensure you have an active internet connection.
/ 功能: 前端界面交互功能完整。分析功能需要连接到已部署的后端API才能正常工作，请确保您有网络连接
