# llama3-medmcqa-finetuning

Sure! Here's the full `README.md` content, ready for you to copy and paste:

---


# 🧠 Fine-Tuning LLaMA3 on MedMCQA – Final Project

This project demonstrates how to fine-tune the `meta-llama/Llama-3.1-8B-Instruct` model using the [MedMCQA](https://huggingface.co/datasets/openlifescienceai/medmcqa) dataset. The notebook covers preprocessing, model preparation, training, and evaluation of performance on medical multiple-choice QA tasks.

---

## 📁 Project Structure



📦 FineTuning\_FinalProject\_AmirKhier


┣ 📜 FineTuning\_FinalProject\_ِAmirKhier.ipynb

┣ 📄 README.md


┗ 📄 requirements.txt



---

## 🚀 Objectives

- Fine-tune `LLaMA3` on a domain-specific medical QA dataset.
- Preprocess MedMCQA to include explanations (`exp` field).
- Train and evaluate model performance on validation data.
- (Optional) Convert model for deployment or inference (e.g., to GGUF).

---

## 🧬 Dataset

- **Name**: MedMCQA
- **Source**: Hugging Face – [openlifescienceai/medmcqa](https://huggingface.co/datasets/openlifescienceai/medmcqa)
- **Description**: A large-scale multiple-choice question answering dataset for medical domain applications.

---

## 🧰 Tech Stack

- Python
- Hugging Face Transformers & Datasets
- LLaMA3 (Meta)
- PyTorch (backend)
- Google Colab (A100 GPU)

---

## 🏁 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/fine-tuning-llama3-medmcqa.git
cd fine-tuning-llama3-medmcqa
````

### 2. Install required packages

```bash
pip install -r requirements.txt
```

Or manually install the core dependencies:

```bash
pip install transformers datasets accelerate peft bitsandbytes
```

### 3. Run the notebook

Use Google Colab or a local Jupyter environment (GPU recommended):

```bash
jupyter notebook FineTuning_FinalProject_ِAmirKhier.ipynb
```

---

## ⚙️ Training Overview

* **Model**: `meta-llama/Llama-3.1-8B`
* **Tokenizer**: Adjusted for `max_length=512`, truncation, and padding.
* **PEFT**: Parameter-efficient fine-tuning applied.
* **Loss Function**: Cross-entropy over multiple-choice answers.
* **Evaluation**: Accuracy on `validation` split.

---

## ✅ Results


| Metric    | Value |
| --------- | ----- |
| Train Loss| 1.443 |
| Eval Loss | 1.551 |

---


## 📦 Export / Deployment (Optional)

* Convert model to GGUF format for use with llama.cpp or local inference engines.
* Push fine-tuned model to [Hugging Face Hub](https://huggingface.co/) using:

```python
model.push_to_hub("your-username/llama3-medmcqa")
```

---

## ✍️ Author

* **Amir Khier** – [LinkedIn](https://www.linkedin.com/in/amir-khier-9b8007198/) | [GitHub](https://github.com/amirkhier)

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgments

* Meta for LLaMA 3
* Hugging Face for the MedMCQA dataset and `transformers` ecosystem
* OpenLifeScienceAI and Google Colab for providing the compute backbone
