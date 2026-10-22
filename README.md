# Llama2 Project for MetaData Generation using FAISS and RAGs

The project aims to streamline metadata generation using large language models, specifically leveraging Llama2, RAGs, and AWS.

## Overview
Metadata refers to descriptive information about data that provides context, meaning, and structure. In simpler terms, metadata is "data about data." It plays a crucial role in organizing, managing, and understanding various types of information.

Examples of Metadata: Text Document: Author, Title, Word Count, File Format Web Page: URL, Last Modified, Meta Tags

This descriptive information aids in efficient search and retrieval, allowing users to find relevant data quickly. Metadata ensures proper interpretation of data, supporting decision-making processes. In diverse fields like libraries, archives, and digital asset management, metadata enhances workflow efficiency and fosters interoperability. Generally, metadata is created by manually documenting relevant details associated with the data.

## Data
The dataset includes project documentation text files and code files. These files represent project-related documents containing various information, including project details, code implementations, and associated documentation. Leveraging this dataset, the project aims to automate and enhance metadata creation for various machine-learning projects.

_Data is not included in this repository._

## Approach
- Project Setup: ○ Creating and Configuring AWS EC2 instances for GPU support ○ Set up the Python environment and dependencies, ensuring compatibility with required libraries and frameworks.
- Data Extraction:

○ Identify and parse project documentation, text files, and code files for metadata generation. ○ Utilize Textract for PDF files and Tika for specific formats. ○ Use langchain to parse and extract information from various file formats, creating a unified, large text dataset.
- Embedding and Vectorization: ○ Employ the HuggingFace Transformers library to embed the large text dataset into numerical vectors. ○ Utilize a quantized version of the Llama2 language model for efficient processing.
- Vector Database Creation: ○ Build a FAISS Vector Database to store and manage the embedded text vectors. ○ Implement a defined structure for storing project-related information.
- Prompt Engineering: ○ Design a prompt template to guide the LLM in generating responses based on the provided context. ○ Emphasize context-aware answers to avoid hallucination and maintain accuracy.
- Question-Answering Pipeline: ○ Load the Llama2 model, tokenizer, and vector database for question-answering tasks. ○ Utilize Streamlit for creating a user-friendly graphical interface.

Modular code overview:

Once you unzip the modular_code.zip file, you can find the following:

Here is a brief information on the files:

- The code folder contains all the Python scripts and sample files used in the project. You can execute either the main.py file or streamlit_main.py file according to your requirements.
- The README.MD and the solution methodology file provides essential information about the project, its purpose, usage, and setup instructions. Kindly follow all the instructions for running the code from Readme.md file
- The requirements.txt file has all the required libraries with respective versions. Kindly install the file by using the command pip install -r requirements.txt

## Tech stack
➔ Language: Python 3.10.4 ➔ Libraries: langchain, torch, Textract, Tika, HuggingFace Transformers, Faiss ➔ Model: Llama2 (13 billion parameters, Quantized) ➔ Cloud Platform: Amazon Web Services (AWS)

## How to run
```bash
pip install -r Code_Folder_CPU/requirements.txt
python Code_Folder_CPU/code/main.py
python Metdata Generation/code/main.py
```

## Project structure
```
.gitignore
Code_Folder_CPU/
  code/
    .streamlit/
    configs.py
    main.py
    sample_files/
    streamlit_main.py
    utils.py
  readme.md
  requirements.txt
Metdata Generation/
  code/
    configs.py
    main.py
    streamlit_main.py
    utils.py
  readme.md
README.md
```

## Credits
Based on a ProjectPro guided project.
