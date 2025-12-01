# VertexDraft - Deep Dive Analyst

## Project Title
**Deep Dive Analyst: Multi-Agent AI Research System with Human-in-the-Loop Control**

---

## Problem Statement

Researchers and decision-makers often face two critical challenges when conducting in-depth topic analysis:

1. **Information Overload**: Too much raw data without clear direction on what matters most
2. **Lack of Control**: AI systems that generate generic reports without incorporating user priorities

Traditional research tools either dump massive amounts of unfiltered information or create rigid, one-size-fits-all reports that miss the specific insights users actually need.

---

## Solution

VertexDraft solves this with a **multi-agent AI system** that puts humans in control:

### Architecture
- **Agent A (Hunter)**: High-creativity research agent (Gemini 2.5 Pro, temp=0.9) that discovers comprehensive data, statistics, players, and trends
- **Agent B (Writer)**: High-precision synthesis agent (Gemini 2.5 Flash, temp=0.2) that creates executive reports tailored to user needs

### Human-in-the-Loop Workflow
1. **User Control Point 1**: Choose any research topic
2. **Automated Research**: Agent A conducts comprehensive investigation
3. **User Control Point 2**: Review findings and direct focus (e.g., "focus on costs" or "focus on technical challenges")
4. **Targeted Report**: Agent B generates a customized executive summary prioritizing your specified area

### Key Features
✅ **Sequential Multi-Agent Pipeline**: Specialized agents for research vs. synthesis  
✅ **Human Checkpoints**: User directs the analysis at critical stages  
✅ **Adaptive Intelligence**: System responds to user priorities in real-time  
✅ **Professional Output**: Data-driven executive reports ready for decision-makers

---

## How to Run

### Prerequisites
- Python 3.8+
- Google AI Studio API key (free tier available at [aistudio.google.com](https://aistudio.google.com))

### Installation & Execution

```bash
# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook VERTEXDRAFT.ipynb
```

### Step-by-Step Instructions for Judges

1. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Open Notebook**
   - Launch: `jupyter notebook VERTEXDRAFT.ipynb`
   - Or open directly in VS Code with Jupyter extension

3. **Configure API Key** (Cell 2)
   - Replace `GOOGLE_API_KEY` with your API key
   - Get free key at: https://aistudio.google.com/app/apikey

4. **Run Cells in Order**
   - Cell 1: Install packages
   - Cell 2: Configure API
   - Cell 3: Setup agents
   - Cell 4: **Start interactive workflow**

5. **Interact with the System**
   - When prompted, enter a research topic (e.g., "quantum computing", "sustainable aviation fuel")
   - Review Agent A's research findings
   - When prompted again, specify your focus (e.g., "focus on commercial viability", "focus on technical barriers")
   - Receive your customized executive report

### Example Session
```
📌 What topic would you like to research? electric vehicle batteries

🔍 Researching: electric vehicle batteries...
[Agent A presents comprehensive research]

⏸️  HUMAN CHECKPOINT
👤 What should the final report focus on? cost reduction strategies and supply chain

✍️  Writing report focused on: cost reduction strategies and supply chain...
[Agent B delivers targeted executive summary]
```

---

## Technical Details

- **Framework**: Google Generative AI (Gemini 2.5 models)
- **Agent A**: `gemini-2.5-pro` with temperature=0.9 for creative research
- **Agent B**: `gemini-2.5-flash` with temperature=0.2 for precise synthesis
- **Language**: Python 3.8+
- **Dependencies**: See `requirements.txt`

---

## Competition Compliance

✅ Multi-agent architecture (2+ agents)  
✅ Human-in-the-loop control mechanism  
✅ Sequential workflow with clear phases  
✅ Demonstrates autonomous research + user-directed synthesis  
✅ Production-ready code with clean interface
