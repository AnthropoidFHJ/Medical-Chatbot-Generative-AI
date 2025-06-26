
## MediBot: A Medical AI Chatbot ##

 **Project Overview**

**MediBot** is a personalized, privacy-preserving Medical Q&A chatbot built to assist users with reliable answers from curated medical documents. MediBot runs on Flask with a cutting-edge retrieval-augmented generation (RAG) pipeline powered by **LLaMA3-70B via Groq API**. The system supports real-time document understanding using **LangChain**, **HuggingFace Embeddings**, and **Pinecone** for semantic search.

---

🔍 **How It Works**

1. **Custom Data Preparation**

   * Medical PDF documents are uploaded and parsed using LangChain loaders.

2. **Semantic Chunking & Embedding**

   * Text data is divided into manageable semantic chunks.
   * Chunks are embedded using HuggingFace's `all-MiniLM-L6-v2` model.

3. **Vector Storage in Pinecone**

   * Embeddings are stored in **Pinecone Vector DB**.
   * A semantic index is built for similarity-based search.

4. **Real-Time Query Flow**

   * User submits a query via the Flask front-end.
   * Query is embedded and searched in the Pinecone database.
   * Top results are processed using LLaMA3 and returned as human-readable answers.

---

🔧 **Key Technologies**

* **Frontend**: Flask + Custom HTML/CSS Chat UI
* **Backend**: Python (LangChain, Groq API, Pinecone, HuggingFace)
* **Vector Database**: Pinecone
* **Embedding Model**: all-MiniLM-L6-v2
* **LLM**: Groq (LLaMA3-70B)

---

📦 **Setup Instructions**

1. **Clone the Repository**

```bash
git clone https://github.com/AnthropoidFHJ/Medical-Chatbot-Generative-AI
```

2. **Create the Conda Environment**

```bash
conda create -n MediBot python=3.10 -y
```

```bash
conda activate MediBot
```

```bash
conda create -n MediBot python=3.10 -y
```

```bash
conda activate MediBot
```

3. **Install Requirements**

```bash
pip install -r requirements.txt
```

4. **Create Folder Structure**

```bash
python folder_Structure.py
```

5. **Configure Environment Variables**
   Create a `.env` file in the root directory and add:

```env
PINECONE_API_KEY="Your_actual_Pinecone_Key"
GROQ_API_KEY="Your_actual_Groq_Key"
```

6. **Run the Application**

```bash
python app.py
```

Visit: [http://localhost:8080](http://localhost:8080)

---

⚙️ **Workflow Summary**

```
PDFs → Text → Chunks → Embeddings → Pinecone Index
                                        ↑ ↓
                Query Embedding →  Knowledge Base
                                        ↓
                                    Ranked Result → Groq LLM → Answer
```

---

🌟 **Future Enhancements**

* Add **Streamlit UI** for improved accessibility
* Implement **Caching Layer** for repeated questions
* Integrate **TTS (Text to Speech)** for accessibility
* Expand dataset to include more domain-specific materials

---

🧪 **Deployment History**

* **Prototype**: Developed in Jupyter Notebook
* **CI/CD**: Migrated to VS Code, folder structure initialized via `folder_structure.py`
* **GitHub**: Linked with GitHub for version control
* **AWS**: Deployable to cloud for scale

---

**This project was developed with a strong intent to help users access accurate, AI-powered medical information quickly and securely.**

---

*Author: Ferdous Hasan*
---
*Date: 26 June 2025*
---