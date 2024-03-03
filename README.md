# COVID-19 Knowledge Retrieval System

![License](https://img.shields.io/badge/license-MIT-blue.svg)

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Dataset](#dataset)
6. [Data Preprocessing](#data-preprocessing)
7. [Text Vectorization](#text-vectorization)
8. [Preparation of the Model](#preparation-of-the-model)
9. [Requirements](#requirements)
10. [Deployment](#deployment)
11. [License](#license)
12. [FAQ](#faq)

## Introduction

This project presents a novel approach for answering high-priority scientific questions related to COVID-19 using the CORD-19 dataset. The system utilizes LangChain and Llama-2, a dense passage retrieval model, to efficiently retrieve relevant passages and generate comprehensive answers to user queries. The framework aids in the extraction of valuable knowledge from the expanding COVID-19 literature, supporting the medical community in their research efforts.

## Features

- **Advanced Retrieval:** Leverages Llama-2 for efficient dense passage retrieval from the extensive CORD-19 dataset.
- **Question Answering System:** Functions as an A+ question answering system, providing comprehensive answers to user queries.
- **Large-Scale Data Processing:** Utilizes LangChain for large-scale data processing and model training.

## Installation

To install and set up the project, follow these steps:

1. Clone the repository: `git clone https://github.com/yourusername/COVID-19-Knowledge-Retrieval-System.git`
2. Change to the project directory: `cd COVID-19-Knowledge-Retrieval-System`
3. Install the required dependencies: `pip install -r requirements.txt`

## Usage

1. Execute the code based on your requirements.
2. Interact with the system using user queries for efficient knowledge retrieval.

## Dataset

The dataset used for training the models is the COVID-19 Open Research Dataset Challenge (CORD-19) obtained from [Kaggle](https://www.kaggle.com/datasets/allen-institute-for-ai/CORD-19-research-challenge). This is a freely available dataset is provided to the global research community to apply recent advances in natural language processing and other AI techniques to generate new insights in support of the fight against COVID-19.
Data Preprocessing

## Data preprocessing 

Textual chunks are created using RecursiveCharacterTextSplitter, approximately 500 characters in length with a 20-character overlap. The chunks are transformed into numerical embeddings using the "sentence-transformers/all-MiniLM-L6-v2" model from Hugging Face. These embeddings are stored in a FAISS vector store, establishing a knowledge base for efficient similarity searches during conversational retrieval.

## Text Vectorization

Text vectorization involves converting textual information into fixed-size numerical embeddings. The code utilizes the Hugging Face model for sentence embeddings, transforming text chunks into embeddings and storing them in a FAISS vector store for efficient similarity search and retrieval during the conversational retrieval process.

## Preparation of the Model

The code provided involves the preparation and integration of the "llama-2" model using the "langchain" library for question answering within a conversational retrieval system. The language model is loaded, configured, and integrated into the Conversational Retrieval Chain, utilizing the FAISS vector store for efficient document retrieval. The system operates in an interactive query loop, responding to user queries with context-aware information retrieval.

### File Structure

The file structure is organized as follows:

```plaintext
.
├──data/                # Place your data here
    ├── metadata.csv
    └── sample.csv
├── models/             # Download and place the Llama 2 Model from https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main
├── vectorstore/        # Stores Text Embeddings
    └── db_faiss/
├── CORD_19.ipynb       # Main Script
└── requirements.txt    # Requirements file
```

## Requirements

The project was developed using Python 3.10 and relies on various dependencies. Install them using:

```bash
pip install -r requirements.txt
```
Please ensure you have Python 3.10 installed, along with the specified package versions, to run the project successfully.

## Deployment

The project can be deployed based on your specific requirements. Ensure the necessary configurations are set for LangChain, Llama-2, and any additional components.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

## FAQ

### 1. What is the primary purpose of this project?

The main goal of this project is to provide an advanced knowledge retrieval system for efficiently answering high-priority scientific questions related to COVID-19. It leverages the CORD-19 dataset, LangChain, and Llama-2 to extract valuable information from the vast COVID-19 literature.

### 2. Can I deploy this system in my own environment?

Yes, the project can be deployed based on your specific requirements. Ensure that you configure LangChain, Llama-2, and any additional components as needed for your environment.

### 3. How can I contribute to this project?

Contributions to the project are welcome! You can contribute by suggesting improvements, reporting issues, or submitting pull requests on the project's GitHub repository. Your engagement and feedback are valuable to enhance the system.
