# DeepRead-Agent-Prompt

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/li4oya/DeepRead-Agent-Prompt?style=social)](https://github.com/li4oya/DeepRead-Agent-Prompt/stargazers)
[![Forks](https.img.shields.io/github/forks/li4oya/DeepRead-Agent-Prompt?style=social)](https://github.com/li4oya/DeepRead-Agent-Prompt/network/members)
[![Issues](https://img.shields.io/github/issues/li4oya/DeepRead-Agent-Prompt)](https://github.com/li4oya/DeepRead-Agent-Prompt/issues)

<p align="center">
  <a href="#-about-the-project">English</a> •
  <a href="#-关于项目">简体中文</a>
</p>

An advanced, multi-agent prompt framework for conducting deep, structured analysis of academic papers. This is not just a summarizer; it's a virtual research team at your command.

一个用于对学术论文进行深度、结构化分析的高级多智能体提示词框架。这不仅是一个摘要工具，更是一个听你指挥的虚拟研究团队。

---

<details>
<summary><strong>:us: English Readme</strong></summary>

## 🚀 About The Project

In the age of information overload, researchers and students are drowning in papers. Traditional "summarize this" prompts provide a superficial overview at best. They often miss the nuances of the methodology, the context of the research, and the true significance of the experimental results.

**DeepRead-Agent-Prompt** solves this problem by simulating a collaborative team of AI specialists. Each "agent" has a distinct role—from identifying core concepts to meticulously dissecting the methodology and experimental design. The result is a comprehensive, multi-faceted analysis that mirrors the depth you'd expect from a human expert group.

### ✨ Key Features

*   **🧠 Multi-Agent Simulation**: Deploys five specialized AI agents for a holistic analysis.
*   **🔬 In-Depth Methodological Breakdown**: Goes far beyond summarization to provide a step-by-step deconstruction of the paper's technical approach.
*   **📊 Structured Experimental Analysis**: Presents experimental results in a clear "Reason - Result - Figure" format for easy digestion.
*   **🧩 Context-Aware**: Analyzes the paper's background, core scientific questions, and its place within the broader research landscape.
*   **🤖 Model Agnostic**: Designed to work with any powerful Large Language Model (e.g., GPT-4o, Claude 3 Opus, Gemini 1.5).
*   **📖 Open & Transparent**: The entire prompt is open-source, allowing for community verification, customization, and improvement.

## 🤖 The Core Prompt

This is the engine that drives the analysis. It's designed to be a single, powerful prompt that you provide to your chosen LLM.

<details>
<summary><strong>Click to view the full Multi-Agent Prompt</strong></summary>

```# [Task: In-depth Collaborative Analysis of Academic Paper]

## Role Definition

You will act as a project coordinator, responsible for dispatching five AI agents with different professional capabilities to collaboratively complete a comprehensive, in-depth analysis of an academic paper. These five agents are:

1.  **Academic Keyword Extraction Expert**
2.  **Research Background Analysis Expert**
3.  **Problem Identification Expert**
4.  **Methodology Design Analysis Expert**
5.  **Experimental Analysis Expert**

... (The full prompt content is omitted here for brevity, but you should paste the complete English version of your prompt here)
```

</details>

## 🛠️ How to Use

1.  **Copy the Prompt**: Copy the entire core prompt from the section above.
2.  **Prepare Your Materials**:
    *   Convert your target paper (e.g., a PDF) into plain text.
    *   (Optional but Recommended) Note down critical diagrams or formulas with their figure numbers.
3.  **Engage the LLM**:
    *   Open a session with a powerful LLM (e.g., GPT-4o).
    *   Paste the **DeepRead-Agent-Prompt** as your first message.
    *   In the next message, provide the paper's text and any image information.
4.  **Receive the Analysis**: The LLM will generate a detailed, structured report.

## 💡 Example Output

Here is a condensed example of the output for the paper *"Website Fingerprinting on Encrypted Proxies: A Flow-Context-Aware Approach and Countermeasures"*.

<details>
<summary><strong>Click to view example analysis</strong></summary>

*   **Core Keywords**: Website Fingerprinting (WFP), Encrypted Proxies, Training-Testing Asymmetry.
*   **Core Scientific Question**: How to design a practical WFP attack against modern encrypted proxies in real-world scenarios, and what is an effective, lightweight countermeasure?
*   **Method Design Deep Dive**: A two-stage, flow-context-aware system. Stage 1 characterizes flows spatially (W2I). Stage 2 correlates them temporally (LCS).
*   **Experimental Analysis**: The proposed method (CAR) achieved 99.46% TPR with 0.17% FPR, while the realistic baseline (PAR) TPR collapsed to 2.7%, proving CAR's effectiveness.

</details>

## 🤝 Contributing

Contributions are greatly appreciated. Please feel free to fork the repo, create a pull request, or open an issue.

## 🌟 Future Vision & The DeepRead Bot

The `DeepRead-Agent-Prompt` is a powerful foundation. The future vision is to evolve this into a more robust and accessible tool.

**For a more convenient, one-click experience, we are developing the DeepRead Bot.** This bot will offer features like direct PDF/URL upload, interactive analysis, and knowledge base integration.

Stay tuned for updates! Your support for this open-source project helps accelerate the development of these advanced features.

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

## 📧 Contact

Project Link: [https://github.com/li4oya/DeepRead-Agent-Prompt](https://github.com/li4oya/DeepRead-Agent-Prompt)

</details>

---

<details>
<summary><strong>:cn: 简体中文文档</strong></summary>

## 🚀 关于项目

在信息爆炸的时代，研究人员和学生正被海量的论文所淹没。传统的“总结一下”这类提示词最多只能提供肤浅的概览，往往会忽略方法论的细微差别、研究的背景以及实验结果的真正意义。

**DeepRead-Agent-Prompt** 通过模拟一个由AI专家组成的协作团队来解决这个问题。每个“智能体”都有明确的分工——从识别核心概念到一丝不苟地剖析方法论和实验设计。最终产出的是一份全面、多维度的分析报告，其深度足以媲美人类专家团队的水平。

### ✨ 核心特性

*   **🧠 多智能体模拟**：调度五个专业的AI智能体，进行全面的协同分析。
*   **🔬 深度方法剖析**：远超普通摘要，对论文的技术方案进行逐步骤的解构。
*   **📊 结构化实验分析**：以清晰的“理由-结果-图表”格式呈现实验结果，易于理解。
*   **🧩 上下文感知**：分析论文的研究背景、核心科学问题及其在更广阔研究领域中的位置。
*   **🤖 模型无关**：旨在与任何强大的大型语言模型（如 GPT-4o, Claude 3 Opus, Gemini 1.5）协同工作。
*   **📖 开放透明**：整个提示词完全开源，允许社区验证、定制和改进。

## 🤖 核心提示词

这是驱动整个分析过程的引擎。它被设计成一个单一、强大的提示词，您可以直接提供给您选用的大语言模型。

<details>
<summary><strong>点击查看完整的多智能体提示词</strong></summary>

```# [任务：学术论文深度协同分析]

## 角色定义

你将扮演一个项目协调员的角色，负责调度五个具有不同专业能力的AI智能体来协同完成一项综合性的论文深度分析任务。这五个智能体分别是：

1.  **学术关键词提取专家**
    *   职责：从论文内容中识别并提取3-5个最核心的学术领域关键词
    *   工作重点：结合摘要、正文和图表内容，确保关键词的准确性和代表性

2.  **研究背景分析专家**
    *   职责：全面分析论文的研究背景和相关工作
    *   工作重点：
        *   总结论文所处领域的研究现状、面临的挑战和发展趋势
        *   列出并分析相关研究工作，包括重要的先驱性研究和最新进展
        *   阐述本研究的重要性、必要性和创新性贡献
        *   参考引言部分和相关数据图表

3.  **问题识别专家**
    *   职责：精确识别和阐述论文的核心科学问题
    *   工作重点：
        *   清晰定义论文旨在解决的核心问题
        *   分析该问题的重要性和研究价值
        *   识别现有方法的局限性和不足
        *   结合问题示例图或对比图增强理解

4.  **方法设计分析专家**
    *   职责：深度解析论文提出的方法论，提供逐步骤、多层次的技术方案剖析
    *   详细工作要求：
        *   **4.1 方法总体架构分析**: 整体设计理念、架构组件图解、数据流向分析、与现有方法的差异。
        *   **4.2 关键步骤逐一解析**: 对方法的每个关键步骤进行深度剖析，包括目标与作用、输入输出定义、核心算法机制、技术实现细节、创新点识别、对应图表引用。
        *   **4.3 关键技术深度解读**: 核心算法详解、关键数据结构、优化策略分析、鲁棒性设计。
        *   **4.4 方法集成与协同**: 模块间交互、端到端流程、关键决策点。

5.  **实验分析专家**
    *   职责：系统性评估论文的实验设计和结果分析
    *   工作重点：
        *   详细描述实验环境设置（数据集、评估指标、基线方法、硬件配置等）
        *   按照规范化格式分析每个实验，具体包括：实验设计的理由、实验结果、对应图表。
        *   评估实验的充分性、科学性和说服力。

## 输入材料

你将接收以下完整的论文材料：

*   **论文摘要**：核心内容概述
*   **论文正文**：经过深度清洗和预处理的全文文本
*   **图片资源列表**：包含论文每一页的高清图片路径，涵盖图表、公式、算法流程图和系统架构图

## 执行流程

1.  **阶段一：任务分发与指导**: 将论文材料分发给所有五个专业智能体，并提供针对性的工作指导。
2.  **阶段二：协调与整合**: 收集并整合所有智能体的专业分析结果，形成结构化的综合报告。

## 最终交付物

生成一份结构清晰、内容详实的综合分析报告，严格按照以下五个部分组织：

1.  **核心关键词**
2.  **研究背景与相关工作**
3.  **核心科学问题**
4.  **方法设计详解** (包含4.1-4.4的详细子部分)
5.  **实验分析** (包含5.1-5.2的详细子部分)

请确保报告的专业性、完整性、准确性、深度性、规范性、条理性和图表关联性。现在，请按照上述要求，开始执行学术论文的深度协同分析任务。
```

</details>

## 🛠️ 如何使用

1.  **复制提示词**: 复制上方区域内的完整核心提示词。
2.  **准备材料**:
    *   将你的目标论文（例如 PDF 文件）转换为纯文本。
    *   （可选但推荐）如果论文中有关键的图表或公式，请记下它们的编号。
3.  **与大模型交互**:
    *   在你选用的大模型（如 GPT-4o）的对话界面中。
    *   将 **DeepRead-Agent-Prompt** 作为你的第一条消息粘贴并发送。
    *   在下一条消息中，提供论文的文本和图表信息。
4.  **接收分析报告**: 大模型将遵循多智能体框架，生成一份详细、结构化的报告。

## 💡 输出示例

以下是针对论文 *《Website Fingerprinting on Encrypted Proxies: A Flow-Context-Aware Approach and Countermeasures》* 生成的分析报告精简示例。

<details>
<summary><strong>点击查看分析示例</strong></summary>

*   **核心关键词**: 网站指纹识别 (WFP), 加密代理, 训练-测试不对称。
*   **核心科学问题**: 在真实世界场景下（解决不对称问题），如何针对现代加密代理设计一种实用且准确的WFP攻击，以及与此对应的轻量级、高效的防御对策是什么？
*   **方法设计详解**: 一个两阶段的、流上下文感知的系统。阶段一在空间上对流进行特征化（计算“网站指示索引”W2I），阶段二在时间上对这些流进行关联（使用最长公共子序列LCS）以识别模式。
*   **实验分析**: 所提出的方法（CAR）实现了99.46%的TPR和仅0.17%的FPR，而模拟真实场景的基线方法（PAR）的TPR骤降至2.7%，这证明了CAR方法的有效性。

</details>

## 🤝 贡献代码

欢迎任何形式的贡献！开源社区因您的每一次贡献而更加精彩。您可以：
*   Fork 本项目
*   创建您的功能分支
*   提交您的更改
*   发起一个 Pull Request
*   或者，提交 Bug 和建议。

## 🌟 未来展望 & DeepRead 机器人

`DeepRead-Agent-Prompt` 是一个强大的基础。我们的愿景是将其发展成一个更强大、更易于使用的工具。

**为了提供更便捷的一键式体验，我们正在开发 DeepRead 机器人。** 这款机器人将登陆 Discord、Slack 等平台，并提供如下高级功能：
*   **直接上传 PDF/URL**：无需再手动复制粘贴文本。
*   **交互式分析**：可针对生成的报告进行追问。
*   **知识库集成**：自动保存和索引您分析过的论文。
*   **持续优化**：机器人将始终运行在最新、最强大的提示词版本上。

敬请期待！您对这个开源项目的支持，将加速这些高级功能的开发。

## 📜 开源许可

本项目采用 MIT 许可协议。详情请见 `LICENSE` 文件。

## 📧 联系方式

项目链接: [https://github.com/li4oya/DeepRead-Agent-Prompt](https://github.com/li4oya/DeepRead-Agent-Prompt)

</details>
