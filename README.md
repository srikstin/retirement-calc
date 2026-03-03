# Savings & Retirement Calculator AU (v1.2)

A high-precision, mobile-responsive web application for financial projections within the Australian tax landscape. Version 1.2 adds a flat Company Tax regime and continues the lightweight, table-driven interface.

## 🚀 Live Demo
Production version: [https://yourusername.github.io](https://yourusername.github.io)

## 🛠 v1.2 Engineering Updates
- **Company Tax Regime:** Added a flat 25% tax option on annual interest earnings.
- **Improved UI Feedback:** Refined green status indicators for the Tax tab to include Company and SMSF selections.
- **Audit Stability:** Standardised the periodic audit tool for easier math verification.

## 📈 Core Calculation Logic
1. **Periodic Deduction:** Annual withdrawal targets (grown by inflation) are divided by the frequency and deducted first.
2. **Periodic Compounding:** Interest is calculated on the remaining balance each period.
3. **Annual Tax Settlement:** Tax is settled once per year (15% SMSF, 25% Company, or Stage 3 Personal).
4. **Purchasing Power:** Nominal balances are deflated by the inflation rate to show "Today's Dollars."

## 📁 Repository Structure
- `index.html`: Main Calculator.
- `logic.html`: Technical documentation.
- `README.md`: Project overview and history.

## 📝 Version History
- **v1.2 (Current):** Added Company Tax (25%).
- **v1.1:** Fixed frequency-adjusted withdrawal logic; removed charting library for stability.
- **v1.0:** Initial official release.
