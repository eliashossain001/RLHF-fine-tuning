# LLM Fine-Tune & Preference Optimization

This repository contains two key components for training and optimizing Large Language Models (LLMs):

- ✅ **Supervised Fine-Tuning (SFT)** using GPT-4-style models for math problem-solving
- ✅ **Direct Preference Optimization (DPO)** to further align LLM behavior with preference data, using models such as Qwen



---

## 🚀 Fine-Tuning GPT-4 for Math Problem Solving

This section focuses on fine-tuning a GPT-style model on a **math reasoning task** using a large dataset of structured QA pairs.

### 📚 Dataset Details

We used a publicly available dataset containing **395,000 math questions** with step-by-step solutions. Each entry includes:

- `original_question`: the input math problem  
- `response`: a detailed, multi-step solution

The questions span a wide range of topics — from basic arithmetic to advanced algebra and functional equations — making it a strong benchmark for testing **LLM mathematical reasoning**.

### 🛠 Technologies
- 🤖 Model: GPT-4-style (any causal LM)
- 📖 Framework: [Unsloth](https://github.com/unslothai/unsloth) for fast fine-tuning
- 💾 Tokenizer: AutoTokenizer from Hugging Face
- 📊 Evaluation: Sample generations and accuracy on held-out test sets

---

## 🎯 Direct Preference Optimization (DPO)

The DPO section focuses on **optimizing LLM outputs** beyond standard SFT by learning from **preference pairs**. This allows models to choose preferred completions aligned with user expectations.

### 🧪 Current Setup

- 🔍 Model: [`Qwen/Qwen2.5-0.5B-Instruct`](https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct)
- ⚙️ Optimizer: DPOTrainer (from `trl` or equivalent)
- 🔁 Preference Data: Synthetic titles and step-by-step completions
- 📁 Notebooks include:
  - Data generation
  - Dataset formatting
  - Fine-tuning with DPO
  - Evaluation and visualization

### 💡 Future Work

We aim to:
- Experiment with larger models (e.g., `Qwen-1.8B`, `LLaMA-3`, `Mixtral`)
- Compare SFT-only vs SFT+DPO pipelines
- Explore human preference data injection

---

## 🧰 Requirements

```bash
pip install -r requirements.txt


