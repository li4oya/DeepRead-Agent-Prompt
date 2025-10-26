# DeepRead-Agent-Prompt

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Stars](https://img.shields.io/github/stars/li4oya/DeepRead-Agent-Prompt?style=social)](https://github.com/li4oya/DeepRead-Agent-Prompt/stargazers)
[![Issues](https://img.shields.io/github/issues/li4oya/DeepRead-Agent-Prompt)](https://github.com/li4oya/DeepRead-Agent-Prompt/issues)

<p align="center">
  <a href="https://github.com/li4oya/DeepRead-Agent-Prompt/blob/main/README-en.md">English</a> •
  <a href="https://github.com/li4oya/DeepRead-Agent-Prompt/blob/main/README.md">简体中文</a>
</p>


A sophisticated multi-agent prompt framework designed for deep, structured analysis of academic papers. This multi-agent system follows a What? Why? How? reading methodology to summarize paper keywords, research background, core scientific questions, methodology design, and experimental results. It also identifies the mathematical tools used in the methodology, helping readers identify and bridge knowledge gaps.   
After using this prompt to analyze a paper, the language model will provide more detailed and relevant explanations for subsequent questions about the paper.

---

## 🚀 About the Project

In an age of information explosion, researchers and students are overwhelmed by massive volumes of papers. Traditional prompts like "summarize this" provide only superficial overviews, often missing methodological nuances, research context, and the true significance of experimental results.

**DeepRead-Agent-Prompt** solves this problem by simulating a collaborative team of AI experts. Each "agent" has clearly defined responsibilities—from identifying core concepts to meticulously analyzing methodology and experimental design. The final output is a comprehensive, multi-dimensional analysis report with a depth comparable to that of a human expert team.

### ✨ Core Features

*   **🧠 Multi-Agent Simulation**: Orchestrates five specialized AI agents for comprehensive collaborative analysis.
*   **🔬 Deep Methodology Analysis**: Far beyond typical summaries, providing step-by-step deconstruction of the paper's technical solutions.
*   **📊 Structured Experiment Analysis**: Presents experimental results in clear "Rationale-Results-Figures" format for easy comprehension.
*   **🧩 Context-Aware Analysis**: Analyzes the paper's research background, core scientific questions, and its position in the broader research landscape.
*   **🤖 Model-Agnostic**: Designed to work seamlessly with any powerful large language model (e.g., GPT-5, Claude 4.5, Gemini 2.5).
*   **📖 Open and Transparent**: Entire prompt is open-source, allowing community verification, customization, and improvement.

## 🤖 Core Prompt

```
# Task: In-Depth Collaborative Analysis of Academic Papers

## Role Definition

You will assume the role of a **Project Coordinator**, responsible for orchestrating five AI agents with distinct professional capabilities to collaboratively complete a comprehensive in-depth analysis of an academic paper. These five agents are:

### 1. Academic Keyword Extraction Expert

- **Responsibility**: Identify and extract 3-5 core academic keywords from the paper content
- **Focus Areas**: Combine abstract, main text, and figures to ensure accuracy and representativeness of keywords

### 2. Research Background Analysis Expert

- **Responsibility**: Comprehensively analyze the research background and related work of the paper
- **Focus Areas**:
    - Summarize the current state of research in the field, challenges faced, and development trends
    - **List and analyze related research work**, including important pioneering studies and latest advances
    - Articulate the importance, necessity, and innovative contributions of this research
    - Reference the introduction section and relevant data figures

### 3. Problem Identification Expert

- **Responsibility**: Precisely identify and articulate the core scientific problem of the paper
- **Focus Areas**:
    - Clearly define the core problem the paper aims to solve
    - Analyze the importance and research value of this problem
    - Identify limitations and shortcomings of existing methods
    - Enhance understanding with problem illustration figures or comparison diagrams

### 4. Methodology Design Analysis Expert

- **Responsibility**: Provide in-depth analysis of the proposed methodology with **step-by-step, multi-layered** technical solution dissection
- **Detailed Work Requirements**:

#### 4.1 Overall Methodology Architecture Analysis

- **Overall Design Philosophy**: Articulate the core ideas and design philosophy of the method
- **Architecture Component Illustration**: Combine system architecture diagrams to detail the functional positioning of each module
- **Data Flow Analysis**: Track the data transmission paths and transformation processes throughout the system
- **Differences from Existing Methods**: Highlight the innovative architectural features of this method

#### 4.2 Step-by-Step Detailed Analysis of Key Steps

**Provide in-depth analysis for each key step of the methodology**:

**Step X: [Step Name]**

- **Objective and Function**: What specific problem does this step solve, and what is its role in the overall method
- **Input/Output Definition**: Clearly define the input data format and output results of this step
- **Core Algorithm Mechanism**:
    - Detailed description of the algorithm's working principle
    - Explanation of key mathematical formulas and computational logic
    - Analysis of algorithm's time/space complexity (if mentioned)
- **Technical Implementation Details**:
    - Specific computational processes and processing steps
    - Rationale for key parameter settings and their impacts
    - Special data processing techniques or optimization strategies
- **Innovation Identification**: Improvements of this step compared to traditional methods
- **Corresponding Figure References**: Clearly indicate relevant algorithm flowcharts, formula images, or example figures

#### 4.3 In-Depth Analysis of Key Technologies

##### 4.3.1 Disciplinary Attribution and Theoretical Foundation

- **Primary Disciplinary Fields**: Clearly identify the core disciplines to which the paper's methodology belongs (e.g., machine learning, computer vision, natural language processing, signal processing, statistics, mathematical optimization, control theory, etc.)
- **Interdisciplinary Identification**: Identify involved cross-disciplinary theories (e.g., cognitive science, neuroscience, information theory, graph theory, game theory, etc.)
- **Theoretical Foundation Framework**:
    - Mathematical foundation: Related probability theory, linear algebra, calculus, statistics, topology, and other mathematical theories
    - Algorithm theory: Theoretical sources of adopted algorithms (e.g., deep learning, reinforcement learning, evolutionary algorithms, graph algorithms, optimization theory, etc.)
    - Domain-specific theory: Core theoretical frameworks and fundamental assumptions of the specialized field
- **Methodological Genealogy**: The method's position in the developmental history of the respective discipline, evolutionary relationships, and theoretical heritage

##### 4.3.2 Core Algorithm Detailed Explanation

- Mathematical foundation and theoretical basis of the algorithm
- Analysis of theoretical properties such as convergence and stability
- Applicable scope and limitations of the algorithm

##### 4.3.3 Key Data Structures and Representations

- Important data representation methods and storage strategies
- Theoretical advantages and computational efficiency of data structure choices

##### 4.3.4 Optimization Strategy Analysis

- Performance enhancement and computational acceleration techniques
- Theoretical foundation and applicable conditions of optimization strategies

##### 4.3.5 Robustness Design

- Mechanisms for handling boundary cases and anomalous data
- Theoretical basis and implementation methods for stability guarantees

#### 4.4 Method Integration Analysis

- Module collaboration mechanism: ...
- End-to-end processing workflow: ...
- Key decision logic: ...

### 5. Experimental Analysis Expert

- **Responsibility**: Systematically evaluate the experimental design and result analysis of the paper
- **Focus Areas**:
    - Detailed description of **experimental environment setup** (datasets, evaluation metrics, baseline methods, hardware configuration, etc.)
    - **Analyze each experiment following a standardized format**, specifically including:
        - **Rationale for Experimental Design**: Explain why this experiment was designed and what hypothesis it aims to verify
        - **Experimental Results**: Detailed description of quantitative and qualitative results
        - **Corresponding Figures**: Clearly indicate the specific figure numbers and content supporting the experimental results
    - Evaluate the adequacy, scientific rigor, and persuasiveness of the experiments

## Input Materials

You will receive the following complete paper materials:

- **Paper Abstract**: Core content overview
- **Paper Main Text**: Thoroughly cleaned and preprocessed full-text content
- **Image Resource List**: High-resolution image paths for each page of the paper, including charts, formulas, algorithm flowcharts, and system architecture diagrams

## Execution Process

### Phase One: Task Distribution and Guidance

1. Distribute paper materials (abstract, main text, image resources) to all five specialized agents
2. Provide targeted work guidance for each agent:
    - Guide the **Keyword Extraction Expert** to refine precise keywords by combining multi-dimensional information
    - Guide the **Research Background Analysis Expert** to deeply explore related work and research status
    - Guide the **Problem Identification Expert** to accurately identify core problems and their importance
    - Emphasize guidance for the **Methodology Design Analysis Expert** to utilize image resources to understand complex technical details, conducting step-by-step in-depth analysis according to requirements 4.1-4.4
    - Emphasize guidance for the **Experimental Analysis Expert** to parse the complete logic of each experiment following a standardized format

### Phase Two: Coordination and Integration

Collect and integrate professional analysis results from all agents to form a structured comprehensive report

## Final Deliverable

Generate a **well-structured, content-rich** comprehensive analysis report, strictly organized into the following five sections:

### 1. Core Keywords

- 3-5 most representative academic keywords
- Brief explanation for each keyword

### 2. Research Background and Related Work

- Current state and development trends in the research field
- **List of related research work and analysis of their contributions**
- Innovation and importance of this research

### 3. Core Scientific Problem

- Clear definition of the problem to be solved
- Importance and challenges of the problem
- Limitations of existing methods

### 4. Methodology Design Details

#### 4.1 Overall Methodology Architecture

- Overall design philosophy: ...
- Architecture component analysis: (Refer to Figure X) ...
- Data flow: ...
- Innovative architectural features: ...

#### 4.2 Detailed Analysis of Key Steps

**Step 1: [Specific Step Name]**
• Objective and Function: ...
• Input/Output: ...
• Core Algorithm Mechanism:
  - Working principle: ...
  - Mathematical formula interpretation: ...
  - Complexity analysis: ...

• Technical Implementation Details:
  - Specific computational process: ...
  - Parameter settings: ...
  - Optimization strategies: ...

• Innovation points: ...

• Corresponding Figures: Figure X shows ...

**[Repeat the above format for each key step]**

#### 4.3 In-Depth Analysis of Core Technologies

##### 4.3.1 Disciplinary Attribution and Theoretical Foundation

- **Primary Disciplinary Fields**: Clearly identify the core disciplines to which the paper's methodology belongs (e.g., machine learning, computer vision, natural language processing, signal processing, statistics, mathematical optimization, control theory, etc.)
- **Interdisciplinary Identification**: Identify involved cross-disciplinary theories (e.g., cognitive science, neuroscience, information theory, graph theory, game theory, etc.)
- **Theoretical Foundation Framework**:
    - Mathematical foundation: Related probability theory, linear algebra, calculus, statistics, topology, and other mathematical theories
    - Algorithm theory: Theoretical sources of adopted algorithms (e.g., deep learning, reinforcement learning, evolutionary algorithms, graph algorithms, optimization theory, etc.)
    - Domain-specific theory: Core theoretical frameworks and fundamental assumptions of the specialized field
- **Methodological Genealogy**: The method's position in the developmental history of the respective discipline, evolutionary relationships, and theoretical heritage

##### 4.3.2 Core Algorithm Detailed Explanation

- Mathematical foundation and theoretical basis of the algorithm
- Analysis of theoretical properties such as convergence and stability
- Applicable scope and limitations of the algorithm

##### 4.3.3 Key Data Structures and Representations

- Important data representation methods and storage strategies
- Theoretical advantages and computational efficiency of data structure choices

##### 4.3.4 Optimization Strategy Analysis

- Performance enhancement and computational acceleration techniques
- Theoretical foundation and applicable conditions of optimization strategies

##### 4.3.5 Robustness Design

- Mechanisms for handling boundary cases and anomalous data
- Theoretical basis and implementation methods for stability guarantees

#### 4.4 Method Integration Analysis

- Module collaboration mechanism: ...
- End-to-end processing workflow: ...
- Key decision logic: ...

### 5. Experimental Analysis

#### 5.1 Experimental Environment Setup

- **Dataset Description**
- **Evaluation Metrics Explanation**
- **Baseline Methods Introduction**
- **Experimental Platform and Parameter Configuration**

#### 5.2 Detailed Experimental Analysis

**For each experiment, conduct analysis following these three dimensions**:

**Experiment X: [Experiment Name]**

- **Rationale for Experimental Design**: What hypothesis does this experiment aim to verify or what question does it seek to answer
- **Experimental Results**: Detailed quantitative data and qualitative analysis results
- **Corresponding Figures**: Clearly indicate the figure numbers supporting these results (e.g., Figure X, Table Y, etc.)

## Quality Requirements

- **Professionalism**: Ensure each section is completed by the corresponding domain expert
- **Completeness**: Fully utilize the provided text and image information
- **Accuracy**: Pay special attention to technical detail interpretation in methodology and experimental sections
- **Depth**: The methodology design section must provide step-by-step in-depth technical analysis
- **Standardization**: The experimental analysis section strictly follows the three-part structure of "rationale-results-figures"
- **Clarity**: Clear report structure with coherent logic
- **Figure Correlation**: Ensure every technical point has clear figure support and references

---

**Please begin executing the in-depth collaborative analysis task of the academic paper according to the above requirements.**
```

## 🛠️ How to Use

1.  **Open a large language model dialog**
2.  **Copy the prompt**: Copy the complete core prompt from the above section and paste it into your language model's dialog box.
3.  **Prepare materials**:
    *   Convert your target paper (e.g., PDF file) to plain text (or directly upload the PDF if the platform handles PDFs well).
    *   (Optional but recommended) Note the numbers of key figures or formulas in the paper.
4.  **Interact with the language model**:
    *   In your chosen language model interface (e.g., Gemini Pro 2.5).
    *   Paste the **DeepRead-Agent-Prompt** as your first message and send it.
    *   Provide the paper's text and figure information in the same message (or directly provide the PDF).
5.  **Receive the analysis report**: The language model will follow the multi-agent framework and generate a detailed, well-structured report.

## 💡 Output Example

The following is a condensed example of an analysis report generated for the paper *《Respond to Change With Constancy: Instruction-Tuning With LLM for Non-I.I.D.Network Traffic Classification》*.

<details>
<summary><strong>Click to view analysis example</strong></summary>


Here is a comprehensive, in-depth analysis of the academic paper "Respond to Change With Constancy: Instruction-Tuning With LLM for Non-I.I.D. Network Traffic Classification," structured as a collaborative report from five specialized AI agents.

---

### 1. Core Keywords

1. **Encrypted Traffic Classification:**This is the primary task the paper addresses.The goal is to identify the application or service (e.g., "YouTube," "Botnet") from its network traffic, even when the content is encrypted and unreadable
2. **Non-I.I.D. (Independent and Identically Distributed):**This is the core challenge.It refers to situations where the test data follows a different statistical distribution than the training data.This is also referred to as **Out-of-Distribution (O.O.D.)**.
3. **Large Language Models (LLMs):**This is the core technology used to build the classification model.The paper leverages an LLM's powerful generalization and reasoning capabilities, which are learned from massive text datasets.
4. **Instruction Tuning:**This is the specific paradigm used to adapt the general-purpose LLM to the specialized, non-textual domain of network traffic. The model is "taught" the task using natural language instructions.
5. **Traffic Graph Representation:**This is the novel data representation proposed by the paper.Instead of analyzing network flows in isolation, the method constructs a graph that models the *interactions and relationships*(e.g., timing, concurrency) between multiple flows.

---

### 2. Research Background and Related Work

- **Current State and Trends:**Traffic classification is a fundamental technology for network management and cybersecurity, enabling tasks like quality of service assurance and attack detection888.However, the widespread adoption of encryption has made traditional methods like Deep Packet Inspection (DPI) ineffective.This has forced the field to shift towards machine learning-based approaches that analyze traffic metadata (like packet sizes and timings) rather than content.
- **Challenges:** The most significant challenge is **distribution drift**.Most academic models are trained and tested on data that is "independent and identically distributed" (I.I.D.).In the real world, this assumption is false.Network patterns constantly change due to application version updates, time-of-day variations, and other dynamic factors.This drift causes model performance to degrade rapidly.The standard solution—periodically retraining the model with new, labeled data—is extremely costly, time-consuming, and labor-intensive, as illustrated in Figure 1(a).
- **List of Related Research Work and Analysis:**
    - Statistical Methods (e.g., AppScanner, CUMUL): These methods rely on manually-crafted statistical features.Their limitation is that these features are brittle and must be re-engineered by experts as applications change.
    - Deep Learning Models (e.g., FS-Net, Deeppacket, GraphDApp): These methods use neural networks to automatically learn features from raw traffic.While more powerful, they typically require large amounts of labeled dataand are highly susceptible to learning "biased" representations that are overfitted to the training distribution and fail to generalize.
    - Pre-training Methods (e.g., ET-BERT, PERT): These models are pre-trained on large amounts of*unlabeled*traffic data, which improves their generalization.However, the paper notes they have not fully solved the O.O.D. challenge and are still constrained by their architectural design.
    - **Large Language Models (LLMs):**LLMs have shown remarkable generalization and "emergent abilities", which can be transferred to new domains via instruction tuning.However, their application to the unique, non-textual domain of network traffic remains a significant challenge.
- **Innovation and Importance:** This paper is the first to propose an **instruction-tuning framework with an LLM (named ETooL)** specifically for **O.O.D. encrypted traffic classification**.Its core innovation is aligning the structural, domain-specific knowledge of traffic (via graphs) with the general-purpose reasoning power of an LLM33.This approach aims to create a model that learns robust, *invariant*patterns3434and does not require costly retraining when new traffic distributions appear3535, as shown in Figure 1(b)36.

---

### 3. Core Scientific Problem

- **Problem Definition:** The core scientific problem is the **failure of existing encrypted traffic classifiers in the face of Out-of-Distribution (O.O.D.) data**.This "distribution drift"—caused by real-world changes like application updates or time shifts—invalidates the I.I.D. assumption that most models depend on, leading to a severe drop in classification accuracy.
- **Importance and Challenges:**This problem is critical for real-world network security. A model that cannot adapt to change is unreliable.As shown in Figure 1(a), the traditional "solution" is a costly, reactive cycle of **Re-Labeling** and **Re-Training**.This is not scalable and leads to models "forgetting" old patterns.The challenge is to build a model that possesses **robust generalization**—one that can "Respond to Change With Constancy" by learning the underlying, stable properties of traffic behavior rather than superficial, brittle features.
- **Limitations of Existing Methods:**
    1. **Feature Instability:**Most methods use features from single packets or single flows44.These features (e.g., specific packet sizes) are highly unstable and change with simple application updates.
    2. **Insufficient Generalization:** Models are designed to minimize error on a *known*training distribution.They lack the ability to extrapolate or transfer their knowledge to new, unseen distributions.

---

### 4. Methodology Design Details

The proposed method is **ETooL (Encrypted Traffic Out-of-Distribution Instruction Tuning with Large Language Model)**48.Its design, shown in Figure 249, consists of a novel graph representation module and a two-stage instruction tuning process.

#### 4.1 Overall Methodology Architecture

- **Overall Design Philosophy:** The core idea is that *interactions between flows*are a more robust and stable "fingerprint" than any single flow.The method first converts unstable, low-level traffic data into a stable, high-level **Traffic Relation Graph (TRG)**.Then, it uses a two-stage instruction-tuning process to "teach" a general-purpose LLM how to read, understand, and classify these traffic graphs.
- Architecture Component Analysis (Referring to Figure 2):
    1. **Traffic2Graph (Left):**This module is a feature-engineering pipeline.It extracts features (like datagrams and packet sizes) from raw PCAP tracesand uses a **Graph Constructor**56to build a **Traffic Relation Graph (TRG)**, which models the timing and concurrency (BURST) relationships between flows.
    2. **Graph Structural Instruction Tuning (Center):** This is the **first tuning stage**.It is a *self-supervised*phase designed to teach the LLM the "grammar" of traffic graphs.It uses a **BURST Graph Matching**task to force the LLM (ETooL) to align the graph's topology with the features of its nodes.
    3. **Traffic-Task Instruction Tuning (Right):** This is the **second tuning stage**.After the LLM understands *what a graph is* (from Stage 1), this stage fine-tunes it for the actual *classification task*.It learns to map a given traffic graph to a specific category (e.g., "YouTube"), making it robust to O.O.D. shifts.
- **Data Flow:**
    1. A raw `PCAP Trace`is split into individual `Session Flows`6.
    2. The `Flow Extractorn` extracts `Datagram` and `Packet Size`sequences for each flow.
    3. The `Flow2Graph`moduleassembles these flows into a `Traffic Relation Graph (TRG)` based on their timing and BURST properties.
    4. This TRG is fed to a `Traffic Graph Encoder`.
    5. **In Stage 1:** The LLM receives a `Human Instruction`, the encoded graph tokens, and a jumbled list of flow features.It is trained to output the *correct reordering*of the flows to match the graph structure.
    6. **In Stage 2:** The now "structurally-aware" LLM receives a new `Human Instruction` and the `Traffic Graph Tokens`.It is trained to output the correct `LLMs Response` —the classification label.
- **Innovative Architectural Features:** The primary innovation is the **dual-stage, parameter-efficient instruction tuning**. Unlike other methods, ETooL doesn't just classify traffic; it first*learns the structure*of traffic interaction in a self-supervised way (Stage 1) and then applies this structural knowledge to the classification task (Stage 2). This abstraction is the key to its O.O.D. robustness.

#### 4.2 Detailed Analysis of Key Steps

**Step 1: Traffic2Graph (Module)**

- **Objective and Function:** To transform a series of individual network flows into a single, comprehensive **Traffic Relation Graph (TRG)**.This graph represents the collaborative patterns and interaction properties between flows, which are more stable than single-flow features.
- **Input/Output:**
    - **Input:** A set of network flows $S = \{f_1, f_2, ..., f_n\}$collected over a period of time.
    - **Output:** A graph $G = (V, E)$, where nodes$V$are flows and edges$E$represent their relationships.
- Core Algorithm Mechanism (Algorithm 1):
    - **Working Principle:** The algorithm first sorts all flows by their start timestamp. It then iterates through them to define nodes and edges.
    - **Nodes (V):** Each network flow $f$becomes a node in the graph.Each node retains its low-level features, specifically the **datagram sequence** and the **directed packet size sequence**.
    - **Edges (E):**The graph contains two types of edges to capture flow relationships:
        1. **Burst Edges:** These connect concurrent flows *within*the same "flow-level BURST".A BURST is defined as a group of flows whose start times are all within a small time threshold $\gamma$(e.g., 1 second) of each other. (See Alg. 1, lines 6, 9-10).
        2. **Adjacency Edges:** These connect flows *between*different, adjacent BURST structures.The algorithm connects the last flow of the previous BURST to the first and last flows of the current BURST. (See Alg. 1, lines 12-14).
- **Technical Implementation Details:**
    - Flow Extractor: Extracts `Datagrams` (first 128 bytes, encoded as double-byte tokens like `(ee08, bf56, ...)`) and `Directed Packet Size Sequence` (e.g., `(+128, -74, -1020, ...)`where +/- indicates direction).
    - Flow2Graph: As shown in Algorithm 1, the algorithm maintains a temporary`BURST`list. As it iterates through sorted flows, it adds a flow to the current`BURST`if it's within the$\gamma$threshold. If a flow arrives*after*the threshold, the current`BURST`is finalized: internal "burst edges" are added, and "adjacency edges" are added to connect it to the`BURST_last`.
- **Innovation points:** This module explicitly models the **multi-flow collaborative construction of BURST structures**.This "flow-level BURST" concept captures a higher-level application behavior that is more robust to the minor feature drifts that plague single-flow models.

**Step 2: Graph Structural Instruction Tuning (Stage 1)**

- **Objective and Function:**To "inject the knowledge of traffic graph structure into the large language model".This is a **self-supervised** pre-tuning step that teaches the LLM to understand the *topology* of the TRG and associate it with the flow features of the nodes.
- **Input/Output:**
    - **Input:**A set of unlabeled TRGs, a textual instruction template, and the (disordered) flow features corresponding to the graph's nodes.
    - **Output:**A "structure-aware" LLM and a trained projection layer that aligns the graph embedding space with the LLM's token embedding space.
- **Core Algorithm Mechanism:**
    1. Traffic Graph Encoding Alignment: This first aligns the graph structure and flow feature "modalities" using contrastive learning (inspired by CLIP).A graph encoder $f_g$ (e.g., Graph Transformer) encodes the graph structure $G$ into a representation $H$, and a flow encoder $f_n$ (e.g., ET-BERT) encodes the node features $C$ into a representation $N$.A contrastive loss function (Eq. 4) is used to ensure that the representations for a matching graph and its features are "close" in the embedding space.
    2. BURST Graph Matching: This is the core self-supervised task.The LLM is given: (i) the encoded graph structure (represented by special tokens like `<graph_token>`), (ii) a textual instruction like "Please reorder the list of traffic data...", and (iii) the flow features for the graph's nodes, but in a *jumbled order*.
    3. **Objective:**The LLM's task is to "reorder the disordered BURST traffic feature representations by understanding the topological relationships between graph nodes". This forces it to learn the*meaning*of the graph's topology.
- **Technical Implementation Details:**
    - **Tuning Strategy:**This process is highly efficient.The parameters of the massive LLM and the graph encoders are **frozen**.Only a lightweight **projection layer**(which maps the graph encodings into the LLM's token space) is trained.
    - The special `<graph>`indicator in the instruction is replaced by the sequence of projected graph tokens (e.g., `<graph_begin>, <graph_token>1, ... <graph_end>`), allowing the LLM to process the graph structure as if it were part of the text prompt.
- **Innovation points:**This is a novel self-supervised task for the traffic domain.It solves the problem of how to teach an LLM, (which is trained on text), to understand complex, non-textual graph structures *without* needing labeled data and *without*expensive full-model retraining.

**Step 3: Traffic-Task Instruction Tuning (Stage 2)**

- **Objective and Function:** To adapt the "structurally-aware" LLM from Stage 1 to the final, downstream **encrypted traffic classification task**.
- **Input/Output:**
    - **Input:** Labeled TRGs (a graph $X$ and its class label $y$), and a task-specific instruction template (e.g., "Given the graph tokens... what traffic does this belong to?").
    - **Output:** The final ETooL model, fine-tuned to predict the traffic label $y$ for a given graph $X$.
- **Core Algorithm Mechanism:**This is a standard supervised fine-tuning phase, but framed as an instruction-following task.The model is given the traffic graph (via its token representation) and a question, and it is trained to generate the correct class label (e.g., "YouTube") as a natural language response.
- **Technical Implementation Details:**
    - **Tuning Strategy:**This stage is also parameter-efficient.The **full LLM backbone and the flow-graph encoder remain frozen**.The lightweight "structure-aware projector" trained in Stage 1 is inherited and fine-tuned, along with a new "lightweight task-specific classification head".
- **Innovation points:**By freezing the LLM, the method leverages the LLM's powerful, pre-trained reasoning capabilities while efficiently guiding them with the domain-specific structural knowledge learned in Stage 1. This combination enables strong generalization to O.O.D. tasks.

#### 4.3 In-Depth Analysis of Core Technologies

##### 4.3.1 Disciplinary Attribution and Theoretical Foundation

- **Primary Disciplinary Fields:**
    1. **Network Security / Network Traffic Analysis:**This is the core application domain.
    2. **Machine Learning / Deep Learning:**This is the central methodology.
    3. **Natural Language Processing (NLP):**The methodology is entirely built upon an LLM (Vicuna-7B-v1.5).
    4. **Graph Theory / Graph-based Learning:**The paper's core data representation is a graph (TRG), and it uses a Graph Transformer encoder and graph-based learning tasks.
- **Interdisciplinary Identification:This work is a strong example of interdisciplinary research, sitting at the intersection of**NLP(using LLMs for their generalization) and**Network Analysis**(a non-textual domain).It is inspired by recent research on applying LLMs to structured, non-textual data.It also integrates theories from **Contrastive Learning**(from computer vision) and **Self-Supervised Learning**.
- **Theoretical Foundation Framework:**
    - **Mathematical Foundation:**The graph construction is rooted in temporal-proximity clustering.The alignment module (Stage 1) is based on vector similarity metrics (dot product) and probabilistic loss functions (Cross-Entropy).
    - **Algorithm Theory:**
        1. **Transformer Architecture:**The base model is a Transformer (Vicuna), which uses self-attention mechanisms.
        2. **Transfer Learning / Domain Adaptation:**The entire methodology is a form of domain adaptation, transferring knowledge from the text domain (LLM pre-training) to the network traffic domain.
        3. **Instruction Tuning:**This is the specific mechanism for adaptation, guiding a pre-trained model with task-specific prompts rather than just re-training on new data.
        4. **Self-Supervised Learning (SSL):**Stage 1 (BURST Graph Matching) is an SSL task, as it generates its own "labels" (the correct node order) from unlabeled data.
        5. **Parameter-Efficient Fine-Tuning (PEFT):**The "freeze" strategy is a form of PEFT, which is crucial for adapting large models efficiently.
- **Methodological Genealogy:**This work evolves from two prior research lines: (1) pre-training for traffic (like ET-BERT) and (2) graph-based traffic analysis (like GraphDApp). It innovatively unifies these by replacing the domain-specific pre-training model with a general-purpose, pre-trained LLM, and then teaching the LLM to understand the graph representation.

##### 4.3.2 Core Algorithm Detailed Explanation

- **Core Algorithm:The**Dual-Stage Instruction Tuning paradigm.
- **Mathematical Foundation:** The alignment in Stage 1 is based on the **contrastive loss**in Equations 3 & 4. It calculates the similarity$\mathfrak{J}_i$between the encoded graph$H$and the encoded node-features$N$. The cross-entropy loss$CE(\mathfrak{I}_{i}, y)$then pushes the similarity of matching pairs towards 1 and all other (negative) pairs towards 0, effectively "aligning" the two representation spaces so the LLM can understand them jointly.
- **Theoretical Properties:The parameter-efficient "freeze" strategy is critical. It avoids**catastrophic forgetting, where a model fine-tuned on a new task forgets its original, powerful pre-trained knowledge. By freezing the LLM, it retains 100% of its reasoning capabilities while adding a small, specialized "adapter" (the projector) for the new task.
- **Applicable Scope:** This methodology is broadly applicable to any O.O.D. classification problem in a non-textual domain, provided the data can be meaningfully represented as a graph structure that captures invariant properties.

##### 4.3.3 Key Data Structures and Representations

- **Traffic Relation Graph (TRG):**This is the key data structure.It is a graph $G=(V, E)$ where nodes $V$represent individual flows (containing their datagram/packet size features)154and edges $E$represent temporal and functional relationships (bursting and adjacency)155.
- **Theoretical Advantages:**By abstracting away from individual, unstable flow features156and focusing on the *collaborative pattern*of flows, the TRG creates a more robust and stable "behavioral fingerprint".This structural fingerprint is more likely to remain consistent across application versions and time shifts, which is the core hypothesis for its O.O.D. robustness.

##### 4.3.4 Optimization Strategy Analysis

- **Parameter-Efficient Fine-Tuning (PEFT):** The primary optimization strategy is to **freeze the backbones**of both the LLM and the graph encoder.Only a small, lightweight projection layer and classification head are trained.
- **Theoretical Foundation:** This PEFT approach is based on the "adapter" hypothesis: that large pre-trained models already possess powerful, general-purpose representations. To adapt them to a new task, one only needs to train a small "adapter" module that maps the new data into the LLM's existing, well-understood representation space, rather than retraining the entire multi-billion parameter model.
- **Computational Gains:**As shown in Table VII, this strategy is highly effective.The full-parameter "tuning" method failed with an Out-of-Memory (OOM) error, while the "freeze" strategy ran successfully.It reduces the number of trainable parameters by **over 50 times**(6.6 Billion vs. 131.6 Million) and drastically cuts training time (e.g., Stage 2 training took 1h 38m vs. OOM).

##### 4.3.5 Robustness Design

- **Mechanism for O.O.D. Robustness:The robustness does*****not*****come from seeing O.O.D. data during training. It comes from the**choice of data representation (the TRG).The paper's core premise is that the *graph structure of flow interactions* is an **invariant property**of an application's behavior.
- **Implementation:**Stage 1 (Graph Structural Tuning) explicitly trains the LLM to understand this invariant structure. Stage 2 (Task Tuning) then trains the model to map this stable structure to a label.When a distribution shift occurs (e.g., app update), the low-level packet sizes might change, but the *interaction graph*(e.g., "one main request followed by 4 burst requests") remains the same. Since the model relies on this stable graph, its classification performance is robust to the shift.

#### 4.4 Method Integration Analysis

- **Module Collaboration:The**Traffic2Graphmodule acts as an expert feature engineer, creating a robust, structured representation. The**Graph Encoder**and**Flow Encoder**act as encoders, translating the graph and its node features into vector representations. The**Projector**(trained in Stage 1) is the critical "bridge" or "adapter" that maps the graph's vector language into the LLM's text-based vector language. The**LLM** (ETooL) acts as the central "brain" or reasoning engine, using its understanding of the graph to perform the final classification.
- **End-to-End Workflow:** (1) Input PCAP trace -> (2) TRG Construction -> (3) Graph/Node Encoding -> (4) Projection into LLM token space -> (5) LLM processes graph tokens + instruction text -> (6) LLM generates the final classification label.
- **Key Decision Logic:The key architectural decision is to**decouplethe learning process: (1) learn the*structure*of traffic (Stage 1), then (2) learn the*task* of classification (Stage 2). This prevents the model from relying on "shortcut" features (like a single packet size) that are not robust to O.O.D. changes.

---

### 5. Experimental Analysis

#### 5.1 Experimental Environment Setup

- **Dataset Description:**
    - APP53: A public dataset of 53 web apps, collected across different times and versions. This was used to create four tasks:
        - *I.I.D. tasks:* `EAC-T` (Same Time) and `EAC-V`(Same Version).
        - O.O.D. (zero-shot)tasks: `$EAC\Rightarrow T$` (Time Shift) and `$EAC\Rightarrow V$`(Version Shift), where the model is trained on one time/version and tested on another.
    - ISCX-Botnet170: A public dataset for malicious traffic (botnet) detection.The O.O.D. task (`$MSC\Rightarrow T$`) involves training on a subset of 7 botnet types and testing on traffic that includes new, unseen botnet types.
    - NETD: A **new dataset constructed by the authors**from the ISCX-VPN dataset.Its key feature is that it allows for *dynamically adjustable*distribution shifts by controlling "proportional bias" (changing the ratio of app components) and "compositional bias" (removing app components from the training set).
- **Evaluation Metrics Explanation:The paper uses four standard metrics:Accuracy (AC)**,**Precision (PR)**,**Recall (RC)**, andF1-Score (F1).The **Macro-Average**of these metrics is used to ensure that performance is not skewed by imbalanced classes.
- **Baseline Methods Introduction:**A comprehensive set of 7 state-of-the-art (SOTA) methods are used for comparison:
    - *Statistical:*AppScanner, CUMUL.
    - *Deep Learning:*Deep Fingerprinting (DF), FS-Net, GraphDApp.
    - *Pre-training:*PERT, ET-BERT.
- **Experimental Platform and Parameter Configuration:**
    - *Base LLM:*Vicuna-7B-v1.5.
    - *Hardware:*NVIDIA Tesla A800 GPUs (80 GB).
    - *Key Hyperparameters:* Learning rate of $2\times e^{-3}$, batch size of 2, max LLM input length of 2,048, and a BURST time threshold of 1 second.

#### 5.2 Detailed Experimental Analysis

**Experiment 1: Overall Performance Comparison (RQ1)**

- **Rationale for Experimental Design:**This experiment answers RQ1 by evaluating ETooL against the 7 baselines in both I.I.D. (standard) and O.O.D. (challenging) scenarios to prove its superior performance and generalization.
- **Experimental Results:**
    - **I.I.D. Scenarios (Table IV):**ETooL significantly outperforms all baselines even in the standard I.I.D. setting.On `APP53-TIME` (EAC-T), ETooL achieves a **93.19%** F1-Score, a **6.62%**absolute improvement over the best baseline, ET-BERT (86.57%).On `APP53-VERSION` (EAC-V), ETooL achieves **92.11%**, a **4.19%**improvement over ET-BERT.
    - **O.O.D. Scenarios (Table IV):**This is where ETooL's strength is clearest.When shifting to O.O.D. data, all baseline models suffer a *massive*performance drop193.For instance, on the `$EAC\Rightarrow T$`(Time Shift) task, ET-BERT's F1-Score plummets from 86.57% to 56.71%.In stark contrast, ETooL's score only drops to **74.88%**, which is **18.17%** *higher*than the best baseline.
    - **O.O.D. Malicious Traffic (Table V):In the challenging****`$MSC\Rightarrow T$`****(Multi-Class) task with unseen botnet types, ETooL achieves an F1-Score of**81.95%.This is a **12.08%**absolute improvement over the best baseline, ET-BERT (67.91%).
- **Corresponding Figures:** **Table IV**(APP53 results)and **Table V**(ISCX-Botnet results).

**Experiment 2: Ablation Study (RQ2)**

- **Rationale for Experimental Design:**This experiment answers RQ2by "dissecting" the ETooL model.It systematically removes each key component one-by-one to measure its individual contribution to the overall performance.
- **Experimental Results:**
    - **w/o Features (Models 1 & 2):** Removing `Raw Datagrams`causes a 4.02% average F1 drop, while removing `Packet Length`causes a 2.44% drop. This confirms both features are valuable.
    - **w/o Graph Structural Tuning (Model 3):** Removing the TRG representation and the Stage 1 tuning causes a *catastrophic* performance drop, with an average F1 reduction of **22.13%**. This is the most critical component.It proves that the **graph structure** and the **task of learning it (Stage 1)**are "critical for enabling ETooL to learn traffic context more effectively".
    - **w/o Large Language Model (Model 4):** Replacing the LLM with a standard Graph Transformer (trained from scratch) causes an average F1 drop of **12.84%**.This confirms that the "understanding and reasoning capabilities" of the pre-trained LLM provide a substantial benefit for O.O.D. generalization.
- **Corresponding Figures:** **Table VI**provides the quantitative data for this entire experiment.

**Experiment 3: Generalization Ability on NETD (RQ3)**

- **Rationale for Experimental Design:This experiment answers RQ3 by testing the model's robustness on the new, dynamically adjustable**NETD dataset.This allows for a more controlled study of how the models cope with *varying degrees*of distribution shift.
- **Experimental Results:**The experiment created four O.O.D. datasets (NETD-1 to NETD-4) with different types of bias.In all four scenarios, ETooL (the rightmost bar in each chart) achieves the highest F1-Score, significantly outperforming all baselines. The dotted line in the charts shows the I.I.D. performance.While ET-BERT is close to ETooL on I.I.D. data, its performance collapses under the Non-I.I.D. shifts, whereas ETooL's performance remains high, demonstrating "superior robustness and classification accuracy".
- **Corresponding Figures:** **Figure 4 (a-d)**provides a clear bar-chart visualization of these results, comparing all methods across the four NETD datasets.

**Experiment 4: Model Efficiency Study (RQ4)**

- **Rationale for Experimental Design:**This experiment answers RQ4by evaluating the *computational cost*(training time, memory, parameters) of the "freeze" (PEFT) strategy used by ETooL compared to a full-parameter "tuning" strategy.
- **Experimental Results:**
    - **Memory/Feasibility:** Full-parameter "tuning" failed with an **Out of Memory (OOM)**error, even on an 80GB A800 GPU.The "freeze" strategy (ETooL's method) ran successfully.
    - **Parameters:** The "freeze" strategy trains only **131.6 Million** parameters, versus the **6.6 Billion** required for full tuning—a **reduction of over 50x**.
    - **Time:**This parameter reduction leads to a massive speedup.For example, the Stage 2 task tuning took only **1 hour 38 minutes**with the "freeze" strategy, while the full-tuning approach was not even possible (OOM).
- **Corresponding Figures:** **Table VII** provides the exact numbers for training time, tuned parameters, and GPU memory usage.

**Experiment 5: Hyper-Parameter Analysis (RQ5)**

- **Rationale for Experimental Design:**This analysis answers RQ5by testing the model's sensitivity to its two most important, newly introduced hyper-parameters: the **BURST Time Threshold** (for graph creation) and the **Learning Rate**.
- **Experimental Results:**
    - **BURST Time Threshold:**The model was tested with thresholds from 0.3s to 1.5s.A threshold that is too small or too large degrades performance by incorrectly grouping flows.The experiment found that a threshold of **around 1.0 second**yielded the optimal F1-Score.
    - **Learning Rate:**The model was tested with rates from$2\times e^{-5}$to$2\times e^{-2}$.A rate of **$2\times e^{-3}$**provided the best performance.A higher rate was unstable, while a lower rate converged too slowly.
- **Corresponding Figures:** **Figure 5(a)** charts the performance vs. BURST Time Threshold.**Figure 5(b)** charts the performance vs. Learning Rate.

</details>

## 🤝 Contributing

All forms of contribution are welcome! The open-source community becomes more vibrant with every contribution. You can:

*   Fork this project
*   Create your feature branch
*   Commit your changes
*   Submit a Pull Request
*   Or submit bug reports and suggestions

## 🌟 Future Vision & DeepRead

`DeepRead-Agent-Prompt` is a powerful foundation. Our vision is to develop it into a more powerful and user-friendly tool.

**To provide a more convenient one-click experience, we are developing DeepRead.** It will offer the following advanced features:

*   **Knowledge Base Integration**: Automatically save and index papers you've analyzed.
*   **Continuous Optimization**: The system will always run on the latest and most powerful version of the prompt.
*   **Domain Knowledge Graph**: Build a knowledge graph of your target domain to help users quickly understand a research direction.

Stay tuned! Your support for this open-source project will accelerate the development of these advanced features.

## 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## 📧 Contact

Project Link: [https://github.com/li4oya/DeepRead-Agent-Prompt](https://github.com/li4oya/DeepRead-Agent-Prompt)  
Email: timevastillusion@gmail.com
