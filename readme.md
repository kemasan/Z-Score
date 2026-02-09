# 📈 Market Anomaly Detection: Rolling Z-Score Framework

### 🎯 The Business Question: "How can we identify statistically significant price deviations to detect market manipulation or extreme over/undervaluation?"
In high-volatility markets (like Crypto and Tech stocks), price "noise" makes it hard to see real risks. This project provides a mathematical tool to filter that noise and identify anomalies—events that happen in the outer 5% of historical probability.

<img width="1322" height="610" alt="Screenshot 2026-02-09 at 15 47 24" src="https://github.com/user-attachments/assets/a593dcad-feec-4b75-b0af-2c6704a6bd74" />

### 📊 Methodology
I developed a Python-based framework that transforms raw price data into a Normal Distribution model using: 
  - Rolling Mean & Standard Deviation:To account for changing market conditions.
  - Normalization: Calculating Z = (Price - Rolling Mean \mu) / Standard Deviation \sigma$ to compare different assets on a single scale.

### 🧠 Strategic Assumptions
1. Mean Reversion: I assume prices eventually return to their historical average after an extreme event.
2. The 95% Rule: I define any price move with a Z-score beyond +/-2.0 as a critical anomaly requiring investigation.
3. Time Windows: I analyzed 30, 60, and 90-day windows to balance short-term "spikes" against long-term trend shifts.

### ⚖️ Risk Trade-offs & Analysis
  - Sensitivity vs. Accuracy (The 80/20 Rule): * A 30-day window catches risks faster but produces more "false alarms."
    - A 90-day window is more reliable for major trends but can be slow to react to a "flash crash.
  - "Threshold Adjustment: * Using a 1.5 threshold increases the "Buy/Sell" signals by 30%, but lowers the quality of the intelligence. I focus on 2.0 to ensure only the most significant risks are flagged.

[PLACEHOLDER: Insert a screenshot of your Z-score "Signals" (the dots on the chart) here]


### 🔄 Sensitivity Analysis
  - Conclusion Change: If the market enters a period of "Hyper-volatility" (e.g., a Black Swan event), the Z-score logic may fail as the "Standard Deviation" expands too fast.
  - Actionable Insight: This tool is best used as an early-warning system alongside OSINT (social media monitoring) to confirm if a price drop is a technical glitch or a fundamental protocol failure.
    
### 🛠️ Tech StackLanguage: 
  - Python
  - Libraries: Pandas, Matplotlib, yFinance
  - Environment: Jupyter Notebook / VSCode




