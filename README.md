# Nestlé HR Policy Chatbot

An AI-powered chatbot designed to help employees get quick and accurate answers to their HR-related questions using the Nestlé HR Policy PDF.

The chatbot uses Retrieval-Augmented Generation (RAG) to retrieve relevant information from the HR policy document and generate helpful, context-aware responses.

## Project Overview

Understanding HR policies can sometimes be time-consuming, especially when employees need to search through lengthy documents to find specific information.

To make this process easier, I built the **Nestlé HR Policy Chatbot**, which allows users to ask questions in natural language and receive answers based on the provided HR policy document.

The chatbot retrieves relevant content from the PDF and uses an LLM to generate responses based on the retrieved information.

## Features

- **PDF-Based Question Answering:** Answers questions using the Nestlé HR Policy PDF.
- **RAG Architecture:** Retrieves relevant information before generating an answer.
- **Semantic Search:** Uses Hugging Face embeddings to find relevant content.
- **Vector Database:** FAISS stores and searches document embeddings efficiently.
- **LLM Integration:** Uses Groq for fast response generation.
- **Interactive Interface:** Built with Gradio for an easy-to-use chat experience.
- **Context-Aware Responses:** Provides answers based on the retrieved policy information.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Groq | LLM inference and response generation |
| LangChain | Building the RAG pipeline |
| langchain-groq | Groq integration with LangChain |
| langchain-community | Community integrations and document tools |
| langchain-huggingface | Hugging Face embedding integration |
| Hugging Face | Text embeddings |
| Sentence Transformers | Generating sentence embeddings |
| FAISS | Vector storage and similarity search |
| PyPDF | Extracting text from PDF |
| Python-dotenv | Managing environment variables |
| Gradio | Building the chatbot interface |

## How It Works

The chatbot follows a Retrieval-Augmented Generation (RAG) workflow:

1. **Load PDF:** The Nestlé HR Policy PDF is loaded using PyPDF.
2. **Text Extraction:** Text is extracted from the PDF.
3. **Text Chunking:** The extracted text is divided into smaller chunks.
4. **Generate Embeddings:** Hugging Face embedding models convert text chunks into numerical vectors.
5. **Store in FAISS:** The embeddings are stored in a FAISS vector database.
6. **Retrieve Relevant Information:** When a user asks a question, FAISS searches for relevant policy information.
7. **Generate Response:** Groq processes the retrieved context and generates an answer using the LLM.
8. **Display Answer:** Gradio displays the response in an interactive chat interface.

## Project Structure

```text
Nestle-HR-Policy-Chatbot/
│
├── app.py
├── HR_Policy.pdf
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```

*Note: Update the file names above if your actual project structure is different. Do not upload your `.env` file to GitHub.*

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

### 2. Navigate to the Project Folder

```bash
cd YOUR-REPOSITORY
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project directory and add your Groq API key:

```env
GROQ_API_KEY=your_groq_api_key
```

Replace `your_groq_api_key` with your actual API key. Never share or upload this key publicly.

### 5. Run the Application

```bash
python app.py
```

The Gradio interface will start, and you can interact with the chatbot through your browser.

## Example Questions

You can ask questions such as:

- Who makes the final hiring decision?
- What are the recruitment and selection procedures?
- What are the responsibilities of HR?
- What policies apply to employees?

The chatbot generates responses based on the information available in the HR policy document.

## Future Improvements

- Add support for multiple HR policy documents.
- Improve response accuracy and document retrieval.
- Add chat history and conversation memory.
- Deploy the chatbot for easier access.

## Disclaimer

This project is developed for learning and demonstration purposes. The chatbot provides answers based on the supplied HR policy document. Its responses should not replace official HR guidance or decisions.

---

**Built with Python, LangChain, Groq, Hugging Face, FAISS and Gradio.**
