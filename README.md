#  Wikipedia QA System using RAG, LangChain, and OpenAI

This project builds a smart **Question Answering (QA) system** that can search and extract relevant information from **Wikipedia articles** using the power of **Retrieval-Augmented Generation (RAG)**. Think of it as a specialized search engine that answers questions like ChatGPT, but it's focused on Wikipedia and uses modern AI tools like **LangChain**, **OpenAI embeddings**, and **ChromaDB**.

---

##  What It Does

- Converts Wikipedia text into **searchable vector embeddings**
- Stores those vectors in a **high-speed vector database (ChromaDB)**
- Retrieves top matching content using a **multi-stage retriever pipeline**
- Generates human-like answers using **OpenAI’s GPT models**

---

##  Why It’s Important

Searching through massive text datasets (like Wikipedia) is hard with traditional keyword-based methods. This project uses:

- **Embeddings**: turns text into high-dimensional vectors to capture meaning.
- **Vector databases**: allows fast similarity search across large volumes of documents.
- **RAG**: combines retrieval and generation for contextual, accurate answers.

---

##  What Was Implemented

- ✅ Downloaded and parsed Wikipedia data
- ✅ Used **OpenAI’s `text-embedding-3-small`** model for embedding articles
- ✅ Stored the vectors in **ChromaDB**
- ✅ Built a smart retrieval chain using **LangChain**
  - Similarity search
  - LLM-based filtering
  - Cross-encoder reranking

---

##  Retrieval Techniques Explored

- 🔹 **Similarity-based Retrieval** using cosine distance
- 🔹 **Multi-Query Retrieval** for better query understanding
- 🔹 **Contextual Compression** using LLMs to filter noisy results
- 🔹 **Chained Retrieval Pipeline** that combines all the above for optimal results

---

##  Tech Stack

- [LangChain](https://www.langchain.com/)
- [OpenAI API](https://platform.openai.com/)
- [ChromaDB](https://www.trychroma.com/)
- [HuggingFace CrossEncoder Reranker](https://huggingface.co/BAAI/bge-reranker-large)
- Python 3.10+

---

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/qa-wikipedia-rag.git
cd qa-wikipedia-rag

# Install dependencies
pip install -r requirements.txt
```

---

##  API Keys

Add your **OpenAI API Key** in a `.env` file at the root of the repo:

```
OPENAI_API_KEY=your-openai-api-key
```

Or modify the script to use `os.environ['OPENAI_API_KEY']`.

---

## How to Run

Run the main Python script:

```bash
python src/qa_rag_pipeline.py
```

Or explore the Jupyter notebook version:

```bash
notebook/QA_RAG_System.ipynb
```

---

##  Example Output

**Input:**  
`Who was the first female scientist to win a Nobel Prize?`

**Output:**  
`Marie Curie was the first woman to win a Nobel Prize for her pioneering work in radioactivity...`

---

##  Project Structure

```
qa-wikipedia-rag/
├── data/                      # Wikipedia dataset or scripts to download it
├── notebook/                  # Jupyter notebook version of the project
├── src/                       # Python code files
├── .env                       # Your API keys (add to .gitignore)
├── requirements.txt           # All Python dependencies
├── README.md                  # You're reading it :)
```

---

## Results

-  Fast response time for complex queries
-  High contextual accuracy and factual consistency
-  Modular and extensible design

This shows how combining retrieval + generation can outperform classic search engines, especially in domain-specific tasks.

---

##  License

This project is licensed under the [MIT License](https://choosealicense.com/licenses/mit/). Feel free to use and adapt!

---

##  Acknowledgements

- OpenAI for the embeddings & language models
- LangChain team for the amazing framework
- Wikipedia dataset via `simplewiki`

---

> Made with ❤️ by Chaytanya Kumar
