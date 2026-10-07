# RAG Question Answering System

A **Retrieval-Augmented Generation (RAG)** based Question Answering System that allows users to ask questions from PDF documents and receive context-aware answers.

The project combines **PDF processing, text chunking, embeddings, vector search, and Large Language Models (LLMs)** to retrieve relevant information from documents before generating an answer.

## Project Workflow

```text
PDF Documents
      ↓
Text Extraction
      ↓
Text Chunking
      ↓
Text Embeddings
      ↓
ChromaDB Vector Store
      ↓
Semantic Retrieval
      ↓
Relevant Context
      ↓
LLM
      ↓
Final Answer
```

## Features

* 📄 PDF document processing
* ✂️ Text chunking for better retrieval
* 🔢 Text embedding generation
* 🗄️ ChromaDB vector database
* 🔍 Semantic similarity-based document retrieval
* 🤖 Retrieval-Augmented Generation (RAG)
* 💬 Context-aware question answering
* 📓 Jupyter Notebook based implementation
* 🔐 Environment-variable support for API keys

## Technologies Used

* **Python**
* **Jupyter Notebook**
* **LangChain**
* **ChromaDB**
* **Sentence Transformers / Embedding Models**
* **Large Language Models (LLMs)**
* **PyPDF**
* **Git & GitHub**

## Project Structure

```text
RAG-Question-Answering-system/
│
├── RAG_pipeline.ipynb
├── README.md
├── .gitignore
│
└── data/
    ├── pdf/
    │   └── PDF documents
    │
    └── python.txt.txt
```

> The generated vector store and temporary files are excluded from Git using `.gitignore`.

## How It Works

### 1. Load PDF Documents

PDF files are loaded and their text content is extracted.

### 2. Split Text

The extracted text is divided into smaller chunks so that relevant information can be retrieved efficiently.

### 3. Generate Embeddings

Each text chunk is converted into a numerical vector using an embedding model.

### 4. Store Embeddings

The embeddings and corresponding document text are stored in **ChromaDB**.

### 5. Retrieve Relevant Information

When a user asks a question, the system converts the question into an embedding and searches the vector database for the most relevant chunks.

### 6. Generate the Answer

The retrieved context is provided to an LLM, which generates a relevant answer based on the retrieved information.

## Installation

Clone the repository:

```bash
git clone https://github.com/mehul2376/RAG-Question-Answering-system-.git
```

Move into the project directory:

```bash
cd RAG-Question-Answering-system-
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## API Key Configuration

If the project uses an external LLM API, store the API key in an environment variable instead of directly writing it inside the notebook.

Create a `.env` file:

```env
GROQ_API_KEY=your_api_key_here
```

Never upload the `.env` file to GitHub.

## Running the Project

Open the Jupyter Notebook:

```bash
jupyter notebook RAG_pipeline.ipynb
```

Run the notebook cells in order to:

1. Load the PDF documents
2. Extract and split the text
3. Generate embeddings
4. Store embeddings in ChromaDB
5. Retrieve relevant document chunks
6. Generate answers using the LLM

## Example

**Question:**

```text
What is RAG?
```

The system searches the uploaded documents for relevant information and generates an answer using the retrieved context.

## Learning Objectives

This project helped me understand:

* Retrieval-Augmented Generation
* Vector databases
* Text embeddings
* Semantic search
* Document retrieval
* LangChain workflows
* Working with LLMs
* Building a basic AI-powered Question Answering system

## Future Improvements

* Add a web-based user interface
* Support multiple PDF uploads
* Add source/page citations to answers
* Improve document retrieval using reranking
* Add conversation history
* Add support for more document formats
* Deploy the application as a web service

## Author

**Mehul Kumar**

B.Tech Computer Science & Engineering
Interested in **AI/ML, Generative AI, RAG, and Machine Learning**.

## License

This project is intended for educational and learning purposes.
