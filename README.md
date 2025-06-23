# RAG_Bench_marking_Implementation_of_LLM-s
# RAGBench – Gradio Interface for Benchmarking Retrieval-Augmented Generation (RAG) Systems

This project implements an interactive Gradio-based evaluation interface for [**RAGBench**](https://arxiv.org/abs/2407.11005), a large-scale, explainable benchmark designed to assess Retrieval-Augmented Generation (RAG) systems. It enables researchers and developers to evaluate LLM-based RAG pipelines using fine-grained, human-annotated metrics like **Groundedness**, **Faithfulness**, and **Coverage**.

---

## 📚 About RAGBench

**RAGBench** is the first benchmark that provides explainable, domain-specific evaluations of RAG systems, going beyond simple answer correctness. It includes over **100,000 QA examples** curated from **five real-world domains**, each with labeled answers and retrievals to test LLM reliability in practical settings.

### ✨ Evaluation Dimensions

| Metric         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| **Groundedness** | Measures whether the generated answer is directly supported by the retrieved context |
| **Faithfulness** | Assesses whether the model introduces hallucinated or unsupported information        |
| **Coverage**     | Evaluates how completely the answer captures all necessary points from the context   |

---

## 🗂 Dataset Overview

RAGBench contains QA data from the following **five real-world domains**:

- 📘 Technical Manuals  
- 🏦 Financial Documents  
- ⚖️ Compliance and Legal Texts  
- 📚 Academic and Scientific Sources  
- 🌐 Open-domain QA  

Each sample in the dataset includes:
- A user query
- Retrieved documents
- An LLM-generated answer
- Human-annotated evaluations on the above dimensionss

---

## 💻 Gradio Interface

The interactive app includes:

### 🔹 Section 1: Evaluate a RAG Pipeline
- Choose:
  - ✅ Dataset
  - 🔎 Embedding Model (e.g., `text-embedding-ada-002`)
  - 💬 QA Model (e.g., `gpt-3.5-turbo`, `Mistral`)
- Click **“Get Metrics”** to view:
  - Groundedness
  - Faithfulness
  - Coverage

### 🔹 Section 2: Custom Q&A (Live Testing)
- Input your own question
- Retrieve and display top context passages
- Generate an answer using the QA model

---
## 🚀 Usage
### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-repo/RAG_Bench_marking_Implementation_of_LLM-s.git
cd RGB_Benchmarking
```

### 2️⃣ RUN the ipynb file

Run all the cells in the ipynb file so that you can use gradio app to evaluate in the last cell.


### 3️⃣ Run the Evaluation

Initially please add your own API Keys of the LLM models in the config.ini file. Select the paramaters and model to evaluate the model will automatically fetch the data set required form the data config folder that is placed in the drive if the data config file dosen't exist in the drive please download and upload in the drive. Also select the input parameters in the gradio app.


## 📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

---

For more details, refer to the original research paper: [RAGBench: Explainable Benchmark for Retrieval‑Augmented Generation Systems](https://arxiv.org/pdf/2407.11005)

