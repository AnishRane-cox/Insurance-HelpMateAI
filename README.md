
# 🧠 RAG-Based Insurance Policy Chatbot

An end-to-end Retrieval-Augmented Generation (RAG) system built to query complex insurance documents. Combines OpenAI embeddings, ChromaDB for vector search, a cross-encoder for reranking, and GPT-3.5 for grounded, context-aware answers.

---

## 🔍 Features

- 📄 PDF-based policy ingestion with text + table extraction (`pdfplumber`)
- 🧱 Sliding-window chunking with metadata tagging
- 🔎 Semantic search using OpenAI `text-embedding-ada-002`
- 🧠 Cross-encoder reranking (`ms-marco` / `stsb-roberta-base`)
- 🤖 GPT-3.5-turbo LLM response generation using retrieved chunks only
- 🔁 ChromaDB-powered persistent cache to reduce redundant calls
- 🛡️ Hallucination-resistant by enforcing grounded generation
- 📸 Screenshot support for search and answer stages (for reporting)

---

## 📂 Project Structure

```
├── notebooks/
│   └── main_pipeline.ipynb        # End-to-end RAG pipeline
├── data/
│   └── Principal-Sample-Life-Insurance-Policy.pdf
├── screenshots/
│   └── query1_search.png
│   └── query1_answer.png
│   └── ...
├── RAG_Insurance_Chatbot_Documentation.docx
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/insurance-rag-chatbot.git
cd insurance-rag-chatbot
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up Environment

Set your OpenAI API key in your environment:

```bash
export OPENAI_API_KEY="your-api-key-here"
```

### 4. Run the Notebook

Open `main_pipeline.ipynb` and run each cell to:
- Load PDF
- Generate embeddings
- Query and rerank results
- Generate grounded answers

---

## 💬 Example Queries

- _“What is the claim process for nominees of the policy?”_
- _“How is the policy surrender value calculated, and when is it applicable?”_
- _“Can a member convert their group life insurance to an individual policy after termination?”_

---

## 📄 License

This project is licensed under the MIT License.

---

## ✨ Acknowledgments

- [OpenAI](https://openai.com)
- [Sentence Transformers](https://www.sbert.net/)
- [ChromaDB](https://docs.trychroma.com)
- [pdfplumber](https://github.com/jsvine/pdfplumber)
