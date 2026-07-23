<div align="center">
  <a href="report.pdf">
    <img src="dp1.png" alt="banner" width="100%">
  </a>
  <p><em>Click the banner to view the full analysis report</em></p>
</div>

# Quantitative Derivative Pricing Project

## Overview
This project implements a comprehensive valuation framework for financial derivatives using numerical methods in Python. It was developed as part of the MSCFE 620 Derivative Pricing course. The core objective is to validate vanilla option prices, analyze sensitivities (Greeks), and simulate dynamic hedging strategies using Binomial and Trinomial trees.

## Project Structure

### 1. Binomial Tree Valuation (Step 1)
- Implemented the Cox-Ross-Rubinstein (CRR) model to price European and American Calls/Puts.
- Validated results using **Put-Call Parity**.
- Computed **Delta** and **Vega** to assess sensitivity to spot price and volatility changes.

### 2. Trinomial Trees & Convergence (Step 2)
- Extended the valuation to Trinomial Trees for faster convergence.
- Priced options across 5 distinct moneyness levels (Deep OTM to Deep ITM).
- Visualized price trends and the "Early Exercise Premium" of American Puts.

### 3. Dynamic Delta Hedging & Exotics (Step 3)
- Simulated a **Dynamic Delta Hedging** strategy to demonstrate risk neutralization.
- Verified that discrete hedging in a Binomial model yields zero hedging error (PnL = 0).
- Priced **Asian Options** (Path-dependent) via Monte Carlo simulation to demonstrate the "volatility dampening" effect compared to standard options.

## Technologies Used
- **Python 3.x**: Core logic.
- **NumPy**: Vectorized numerical operations for tree construction.
- **Pandas**: Structured data analysis for hedging logs.
- **Matplotlib**: Visualization of option surfaces and convergence graphs.

## Key Insights
1. **Put-Call Parity**: Holds strictly for European options but serves only as an inequality boundary for American options.
2. **Early Exercise**: Verified that American Puts trade at a premium to European Puts (especially when ITM) due to the interest on the strike price.
3. **Hedging**: Demonstrated that frequent rebalancing (Delta Hedging) can effectively eliminate directional risk in an option portfolio.