# PDF Document Understanding with Transformers

This project is a Python-based NLP pipeline for automatic document understanding.  
It extracts text from a PDF document, summarizes the content, generates relevant questions, and answers those questions using Transformer-based models. It was possible thank to https://amanxai.com/2024/10/21/document-analysis-using-llms-with-python/

## Features

- PDF text extraction using `pdfplumber`
- Text cleaning and preprocessing
- Sentence segmentation using `NLTK`
- Document summarization using `T5`
- Automatic question generation using `valhalla/t5-base-qg-hl`
- Question answering using `deepset/roberta-base-squad2`
- Modular and reusable code structure
- JSON export of generated Q&A results

## Workflow

The pipeline follows these steps:

1. Load a PDF document
2. Extract and clean the text
3. Split the document into manageable passages
4. Generate a summary of the document
5. Generate questions from each passage
6. Answer the generated questions using the passage as context
7. Store the results in a structured format

## Models Used

| Task | Model |
|---|---|
| Summarization | `t5-small` |
| Question Generation | `valhalla/t5-base-qg-hl` |
| Question Answering | `deepset/roberta-base-squad2` |

## Installation

```bash
pip install transformers torch sentencepiece nltk pdfplumber
