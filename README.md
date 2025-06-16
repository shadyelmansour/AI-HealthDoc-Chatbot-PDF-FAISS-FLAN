

# AI HealthDoc Chat — A Local PDF-Based Healthcare Question Answering System

## Description

AI HealthDoc Chat is a privacy-focused, offline-capable chatbot system that allows users to upload any healthcare-related PDF and ask questions about its contents. It uses local open-source models to ensure sensitive medical information is not exposed to external APIs.

This project is ideal for interacting with discharge summaries, prescriptions, lab reports, clinical documents, and educational healthcare PDFs.

## Features

* Upload a PDF and chat with its content
* No OpenAI or paid APIs — works with free, local models like FLAN-T5
* Embeds document chunks using FAISS for fast semantic search
* Natural language Q\&A using LangChain and Hugging Face models
* Easy-to-use Gradio interface
* Built and tested in Google Colab

## Tech Stack

* Python
* Google Colab
* LangChain
* FAISS
* PyMuPDF (fitz)
* Hugging Face Transformers (FLAN-T5)
* Gradio

## Project Workflow

1. Upload your healthcare PDF
2. Split the document into chunks using LangChain’s text splitter
3. Embed the chunks using a local embedding model
4. Store and retrieve using FAISS vector database
5. Answer user queries using a FLAN-T5 model via LangChain chain
6. Interact through a simple Gradio interface

## Setup Instructions

### 1. Clone the Repository


git clone https://github.com/yourusername/AI-HealthDoc-Chat.git
cd AI-HealthDoc-Chat


### 2. Install Dependencies

You can run this in Google Colab, or install locally using:


pip install langchain faiss-cpu gradio pymupdf transformers


### 3. Run in Google Colab

Open the provided `.ipynb` file in Colab. It will:

* Prompt for uploading your PDF
* Build the vector store
* Launch a Gradio app to ask questions

### 4. Local Running Option (Advanced)

If you wish to run it locally:

* Download any FLAN-T5 model from Hugging Face
* Replace the embedding and LLM pipeline with local references
* Launch using Gradio

## Sample Use Cases

* Reviewing doctor notes and prescriptions
* Asking questions about a lab test report
* Learning from medical textbooks or guides
* Summarizing patient records privately

## Example Questions

* What is the diagnosis in this report?
* What medications were prescribed?
* What follow-up is advised?
* What tests were conducted?


## Limitations

* Works best with clearly formatted text PDFs
* Not suitable for scanned or image-only documents
* Basic summarization and question answering; not a diagnostic tool

## Contributions

Pull requests, bug reports, and suggestions are welcome.


