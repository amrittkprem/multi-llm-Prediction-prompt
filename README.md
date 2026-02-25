# Multi-llm-Prediction-Prompt

A curated prompt template for aggregating predictions from multiple large language models (e.g., GPT, Claude, DeepSeek) with web search enabled to estimate football match outcomes.

This project focuses on prompt engineering and LLM ensembling, not on building a statistical sports prediction model. The goal is to explore how combining multiple model outputs and web-augmented context can produce more stable, consensus-based match outcome estimates.

---

## 📌 What This Is

- A single, well-structured prompt designed to be run across multiple LLMs  
- An LLM ensemble approach: run the same prompt on different models and combine their outputs  
- A way to experiment with:
  - Prompt design  
  - Multi-model consensus  
  - Information aggregation from web-augmented LLM responses  

---

This project does not replace proper sports modeling techniques (e.g., ELO, Poisson models, xG-based regressions). It is an experiment in LLM-driven aggregation, not predictive sports science.

---

## ⚙️ How It Works

1. You provide match details:
   - Team A  
   - Team B  
   - League  
   - Match Date  

2. The same prompt is run on multiple LLMs (e.g., GPT, Claude, DeepSeek) with web search and DeepReasearch enabled(If Available).

3. Each model independently gathers and summarizes publicly available information about the match:
   - Recent form  
   - Team news  
   - Injuries/suspensions (if available)  
   - General expert/preview sentiment  

4. The outputs from each model are collected.

5. The combined outputs are fed into a final summarization prompt to produce a consensus prediction.

This acts as a meta-prediction layer over public information, not a data-driven forecasting model.

---

## ▶️ Usage

### Step 1: Fill in Match Details in the Prompt

Replace the placeholders in the prompt with real match information:

---

### Step 2: Run the Prompt on Multiple LLMs

Run the same filled-in prompt on:

- GPT (with web/browsing enabled)  
- Claude (with web search enabled)  
- DeepSeek (with online search enabled)  

---

### Step 3: Collect Model Outputs

Copy the responses from each model into a single combined input. Keep the outputs clearly labeled by model.

---

### Step 4: Final Consensus Pass

Feed the combined outputs into another LLM using a summarization or aggregation prompt to produce a final consensus prediction for:

- Likely match outcome (Home Win / Draw / Away Win)  
- High-level reasoning  

---

## 📊 Observed Behavior

- Match outcome (win/draw/loss) predictions may achieve moderate accuracy in some cases, as the models often converge toward public consensus and betting market sentiment.  
- Exact score predictions tend to be highly unreliable, which is expected given the inherent difficulty of scoreline forecasting and the lack of statistical calibration.

---

## ⚠️ Disclaimer

- Football outcomes are highly uncertain and noisy.  
- This prompt produces opinion-based, web-augmented estimates, not statistically grounded predictions.  
- Do not use this for betting, gambling, or financial decisions.  
- This project is intended for learning, experimentation, and portfolio demonstration only.

---

## 🧩 Limitations

- Outputs depend heavily on:
  - The quality of web search results  
  - The current retrieval behavior of each LLM  
- No probabilistic calibration or formal evaluation  
- Susceptible to media bias, recency bias, and market sentiment bias  

---

## 🛠️ Future Ideas

- Add a structured template so each model outputs the same fields  
- Introduce simple voting or weighting strategies for aggregation  
- Compare LLM ensemble outputs against bookmaker odds or baseline statistical models  
- Track accuracy across a larger set of matches over time  

---

## 👤 Author

Created as an experiment in:
- Prompt engineering  
- Multi-LLM ensembling  
- Consensus-based information aggregation  

This project intentionally avoids claiming predictive authority and is shared for learning and exploration.
