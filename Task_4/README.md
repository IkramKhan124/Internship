# 🏥 General Health Query Chatbot

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Model: Mistral-7B](https://img.shields.io/badge/Model-Mistral--7B--Instruct-green)](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.3)
[![GPU: T4](https://img.shields.io/badge/GPU-T4-orange)](https://colab.research.google.com/)

> **AI-Powered Health Education Assistant with Advanced Safety Filters**

---

## 🎯 Task Objective

The project aims to build a **safe, helpful AI chatbot** that answers general health-related questions using open-source Large Language Models (LLMs).  

**Key Goals:**
- Provide accurate general health information
- Prevent harmful advice through multi-layer safety filters
- Offer educational insights while remaining free and open-source
- Modular, well-documented Python code for easy reuse

---

## 📊 Dataset Used

Instead of conventional training datasets, this project uses **engineered prompts and test cases**:

1. **Safety Filter Database**
   - 14 critical emergency keywords (e.g., chest pain, heart attack, stroke)
   - 5 regex patterns for dosage, medication changes, diagnosis requests, and treatment instructions

2. **Few-Shot Examples**
   - Curated examples to ensure consistent response formatting
   - Example topics: sore throat remedies, paracetamol safety for children

3. **Test Query Dataset**
   - 8 queries covering:
     - General health info
     - Emergency detection
     - Safety enforcement
     - Wellness/edge cases

---

## 🤖 Models Applied

**Primary Model:** [Mistral-7B-Instruct-v0.3](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.3)  

| Attribute          | Specification                                |
|------------------ |---------------------------------------------|
| Model Name         | `mistralai/Mistral-7B-Instruct-v0.3`       |
| Parameters         | 7 billion                                   |
| Architecture       | Transformer with Grouped-Query Attention    |
| Context Length     | 32k tokens                                  |
| License            | Apache 2.0                                  |

**Optimization Techniques:**
- **4-bit Quantization (NF4):** ~70% memory reduction
- **Double Quantization:** Extra compression (~0.4 bits/param)
- **Gradient Checkpointing:** Trade compute for ~30% memory savings
- **Flash Attention 2:** Faster inference

**Inference Configuration:**
```python
{
  "max_new_tokens": 512,
  "temperature": 0.7,
  "top_p": 0.9,
  "repetition_penalty": 1.1,
  "device": "cuda"
}
