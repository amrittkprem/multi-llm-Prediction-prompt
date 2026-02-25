# multi-llm-Prediction-prompt

A curated prompt template for aggregating predictions from multiple large language models (e.g., GPT, Claude, DeepSeek) using web search to estimate football match outcomes.

This project focuses on **prompt engineering and LLM ensembling**, not on building a statistical sports prediction model. The goal is to explore how combining multiple model outputs and web-augmented context can produce more stable, consensus-based match outcome estimates.

---

## 📌 What This Is

- A single, well-structured **prompt** designed to be run across multiple LLMs  
- An **LLM ensemble approach**: run the same prompt on different models and combine their outputs  
- A way to experiment with:
  - Prompt design
  - Multi-model consensus
  - Information aggregation from web-augmented LLM responses  

---

## ❌ What This Is Not

- Not a machine learning model trained on historical match data  
- Not a statistical sports analytics system  
- Not a reliable or calibrated betting tool  
- Not guaranteed to be accurate  

This project does **not** replace proper sports modeling techniques (e.g., ELO, Poisson models, xG-based regressions). It is an experiment in **LLM-driven aggregation**, not predictive sports science.

---

## ⚙️ How It Works

1. Run the same prompt on multiple LLMs (e.g., GPT, Claude, DeepSeek) with web search enabled.
2. Each model independently summarizes relevant information about the match:
   - Recent form
   - Team news
   - Injuries/suspensions (if available)
   - General expert/preview sentiment
3. Collect the outputs.
4. Feed the combined responses into a final summarization prompt to produce a consensus prediction.

This acts as a **meta-prediction layer over public information**, not a data-driven forecasting model.

---

## ▶️ Usage

### Step 1: Copy the Prompt
Use the prompt provided in this repository.

### Step 2: Run on Multiple LLMs
Run the same prompt on:
- GPT (with browsing / web tools enabled)
- Claude (with web search enabled)
- DeepSeek (with online search enabled)

### Step 3: Aggregate Outputs
Copy the outputs from each model and combine them.

### Step 4: Final Consensus Pass
Feed the combined responses into another LLM using a summarization prompt to produce a final consensus prediction.

---

## 📊 Observed Behavior

- Match outcome (win/draw/loss) predictions may achieve **moderate accuracy** in some cases, as the models often converge toward public consensus and betting market sentiment.
- Exact score predictions tend to be **highly unreliable**, which is expected given the inherent difficulty of scoreline forecasting and the lack of statistical calibration.

---

## ⚠️ Disclaimer

- Football outcomes are highly uncertain and noisy.
- This prompt produces **opinion-based, web-augmented estimates**, not statistically grounded predictions.
- Do **not** use this for betting, gambling, or financial decisions.
- This project is intended for:
  - Prompt engineering experiments  
  - LLM behavior analysis  
  - Educational and portfolio purposes  

---

## 🧩 Limitations

- Outputs depend heavily on:
  - The quality of web search results
  - The current training and retrieval behavior of each LLM
- No probabilistic calibration or formal validation
- Susceptible to:
  - Media bias
  - Recency bias
  - Market sentiment bias

---

## 🛠️ Future Ideas

- Add a structured template for extracting comparable signals from each model  
- Introduce simple voting or weighting strategies for aggregation  
- Compare LLM ensemble outputs against bookmaker odds or baseline statistical models  
- Build a small evaluation set to track outcome accuracy over time  

---

## 👤 Author

Created as an experiment in:

- Prompt engineering  
- Multi-LLM ensembling  
- Consensus-based information aggregation  

This project intentionally avoids claiming predictive authority and is shared for learning and exploration purposes.
