# Wallet Risk Scoring Report

## Introduction  
I built a DeFi wallet risk-scoring model that assigns each wallet a **score from 0 (highest risk) to 1000 (lowest risk)**. I base this score on on-chain Compound V2 behavior—borrow vs. supply ratios, repayment activity, transaction volume, and method diversity.

---

## How I Got the Data  
I fetched each wallet’s full transaction history using the **Etherscan API**. From those transactions, I filtered for calls to known Compound V2 contracts (cTokens and the Comptroller) to isolate all relevant borrow, supply, repay, and redemption events.

---

## Score Distribution  
I divided the 0–1000 range into ten 100-point buckets:  
• 0–100  
• 100–200  
• 200–300  
• 300–400  
• 400–500  
• 500–600  
• 600–700  
• 700–800  
• 800–900  
• 900–1000  

**What I Observed:**  
• Most wallets fall in the mid-range buckets (300–700), indicating balanced activity.  
• Few wallets occupy the extreme low (0–100) or extreme high (900–1000) buckets, so very risky or very safe profiles are uncommon.

---

## Low-Scoring Wallet Behavior (0–300)  
Wallets scoring in this segment typically show:  
• High borrow-to-supply ratios (mostly borrow calls)  
• Little to no repayBorrow activity  
• Low total transaction counts  
• Minimal method diversity  

These patterns suggest under-collateralized or one-off speculative activity.

---

## Mid-Range Wallets (300–700)  
“Average” wallets exhibit:  
• A mix of supply and borrow transactions  
• Occasional repayBorrow calls  
• Moderate transaction volume  
• Use of several different Compound functions  

This reflects typical user behavior—neither overly aggressive nor overly conservative.

---

## High-Scoring Wallet Behavior (700–1000)  
Top-tier wallets demonstrate:  
• High supply ratios (majority mint/supply calls)  
• Frequent debt repayments  
• Broad method usage (multiple distinct function calls)  
• Substantial transaction volumes  

These wallets are the most reliable—ideal candidates for low-risk lending or whitelisting.

---

## Conclusion  
This 0–1000 scoring effectively segments wallets by on-chain behavior:  
- **0–300:** Risky—heavy borrowing, low collateral, minimal management  
- **300–700:** Moderate—balanced borrow/supply with some repayment  
- **700–1000:** Safe—supply-heavy, active debt management, diversified usage  

---


