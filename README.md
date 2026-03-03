# Savings & Retirement Calculator AU (v1.1)

A high-precision, mobile-responsive web application designed for long-term financial projections within the Australian tax landscape. Version 1.1 focuses on mathematical accuracy across different compounding frequencies and a lightweight, table-first user interface.

## 🚀 Live Demo
Access the production version here: [https://yourusername.github.io](https://yourusername.github.io)

## 🛠 v1.1 Engineering Updates
- **Frequency-Adjusted Withdrawals:** Fixed logic to ensure the annual withdrawal total is correct regardless of compounding frequency (e.g., Annual, Quarterly, Monthly).
- **Lightweight Build:** Removed external Chart.js dependencies to guarantee 100% rendering reliability on older iOS devices and Microsoft Edge.
- **Audit Precision:** Enhanced the "Monthly/Periodic Breakdown" tool to show exact cash flow per compounding period.

## 📈 Core Calculation Logic
The engine follows a strict "Withdrawal-First" protocol:
1. **Periodic Deduction:** The annual withdrawal target is divided by the `Compounding Frequency` and deducted at the start of each period.
2. **Periodic Interest:** Interest is calculated on the remaining balance using the rate: `Monthly Rate × (12 / Frequency)`.
3. **Annual Tax:** Tax is settled once per year based on total interest earned.
4. **Purchasing Power:** The nominal year-end balance is deflated by the `Inflation Rate` to provide a "Today's Dollars" valuation.

## 📁 Repository Structure
- `index.html`: The main calculator (Tabbed UI, Vanilla JS).
- `logic.html`: Technical documentation of formulas and order of operations.
- `README.md`: Project overview and version history.

## 📝 Version History
- **v1.1 (Current):** Standardised withdrawal logic for all frequencies; removed charting library for stability.
- **v1.0:** Official release with tabbed UI, Stage 3 Tax Brackets, and Inflation logic.

## ⚖️ Disclaimer
This tool is for illustrative purposes only and does not constitute financial advice. All tax calculations are based on 2024-25 Australian Treasury standards.
