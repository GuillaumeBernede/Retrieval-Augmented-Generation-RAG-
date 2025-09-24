## Project Overview
This project implement a **Retrieval-Augmented Generation (RAG)** system using [LangChain](https://www.langchain.com/) and model hosted on [Hugging Face Hub](https://huggingface.co/)

The notebook explores different ways to load documents (TXT & PDF), generate embeddings, store them in a vector database, and query them using multiple Large Language Models (LLMs). Finally, a simple user interface was built with **Gradio**.

---

## Workflow

### 1. Experimenting with .txt file
First, the project experiments with different Hugging Face models:
  - `google/flan-t5-large`
  - `mistralai/Mistral-7B-Instruct-v0.1`
  - `google/gemma-7b-it`

The text used was *Alice in Wonderland* (`alice_in_wonderland.txt`).

The models were compared on simple Q&A tasks.

Here are some example of the obtained results :
<img width="1774" height="382" alt="image" src="https://github.com/user-attachments/assets/59eaa307-7dcb-482a-8c26-88eaec2224e8" />

---

### 2. Multilingual test with GOODLUCK.pdf
The file `GOODLUCK.pdf` was used to test multilingual capabilities. It is a **poem written in multiple languages**. 

The objective was to evaluate how well the models can handle and understand multilingual text inside the RAG pipeline.  

#### Flan-t5-large
<img width="1682" height="61" alt="image" src="https://github.com/user-attachments/assets/b5c8e65b-68d0-4cad-8d22-3ef26c236aa3" />
#### Gemma-7b-it
<img width="1182" height="86" alt="image" src="https://github.com/user-attachments/assets/0dc8f7cd-1b23-4dca-8735-b7ee6dee69c2" />


---

### 3. Working with PDF documents
Now, we want the pipeline to work with PDF files. Several PDFs related to **sports and health** were used ( they can be found in the PDF_DATABASE folder ).

I tested how differents models could retrieve and answer questions based on these PDFs, and I used Gradio to create a user friendly interface :  

<img width="1902" height="686" alt="Capture d'écran 2024-03-24 183033" src="https://github.com/user-attachments/assets/09a97eb5-8d9f-4c36-b7dd-a031c90d756b" />

<img width="1918" height="505" alt="Capture d'écran 2024-03-24 183941" src="https://github.com/user-attachments/assets/e345e2f9-337d-477a-8be9-266a6ae0d916" />

