# RAG-Based Chat Bot

## Overview

This project implements a Retrieval-Augmented Generation (RAG) based chat bot. The chat bot processes a PDF file, splits the text into sentences, and uses a Parent-Child Document Retriever to answer user questions based on the content of the PDF file.

## Data Preprocessing

The data preprocessing includes the following steps:

1. **Split Text into Sentences**: The text extracted from the PDF file is split into individual sentences for more granular analysis.
2. **Duplicate First and Last Page Texts**: To improve the accuracy of the retrieval, the text from the first and last pages of the PDF is duplicated and included in the combined text.
3. **Use Parent-Child Document Retriever**: The document retriever uses a parent-child chunking strategy, where small chunks (child) are used to find relevant information, and larger chunks (parent) are used to provide context for answering questions.

## Usage

### Dependencies

Ensure you have the following dependencies installed:
- `PyPDF2`
- `re`
- `concurrent.futures`
- `pandas`
- `google.colab`
- `os`
- `huggingface_hub`
- `Chroma`

