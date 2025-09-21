# Real-Time Market Sentiment Analyzer

This project builds a **LangChain/Google Gemini-based pipeline** to fetch company news, analyze market sentiment, and log results to **MLflow**.

---

## Features

- Accepts a company name (e.g., "Google") as input.
- Resolves stock code using **Yahoo Finance** or a static mapping.
- Fetches recent news headlines/summaries for the company.
- Sends news to **Google Gemini (gemini-2.5-flash)** for sentiment analysis.
- Generates a **structured JSON** output with:
  - Company info, sentiment, named entities, market implications, and confidence score.
- Logs **prompt, raw model output, and structured JSON** to MLflow for tracing/debugging.
- Fully modular pipeline suitable for Jupyter notebooks or Python scripts.

---

## Tech Stack

- **Language**: Python 3.10+  
- **LLM**: Google Gemini (`google-generativeai` public API)  
- **Pipeline Framework**: LangChain  
- **Data Source**: Yahoo Finance (`yfinance`)  
- **Prompt Management & Observability**: MLflow  
- **Environment Variables**: `.env` file  

---

## Setup Instructions

1. **Clone the repository**:

```bash
git clone <repo-url>
cd <repo-folder>
