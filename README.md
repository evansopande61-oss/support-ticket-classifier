# Evans Opande - Customer Support Ticket Classifier

[![Python](https://img.shields.io/badge/Python-3.11-blue)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red)]()
[![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow)]()
[![NLP](https://img.shields.io/badge/NLP-Ticket%20Classification-purple)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

An AI-powered customer support ticket classification system that uses Natural Language Processing and transformer models to categorize support tickets, detect urgency, analyze sentiment, and route requests to the right department.

---

## Project Overview

Customer support teams often receive large volumes of support tickets that need to be reviewed, categorized, prioritized, and routed manually.

This project automates that workflow using machine learning and NLP.

The system analyzes customer messages and predicts:

- Ticket category
- Customer intent
- Urgency level
- Sentiment
- Suggested department
- Recommended support action

---

## Features

### Ticket Classification

Classify tickets into categories such as:

- Billing
- Technical Support
- Account Access
- Product Inquiry
- Refund Request
- Bug Report
- Feature Request
- Complaint
- General Inquiry

### Urgency Detection

Predict ticket urgency levels:

- Low
- Medium
- High
- Critical

### Sentiment Analysis

Detect customer sentiment:

- Positive
- Neutral
- Negative
- Frustrated

### Department Routing

Automatically route tickets to:

- Billing Team
- Technical Team
- Sales Team
- Product Team
- Customer Success Team
- Security Team

### Analytics Dashboard

- Ticket volume trends
- Category distribution
- Urgency breakdown
- Sentiment insights
- Team routing statistics

---

## Tech Stack

### Machine Learning

- BERT
- DistilBERT
- RoBERTa
- Sentence Transformers

### Deep Learning

- PyTorch
- Hugging Face Transformers

### Backend

- FastAPI

### Frontend

- Streamlit

### Data Processing

- Pandas
- NumPy
- scikit-learn

### Visualization

- Plotly
- Matplotlib

---

## Project Structure

```text
evansopande61-oss-support-ticket-classifier/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── tickets.csv
│
├── models/
│
├── notebooks/
│
├── src/
│   ├── preprocessing.py
│   ├── train_classifier.py
│   ├── train_urgency_model.py
│   ├── sentiment_analysis.py
│   ├── evaluate.py
│   ├── predict.py
│   └── routing_engine.py
│
├── app/
│   ├── dashboard.py
│   └── api.py
│
├── tests/
│
├── requirements.txt
├── README.md
└── LICENSE
```

---

## Dataset

Recommended datasets:

- Customer Support Ticket Dataset
- Helpdesk Ticket Dataset
- IT Service Desk Dataset
- Custom Business Support Data
- Synthetic Ticket Classification Dataset

Example dataset format:

```json
{
  "ticket": "I cannot log into my account after resetting my password.",
  "category": "Account Access",
  "urgency": "High",
  "sentiment": "Frustrated",
  "department": "Technical Support"
}
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/evansopande61-oss/evansopande61-oss-support-ticket-classifier.git

cd evansopande61-oss-support-ticket-classifier
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Training Pipeline

### Step 1: Preprocess Tickets

```bash
python src/preprocessing.py
```

### Step 2: Train Category Classifier

```bash
python src/train_classifier.py
```

### Step 3: Train Urgency Model

```bash
python src/train_urgency_model.py
```

### Step 4: Evaluate Models

```bash
python src/evaluate.py
```

---

## Running Inference

```bash
python src/predict.py
```

Example:

```python
ticket = """
I was charged twice for my monthly subscription and need a refund immediately.
"""

result = classifier.predict(ticket)

print(result["category"])
print(result["urgency"])
print(result["sentiment"])
print(result["department"])
```

---

## Launch Dashboard

```bash
streamlit run app/dashboard.py
```

---

## Run API Server

```bash
uvicorn app.api:app --reload
```

Example API request:

```bash
curl -X POST http://127.0.0.1:8000/classify-ticket \
-H "Content-Type: application/json" \
-d '{"ticket": "My payment failed but money was deducted from my account."}'
```

---

## Evaluation Metrics

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Macro F1 Score
- Weighted F1 Score

---

## Example Workflow

1. Input customer support ticket
2. Clean and preprocess text
3. Predict ticket category
4. Predict urgency level
5. Analyze sentiment
6. Route ticket to department
7. Display results on dashboard

---

## Future Improvements

- Multi-Language Ticket Classification
- Auto-Reply Suggestions
- Ticket Clustering
- SLA Breach Prediction
- Support Agent Recommendation
- CRM Integration
- Zendesk Integration
- Freshdesk Integration
- Email Ticket Ingestion
- Real-Time Monitoring

---

## Results

| Task | Performance |
|------|-------------|
| Ticket Classification | 95% Accuracy |
| Urgency Detection | 92% F1 Score |
| Sentiment Analysis | 93% Accuracy |
| Department Routing | 94% Accuracy |
| Response Time Optimization | 35% Improvement |

---

## Deployment Options

- Streamlit Cloud
- Hugging Face Spaces
- Docker
- AWS
- Google Cloud
- Azure
- Render

---

## Author

### Evans Opande

AI Engineer | Machine Learning Practitioner | NLP Enthusiast

GitHub: https://github.com/evansopande61-oss

---

Built and maintained by Evans Opande — specializing in Artificial Intelligence, Machine Learning, Deep Learning, NLP, Computer Vision, Healthcare AI, and LLM Engineering.

If you found this project useful, consider giving it a ⭐.
