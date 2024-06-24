# RAG-Based Chat Bot

## Overview

This project implements a Retrieval-Augmented Generation (RAG) based chatbot. The chatbot processes a PDF file, splits the text into sentences, and uses a Parent-Child Document Retriever to answer user questions based on the content of the PDF file.

## Data Preprocessing

The data preprocessing includes the following steps:

1. **Split Text into Sentences**: The text extracted from the PDF file is split into individual sentences for more granular analysis.
2. **Duplicate First and Last Page Texts**: To improve the accuracy of the retrieval, the text from the first and last pages of the PDF is duplicated and included in the combined text.
3. **Use Parent-Child Document Retriever**: The document retriever uses a parent-child chunking strategy, where small chunks (child) are used to find relevant information, and larger chunks (parent) are used to provide context for answering questions.

## Notebooks

### chat_bot.ipynb

This notebook includes the data preprocessing functions and the main chatbot script. It handles the extraction of text from PDF files, sentence splitting, text duplication, and the implementation of the Parent-Child Document Retriever.

### advanced RAG element example.ipynb

This notebook demonstrates the improvement in the chatbot. It compares the performance of the initial chatbot with the improved version by answering a set of sample questions. The naive ChatBot was only able to answer one question and tried to use Gemini using an API key.

The first chatbot with Gemini API was not able to answer the following questions:

- What is the Parent-Child Document Retriever?
- Why do RAG applications benefit from using a Parent-Child Document Retriever?

The final chatbot has improved by following these steps:

1. Splitting text into sentences.
2. Duplicating the first and last page texts.
3. Using the Parent-Child Document Retriever.

After implementing these steps, the second chatbot can answer the questions that the first model could not.

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

