# 🧠 Reddit Stock Sentiment Analyzer

An interactive sentiment analysis tool that extracts and analyzes stock-related discussions from Reddit. It leverages NLP and sentiment scoring to reveal public opinion trends on tickers like AAPL, TSLA, or any stock symbol in real time.

---

## 🔍 What It Does

- 📰 Scrapes Reddit comments and threads using the PRAW API
- 💬 Analyzes sentiment using VADER and custom heuristics
- 🧹 Filters out low-quality/noisy posts
- 📈 Detects and visualizes sentiment trends over time
- 🧠 Supports enhanced signal classification (Bullish, Bearish, Neutral)

---

## 🗂️ Project Structure

```
reddit-stock-sentiment/
├── src/
│   ├── app.py                    # Main Flask or Streamlit app
│   ├── reddit_sentiment.py       # Reddit data scraping logic
│   ├── stock_data.py             # Optional: stock price data
│   ├── stock_sentiment.py        # Merges and processes final sentiment
│   ├── models/
│   │   └── sentiment_analyzer.py # Custom sentiment logic + trend detection
│   ├── visualization/
│   │   └── plotter.py            # Generates visualizations
│   └── templates/
│       └── index.html            # Frontend (for Flask version)
├── requirements.txt
├── README.md
```

---

## ⚙️ How to Run

### 1. Clone the repo and create a virtual environment

```bash
git clone https://github.com/moh1tt/reddit-stock-sentiment.git
cd reddit-stock-sentiment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
python -m textblob.download_corpora
```

### 3. Set up your Reddit API credentials in `src/config.py`

```python
client_id = "your_client_id"
client_secret = "your_client_secret"
user_agent = "your_app by /u/your_username"
```

Create these at https://www.reddit.com/prefs/apps (choose script type)

### 4. Run the app

If Flask:
```bash
python src/app.py
```

If Streamlit:
```bash
streamlit run src/app.py
```

---

## 📊 Example Outputs

- ✅ Sentiment trend plots (Bullish / Bearish / Neutral)
- 📈 Daily sentiment averages with moving averages
- 🧠 Enhanced compound score using VADER + contextual features

---

## 🚀 Features to Add Next

- 📈 Stock price overlay from Yahoo Finance
- 🧠 Fine-tuned transformer model (e.g., FinBERT)
- 🌍 Live deployment with Streamlit Cloud or Hugging Face Spaces
- 📬 Daily summary export or Telegram bot

---

## 📎 License

MIT — use and modify freely for personal or educational use.

---

> Built with ❤️ by Mohit Appari
