# Agentic AI RAG System with Weaviate and Gemini

This project implements a Retrieval Augmented Generation (RAG) system that answers questions based on the "Agentic AI" PDF document ([https://www.artificiality.world/content/files/2024/05/Agentic-AI.pdf](https://www.artificiality.world/content/files/2024/05/Agentic-AI.pdf)). It utilizes Weaviate as a vector database for efficient retrieval of relevant information and Gemini (or another LLM) to generate natural language responses.

## Overview

This RAG system follows these key steps:

1.  **Data Ingestion:** The "Agentic AI" PDF is downloaded and its text content is extracted.
2.  **Text Chunking:** The extracted text is divided into smaller chunks to improve retrieval relevance and manage context within the LLM.
3.  **Embedding Generation:** Sentence embeddings are created for each text chunk using the "sentence-transformers/all-mpnet-base-v2" Hugging Face model.
4.  **Vector Database Storage:** The text chunks and their corresponding embeddings are stored in a Weaviate vector database.
5.  **Retrieval and Question Answering:** When a user asks a question, the system generates an embedding for the query, retrieves the most similar text chunks from Weaviate, and uses Gemini (or another LLM) to generate a natural language answer based on the retrieved context.

## Technologies Used

*   **Weaviate:** Vector database for storing and retrieving embeddings.
*   **Hugging Face Transformers:** For generating sentence embeddings using "sentence-transformers/all-mpnet-base-v2".
*   **Gemini (or alternative LLM):** Large Language Model for generating natural language responses.
*   **Python:** Programming language for implementation.
*   **LangChain (Optional but recommended):** For streamlining the RAG pipeline.
*   **DirectoryLoader :** For all PDF files text extraction.
