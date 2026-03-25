# 🛡️ LLM Automated Red Teaming & Security Audit

This project demonstrates an **Automated Vulnerability Scan** on Large Language Models (LLMs) using the **Giskard Framework**. The goal is to identify security flaws like **Prompt Injection**, **Hallucination**, and **Toxicity** in AI models.

## 🎯 Project Overview
In this project, I performed a **Red Teaming** operation on a **GPT-2 model** (via Hugging Face) to see how it handles adversarial inputs.

### 🔍 Key Findings
- **Major Issue Detected:** **Control Character Injection (`\x08`)**.
- **Impact:** By injecting long sequences of control characters, I was able to manipulate the model's output, causing it to produce unexpected and repetitive data (e.g., `000000`).
- **Fail Rate:** 0.500 (50% Success Rate), highlighting a significant security gap in basic LLM architectures.

## 🛠️ Tools Used
- **Python** 🐍
- **Giskard** (Security Audit Framework)
- **Transformers / Hugging Face** (Model Hosting)
- **Pandas** (Data Handling)

## 🚀 How to Run the Project
1. Clone the repository.
2. Install dependencies: `pip install "giskard[llm]" langchain transformers`
3. Run the attack script: `python attack.py`
4. Open the generated `attack_report.html` in your browser.

**Disclaimer:** This project is for educational and security research purposes only.
