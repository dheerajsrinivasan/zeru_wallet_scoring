# Wallet Risk Scoring Report

## Introduction  
This report summarizes a DeFi wallet risk‐scoring exercise based on on‐chain Compound V2 interactions. Each wallet was assigned a **score from 0 (highest risk) to 1000 (lowest risk)** by modeling borrow vs. supply behavior, repayment activity, transaction volume, and method diversity.

---

## Score Distribution  
We partitioned the 0–1000 range into ten 100-point buckets:  
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

**General Observations:**  
• Most wallets fall in the mid-range buckets (300–700), indicating balanced activity.  
• Few wallets occupy the extreme low (0–100) or extreme high (900–1000) buckets, showing that very risky or very safe profiles are uncommon.

---

## Low-Scoring Wallet Behavior (0–300)  
Wallets in this segment typically exhibit:  
• High borrow-to-supply ratios (mostly borrow calls)  
• Little to no repayBorrow activity  
• Low total transaction counts  
• Minimal method diversity  

These patterns often correspond to under-collateralized or one‐off speculative activity.

---

## Mid-Range Wallets (300–700)  
“Average” wallets display:  
• A mix of supply and borrow transactions  
• Occasional repayBorrow calls  
• Moderate transaction volume  
• Use of several different Compound functions  

This reflects typical user behavior—neither overly aggressive nor overly conservative.

---

## High-Scoring Wallet Behavior (700–1000)  
Top-tier wallets show:  
• High supply ratios (majority mint/supply calls)  
• Frequent debt repayments  
• Broad method usage (multiple distinct function calls)  
• Substantial transaction volumes  

These are the most reliable participants—ideal for low-risk lending and whitelisting.

---

## Conclusion  
The 0–1000 scoring effectively segments wallets by on-chain behavior:  
- **0–300:** Risky—heavy borrowing, low collateral, minimal management  
- **300–700:** Moderate—balanced borrow/supply with some repayment  
- **700–1000:** Safe—supply-heavy, active debt management, diversified usage  

---

