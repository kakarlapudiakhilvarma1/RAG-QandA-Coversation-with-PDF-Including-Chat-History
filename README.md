# Conversational RAG with PDF Uploads and Chat History

Welcome to the **Conversational RAG with PDF Uploads and Chat History** app! This app allows users to upload PDF documents and interact with their content using a **Conversational Retrieval-Augmented Generation (RAG)** model. The app combines the power of document retrieval, question-answering, and chat history to provide a seamless conversational experience. Users can upload PDF files, ask questions, and receive answers based on the content of the PDFs and previous chat history.

## Features ✨

- **📄 PDF Upload**: Upload multiple PDF files, which will be processed and made available for querying.
- **💬 Conversational Interface**: Engage in a conversation with the assistant, ask questions, and receive contextually aware answers based on uploaded documents and chat history.
- **🔄 Chat History**: The app maintains chat history to enhance user interactions and provide relevant responses based on past conversations.
- **🔍 Retrieval-Augmented Generation (RAG)**: The app combines **retrieval-based** techniques to search for relevant document chunks and **generation-based** techniques to generate concise and relevant answers.
- **⚡ Groq API Support**: The language model is powered by **Groq’s Gemma2-9b model**, offering fast and accurate natural language processing.

## Tech Stack 🛠️

- **Streamlit**: An easy-to-use framework to create interactive web applications.
- **LangChain**: A framework for developing language model-powered applications, used for handling chat, retrieval, and document processing.
- **Groq API**: Provides the **Gemma2-9b model** to process user input and generate responses.
- **HuggingFace Embeddings**: For document vectorization and retrieval.
- **FAISS**: For fast nearest-neighbor searches on document embeddings.
- **PyPDFLoader**: For loading and processing PDF files into documents.
- **RecursiveCharacterTextSplitter**: For splitting large text chunks from PDFs into smaller, retrievable chunks.

## Installation ⚙️

### 1. Clone the Repository
Clone the repository to your local machine:
```bash
git clone https://github.com/your-username/conversational-rag-pdf-chat-history.git
cd conversational-rag-pdf-chat-history
```

### 2. Install Dependencies
Ensure Python 3.7+ is installed. Then, install the necessary dependencies:
```bash
pip install -r requirements.txt
```

### 3. Setup Environment Variables
The app uses the **Groq API** for natural language processing. Create a `.env` file in the root of your project and add your API key:
```bash
GROQ_API_KEY=your_groq_api_key
HF_TOKEN=your_huggingface_token
```

Alternatively, you can manually input the **Groq API Key** in the Streamlit sidebar.

### 4. Run the App 🚀
Once the dependencies are installed and environment variables are set, you can run the app:

```bash
streamlit run app.py
```

Visit [http://localhost:8501](http://localhost:8501) in your browser to start interacting with the app.

## Usage 📝

1. **Enter your Groq API Key**: Provide your Groq API key for the model to process the questions and responses.
2. **Upload PDF Files**: Upload one or more PDF files that contain the content you want to query.
3. **Ask Questions**: Type your question in the provided text input box. The assistant will respond based on the content from the PDFs and the chat history.
4. **View Chat History**: The chat history is maintained for context. You can see the entire conversation and reference previous questions and answers.
5. **Interactive Conversations**: The model will remember your session and maintain context across multiple questions and interactions.

### Example Use Case 💬
- **Upload a PDF**: Upload a PDF document on any topic (e.g., a research paper, a book chapter, etc.).
- **Ask Questions**: Ask questions like "What is the main topic of the document?" or "Can you summarize the second section of the PDF?"
- **Contextual Answers**: The assistant will respond based on the content of the uploaded document and will incorporate relevant context from previous questions.

## Project Structure 🗂️

```plaintext
conversational-rag-pdf-chat-history/
│
├── app.py                     # Main Streamlit app file
├── requirements.txt           # List of dependencies
├── .env                       # Environment variables file to store API keys (e.g., GROQ_API_KEY, HF_TOKEN)
├── README.md                  # Project documentation
└── assets/
    └── (optional)             # Folder for storing assets (e.g., images, icons)
```

## Screenshots 📸

![Conversational RAG with PDF](screenshots/chat_with_pdf.png)
*Example of interacting with the uploaded PDF content through the conversational interface.*

## Contributing 🤝

We welcome contributions to improve this project! If you'd like to contribute, follow these steps:

1. Fork the repository.
2. Create a new branch for your changes.
3. Implement your changes.
4. Submit a pull request explaining the changes you've made.

## Acknowledgements 🙏

- **LangChain**: For building the framework that integrates retrieval and generation-based approaches.
- **Groq**: For providing the **Gemma2-9b** model to generate natural language responses.
- **HuggingFace**: For the **all-MiniLM-L6-v2** embeddings model used to vectorize documents.
- **FAISS**: For enabling fast document retrieval based on embeddings.
- **PyPDFLoader**: For loading PDF files into a format that can be processed and queried.

---

**Note**: Make sure you have a valid **Groq API Key** to process questions and responses effectively. If you don't have a key, please obtain one from the Groq platform.

---

This `README.md` provides a comprehensive overview of the app, detailing its functionality, installation, usage instructions, and contributing guidelines. It also includes setup details for environment variables and dependencies.
