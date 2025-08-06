# Talk to Your PDF: RAG with Gemini

This repository contains a Google Colab notebook that demonstrates how to build a simple Retrieval Augmented Generation (RAG) application to chat with your PDF documents using the Gemini API.

## How to Use

1.  **Open in Google Colab:**

    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-github-username/your-repo-name/blob/main/RAG_PDF_Intro.ipynb)

    *(Note: You will need to replace `your-github-username` and `your-repo-name` with your actual GitHub information if you are hosting this repository.)*

2.  **Get your Gemini API Key:**

    *   Go to the [Google AI Studio](https://aistudio.google.com/app/apikey).
    *   Click on **"Create API key"**.
    *   Copy the generated API key.

3.  **Set up your API Key in Colab:**

    *   In the Colab notebook, click on the **"Key"** icon in the left sidebar to open the **Secrets** tab.
    *   Click on **"+ Add a new secret"**.
    *   Enter `GEMINI_API_KEY` as the name of the secret.
    *   Paste your copied API key into the **"Value"** field.
    *   Make sure the **"Notebook access"** toggle is enabled.

4.  **Run the Notebook:**

    *   Follow the instructions in the notebook to install the required libraries.
    *   Upload your PDF file when prompted.
    *   Run the cells to interact with your PDF.

## How it Works

The notebook uses the following technologies:

*   **Google Gemini:** For the generative language model.
*   **LangChain:** To orchestrate the RAG pipeline.
*   **FAISS:** For efficient similarity search in a vector store.
*   **PyPDF:** To load and parse PDF documents.

The process is as follows:

1.  The text is extracted from the uploaded PDF.
2.  The extracted text is split into smaller chunks.
3.  The text chunks are converted into numerical vectors (embeddings) using a Gemini embedding model.
4.  The embeddings are stored in a FAISS vector store for efficient retrieval.
5.  When you ask a question, the notebook searches the vector store for the most relevant text chunks.
6.  The question and the retrieved text chunks are passed to the Gemini Pro model to generate a response.
