# RAG with LLM: Retrieval-Augmented Generation using Large Language Models

This repository contains a Jupyter Notebook (`RAG_LLM.ipynb`) that demonstrates how to implement Retrieval-Augmented Generation (RAG) using Large Language Models (LLMs). The notebook leverages the `langchain` library to interact with a large language model (LLM) and retrieve information from a specified set of documents, in this case, the U.S. Constitution.

## What is RAG?

Retrieval-Augmented Generation (RAG) is a process that enhances the interaction with a large language model by allowing it to respond to queries with reference to a specified set of documents. This approach is particularly useful when you want the model to prioritize information from a specific dataset over its general training data.

## Features

- **Document Loading**: The notebook uses `PyPDFLoader` from the `langchain_community.document_loaders` module to load the U.S. Constitution PDF document.
- **Text Splitting**: The document is split into smaller chunks using `CharacterTextSplitter` from `langchain_text_splitters` to facilitate better processing.
- **Embeddings**: The notebook uses `GoogleGenerativeAIEmbeddings` to generate embeddings for the text chunks.
- **Vector Store**: The embeddings are stored in a vector store using `chromadb` for efficient retrieval.
- **Retrieval Chain**: The notebook sets up a retrieval chain using `create_retrieval_chain` to retrieve relevant documents based on user queries.
- **Prompt Template**: A custom prompt template is used to guide the LLM in generating responses based on the retrieved documents.

## Requirements

To run this notebook, you need to install the following Python libraries:

```bash
pip install langchain_google_genai
pip install langchain_community
pip install langchain_text_splitters
pip install pypdf
pip install chromadb
