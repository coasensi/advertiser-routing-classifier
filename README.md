## Overview

This project implements two systems for user search queries to advertiser verticals:

- Low-latency baseline (~1 ms) : TF-IDF + Logistic Regression (Top-3 Accuracy = 0.786)
- High-latency semantic model (~1 ms): LLM-based classifier with structured outputs (category + intent) (Top-3 Accuracy = ~1.00)

## Setup

### create venv (recommended)

```bash
python -m venv venv
source venv/bin/activate      # macOS/Linux
venv\Scripts\activate         # Windows
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### set api_key

option A (environment variable)

```bash
export OPENAI_API_KEY="sk-xxxx"
```

option B (.env file)

```
OPENAI_API_KEY=sk_xxxx
```

### Place the dataset

```bash
mkdir -p data
cp queries.csv data/queries.csv
```

### Run

```bash
jupyter notebook
```
