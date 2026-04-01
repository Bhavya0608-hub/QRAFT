# QRAFT: QLoRA Retrieval-Augmented Fine-Tuning for Causal Span Extraction in Financial Documents

📄 Research Paper: [View PDF](./QRAFT-FinCausal-2026.pdf)

---

## 📌 Overview

Understanding *why* financial outcomes occur is critical for financial analysis, risk assessment, and intelligent automation.

This project presents **QRAFT**, a system developed for the **FinCausal 2026 Shared Task**, focused on extracting **causal spans** from financial documents using modern **LLM fine-tuning and retrieval techniques**.

---

## 🧠 Key Highlights

* Fine-tuned **Qwen2.5-4B-Instruct** using **QLoRA** on 2,000 financial instances
* Integrated **TF-IDF based retrieval** to guide model predictions
* Designed a **verbatim span extraction pipeline** to reduce hallucination
* Achieved **4.76 / 5 LLM-as-a-judge score**
* Ranked **4th out of 9 teams** on the official leaderboard

---

## ⚙️ Methodology

### 1. Instruction Formatting

Training data is converted into **ChatML format** to align with instruction-tuned LLM behavior.

### 2. QLoRA Fine-Tuning

* 4-bit quantization
* Low-rank adapters (LoRA)
* Efficient domain adaptation with limited compute

### 3. Retrieval-Augmented Inference

* TF-IDF cosine similarity retrieves the most relevant sentence
* Retrieved context improves answer grounding

### 4. Deterministic Decoding

* Greedy decoding ensures stable and verbatim outputs

---

## 📊 Results

| Metric         | Score             |
| -------------- | ----------------- |
| LLM-as-a-judge | **4.76 / 5**      |
| Rank           | **4th / 9 teams** |

---

## 📂 Dataset

* FinCausal 2026 (English Subtask)
* 2,000 training instances
* 500 test instances
* Task: Extract causal spans from financial documents

---

## ⚠️ Limitations

* Long causal spans may introduce boundary errors
* Multi-hop causal reasoning remains challenging
* Limited discourse-level understanding

---

## 🔮 Future Work

* Discourse-aware models for complex reasoning
* Dense retrieval for improved semantic matching
* Enhanced span extraction for long contexts

---

## 👨‍💻 Authors

* **Bavya Sarda** – Galgotias University
* Pulkit Chatwal – RGIPT
* Sonal Dabral – Sony Research India

---

## 📢 Publication Status

✅ Accepted for publication (to appear in 2026)

---

## 🛠 Tech Stack

* Python
* PyTorch
* Transformers
* QLoRA
* Qwen LLM
* TF-IDF Retrieval

---

## ⭐ Support

If you find this work useful, consider giving it a ⭐ on GitHub!

---

## 📬 Contact

📧 [bhavyasarda19@gmail.com](mailto:bhavyasarda19@gmail.com)
🔗 [LinkedIn](https://linkedin.com/in/bavya-sarda-8a5011270)
