# QRAFT: QLoRA Retrieval-Augmented Fine-Tuning for Causal Span Extraction in Financial Documents

📄 Research Paper: [View PDF](QRAFT__QLoRA_Retrieval_Augmented_Fine_Tuning_for_Causal_Span_Extraction_in_Financial_Documents...pdf)

---

# QRAFT: QLoRA Retrieval-Augmented Fine-Tuning for Causal Span Extraction in Financial Documents

📄 Research Paper: [View PDF](./QRAFT-FinCausal-2026.pdf)

---

## 📌 Overview

Financial documents do not just report outcomes — they explain **why those outcomes occur**. Extracting this causal reasoning automatically is a challenging task due to domain complexity, implicit relationships, and linguistic nuance.

This project presents our system for the **FinCausal 2026 Shared Task (English Subtask)**, where the objective is to extract **verbatim causal spans** from financial text in response to abstractive causal questions.

Our approach is based on the idea that a **well-adapted compact model**, combined with **targeted retrieval**, can outperform larger but unfocused systems.

---

## 🧠 Approach

Our system consists of three core components:

### 🔹 1. Instruction-Tuned Fine-Tuning

* Reformatted all training data into **Qwen ChatML format**
* Fine-tuned **Qwen2.5-4B-Instruct** using **QLoRA**
* Enabled efficient domain adaptation with limited computational resources

### 🔹 2. Retrieval-Augmented Inference

* Applied **TF-IDF cosine similarity** to retrieve the most causally relevant sentence
* Provided an explicit **local relevance signal** before generation

### 🔹 3. Verbatim Span Extraction

* Enforced strict extraction from source text
* Used **greedy decoding** for deterministic, source-grounded outputs
* Reduced hallucination and ensured faithful predictions

---

## 📊 Results

Under the official **LLM-as-a-judge evaluation framework** (semantic adequacy scoring):

* ⭐ **Score:** 4.76 / 5
* 🏆 **Rank:** 4th out of 9 teams

This evaluation prioritizes **semantic correctness over lexical overlap**, making it a more realistic measure of causal reasoning quality.

---

## 🔍 Key Insights

* Compact models can achieve strong performance when **fine-tuned on domain-specific data**
* Instruction formatting significantly improves **verbatim extraction behavior**
* Lightweight retrieval methods like TF-IDF remain highly effective for **grounding generation**
* LLM-as-a-judge evaluation provides a **better signal than exact match metrics**

---

## ⚠️ Limitations

* Long causal spans may introduce boundary inaccuracies
* Multi-hop causal chains remain difficult to resolve
* Limited discourse-level reasoning capability

---

## 🔮 Future Work

* Develop **discourse-aware models** for multi-hop causal reasoning
* Explore **dense retrieval techniques** for improved semantic matching
* Improve extraction accuracy for complex, long-span answers

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
* PyTorch / Transformers
* QLoRA
* Qwen LLM
* TF-IDF Retrieval

---

## 📬 Contact

📧 [bhavyasarda19@gmail.com](mailto:bhavyasarda19@gmail.com)
🔗 [LinkedIn]([https://linkedin.com/in/bavya-sarda-8a5011270](https://leetcode.com/u/bavya_sarda/))

---

## ⭐ Support

If you found this work useful, consider giving this repository a ⭐


## 📬 Contact

📧 [bhavyasarda19@gmail.com](mailto:bhavyasarda19@gmail.com)
🔗 [LinkedIn]([https://linkedin.com/in/bavya-sarda-8a5011270](https://leetcode.com/u/bavya_sarda/))
