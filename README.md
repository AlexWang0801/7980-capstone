# AI-generated Email Evaluation System

This project evaluates AI-generated emails using a three-layer framework:
1. **Layer 1 Pre-screening** — Remove low-quality emails with fundamental issues
2. **Layer 2 Intrinsic Evaluation** — Multi-dimensional evaluation (CTA, personalization, human-likeness, Instruction Adherence)
3. **Layer 3 Aggregation & Ranking** — Summary and comparison of results

---

## 🚀 Features

✔ Pre-filter low language quality or hallucinated content  
✔ Multi-dimensional scoring across 6 evaluation criteria  
✔ Tiered ranking and export for downstream decisions  
✔ Low latency & low inference cost   
✔ CSV result output for easy analysis

**Evaluation Dimensions:**
1. Hallucination (filtering — pass/fail)
2. Language Quality & Coherence
3. Instruction Adherence
4. CTA Quality
5. Personalization
6. Human-likeness

Scores use a 1–5 scale and are aggregated into a final intrinsic score.

---
## 🧱 Project Structure

project/   
│── JSON/  
│ └── input_emails.json  
│── CODE/  
│ ├── Prompt_Engineering  
│ │ ├── few_shot.ipynb  
│ │ ├── test_CoT.ipynb  
│ │ ├── test_One_Shot.ipynb  
│ ├── Test  
│ │ ├── Copy_of_email_system_version_2.ipynb  
│ │ ├── model_test_version.ipynb  
│ │ ├── score10_version.ipynb  
│ ├── email_evaluation_system.ipynb   
└── README.md  



---

## 🛠️ Setup

### **1️⃣ Create environment (optional)**
```bash
python3 -m venv venv
source venv/bin/activate        # macOS / Linux
venv\Scripts\activate           # Windows PowerShell
```
Ensure your OpenAI / OpenRouter API key is configured:
```bash
export OPENAI_API_KEY="your_key_here"
# or:
export OPENROUTER_API_KEY="your_key_here"
```

## ▶️ Usage
Run the full evaluation pipeline:
```bash
Project/CODE/email_evaluation_system.ipynb
```
Additional output:  
✔ CSV result  
✔ Score distributions  
✔ Runtime cost summary  

## 🔍 System Overview
```mermaid
flowchart TD
    A[[📨 Input<br/>AI-generated Emails]]
    B[[🚫 Layer 1: Filtering & Qualification<br/>Hallucination Check + Language Quality Threshold]]
    C[[🧠 Layer 2: Intrinsic Evaluation<br/>CTA · Personalization · Human-Likeness · Instruction Adherence]]
    D[[📊 Layer 3: Score Aggregation & Bucketing<br/>Top · Medium · Low]]
    E[[📁 Export Results<br/>JSON + CSV + Stats]]

    A --> B --> C --> D --> E




