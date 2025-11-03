# LLM Evaluation Notebook

This notebook demonstrates **how to evaluate text outputs** from large language models (LLMs) using both **classical** and **embedding-based** metrics.

---

## Overview

LLM evaluation can be quantitative when you compare generated text to reference ground truth.  
This notebook includes implementations for:

| Metric Type | Library | Description |
|--------------|----------|-------------|
| **BLEU** | `nltk.translate.bleu_score` | n-gram precision metric |
| **ROUGE** | `rouge_score` | recall-oriented overlap metric |
| **BERTScore** | `bert_score` | contextual embedding similarity using a pretrained transformer |

---

## Features
- Input data: `reference` and `generated` text pairs (from CSV or in-notebook lists)
- Compute **BLEU, ROUGE-L, and BERTScore**
- Aggregate metrics (mean, std, percentile)
- Easy extension for LLM benchmarks (e.g., GPT, Claude, Gemini outputs)

---

## Usage

```bash
# 1) Create and activate virtual environment
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

# 2) Install dependencies
pip install -r requirements.txt

# 3) Launch notebook
jupyter lab   # or: jupyter notebook

# 4) Git clone
git clone https://github.com/Joe-Naz01/llm_evaluate.git
cd llm_evaluate
