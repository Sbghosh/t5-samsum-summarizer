# T5 SAMSum Text Summarizer

A text summarization web application built using a fine-tuned **T5-small** Transformer model trained on the **SAMSum dialogue summarization dataset**.

The project provides a FastAPI-based web interface where users can enter a conversation or dialogue and generate a concise summary.

## Demo

![T5 SAMSum Text Summarizer](screenshot.png)

## Project Overview

This project demonstrates an end-to-end NLP workflow:

- Dataset preprocessing and cleaning
- Fine-tuning a pretrained T5-small Transformer model
- Dialogue summarization
- Model saving and loading
- FastAPI backend development
- Web-based user interface
- Hugging Face model deployment and versioning

## Architecture

```text
User
  │
  ▼
Web Interface
  │
  ▼
FastAPI Backend
  │
  ▼
T5-small Fine-tuned Model
  │
  ▼
Generated Summary
```

## Model

**Model:** T5-small  
**Task:** Abstractive text summarization  
**Training Dataset:** SAMSum  
**Framework:** Hugging Face Transformers + PyTorch

The fine-tuned model is available on Hugging Face:

**[SBG06/t5-samsum-summarizer](https://huggingface.co/SBG06/t5-samsum-summarizer)**

## Dataset

The model was fine-tuned on the **SAMSum dataset**, which contains messenger-style conversations paired with human-written summaries.

For experimentation and training within available computational resources, a sampled subset of the dataset was used:

- Training samples: 4,000
- Validation samples: 500

## Preprocessing

The dialogue data was cleaned before training using:

- Whitespace normalization
- Removal of HTML-like tags
- Newline normalization
- Lowercasing
- Input truncation to a maximum length of 512 tokens

## Fine-Tuning

The pretrained T5-small model was fine-tuned for dialogue summarization.

Key training configuration included:

- Model: `t5-small`
- Training epochs: 6
- Training batch size: 8
- Maximum input length: 512
- Maximum target length: 150
- Beam search used during generation

## Web Application

The application uses **FastAPI** as the backend.

### Technologies

- Python
- FastAPI
- Uvicorn
- Hugging Face Transformers
- PyTorch
- SentencePiece
- Jinja2
- HTML/CSS
- T5 Transformer architecture

## Project Structure

```text
t5-samsum-summarizer/
│
├── app.py
├── index.html
├── requirements.txt
├── .gitignore
└── README.md
```

The trained model files are hosted separately on Hugging Face rather than stored directly in this GitHub repository.

## Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/Sbghosh/t5-samsum-summarizer.git
cd t5-samsum-summarizer
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the FastAPI application

```bash
uvicorn app:app --host 0.0.0.0 --port 8000
```

### 4. Open the application

Open the local address in your browser:

```text
http://127.0.0.1:8000
```

The application downloads the fine-tuned model from Hugging Face when it starts.

## Live Demo

A permanent public demo is not currently hosted.

The application can be run locally using the instructions above.

## Model Repository

The trained model is publicly available on Hugging Face:

**[SBG06/t5-samsum-summarizer](https://huggingface.co/SBG06/t5-samsum-summarizer)**

## Future Improvements

Potential improvements include:

- Training on the complete SAMSum dataset
- Hyperparameter optimization
- Evaluation using ROUGE metrics
- Improved preprocessing
- Better generation controls
- Deployment on a dedicated inference service
- Support for longer conversations
- Improved frontend design

GitHub: **[Sbghosh](https://github.com/Sbghosh)**
