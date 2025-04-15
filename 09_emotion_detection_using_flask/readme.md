# 🧠 AI-Powered Sentiment Analysis API using IBM Watson NLP

This project is a Flask-based web application that performs sentiment analysis on text inputs using **IBM Watson NLP BERT model** via REST API.

---

## 🚀 Features

- 🔍 Analyze the sentiment of any text (positive, negative, neutral, or mixed)
- 🌐 Built using Flask and Python
- 🧠 Powered by IBM Watson NLP BERT endpoint
- ⚙️ Includes error handling and response codes (e.g., 400 for bad input, 500 for server errors)
- 🧪 Unit tested for robustness
- 📦 Easily importable and reusable as a Python module

---

## 📁 Project Structure

```
.
├── app.py                 # Flask API server
├── sentiment_analyzer.py # Core Watson NLP logic
├── test_sentiment.py     # Unit tests
├── requirements.txt      # Dependencies
└── README.md             # Project overview
```

---

## 📦 Installation

1. **Clone the repository**
```bash
git clone https://github.com/your-username/sentiment-analyzer-flask.git
cd sentiment-analyzer-flask
```

2. **Create a virtual environment (optional but recommended)**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

---

## 🛠️ Usage

### 🔧 Start the Flask server

```bash
python app.py
```

The app will start on:  
```
http://127.0.0.1:5000/
```

### 📡 Test the Sentiment Endpoint

Send a POST request to `/analyze` with a JSON body:

#### Example Request
```bash
curl -X POST http://127.0.0.1:5000/analyze \
     -H "Content-Type: application/json" \
     -d '{"text": "This app is amazing!"}'
```

#### Example Response
```json
{
  "label": "positive",
  "score": 0.93
}
```

---

## ⚙️ Error Handling

| Error | Code | Description                  |
|-------|------|------------------------------|
| 400   | Bad Request | Empty or invalid input |
| 500   | Internal Server Error | API or server issues |

---

## 🧪 Running Unit Tests

```bash
python test_sentiment.py
```

---

## 🧹 Code Quality

PEP8 style check:
```bash
pip install flake8
flake8 sentiment_analyzer.py app.py
```

---

## 🧠 Powered By

- [IBM Watson NLP](https://developer.ibm.com/apis/catalog/watson-natural-language-understanding-nlu/)
- Flask
- Python `requests`

---

## 📄 License

MIT License

---
