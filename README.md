# T5 SAMSum Text Summarizer

An abstractive dialogue summarization application built by fine-tuning **T5-small** on the **SAMSum** dataset and serving the model with **FastAPI**.

## Features

- Fine-tuned T5-small Transformer model
- SAMSum dialogue summarization
- FastAPI inference API
- Simple web interface
- Model hosted on Hugging Face

## Model

- Base Model: T5-small
- Dataset: SAMSum
- Training Samples: 4,000
- Validation Samples: 500
- Epochs: 6
- Batch Size: 8
- Max Input Length: 512 tokens
- Generation: Beam Search

Fine-tuned model: **SBG06/t5-samsum-summarizer**

## Tech Stack

- Python
- PyTorch
- Hugging Face Transformers
- FastAPI
- Uvicorn
- HTML/CSS
- Git/GitHub

## Project Structure

```text
t5-samsum-summarizer/
├── app.py
├── index.html
├── requirements.txt
├── .gitignore
└── README.md
```

## Run Locally

```bash
git clone https://github.com/Sbghosh/t5-samsum-summarizer.git
cd t5-samsum-summarizer
pip install -r requirements.txt
uvicorn app:app --host 0.0.0.0 --port 8000
```

Open `http://127.0.0.1:8000` in your browser.

## Deployment

No permanent public demo is currently available. The application runs locally and loads the fine-tuned model from Hugging Face.
