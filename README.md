# Savings & Retirement Calculator AU (v1.3)

A high-precision, mobile-responsive web application for financial projections within the Australian tax landscape. Version 1.3 adds recurring monthly contributions with an optional stop year.

## 🚀 Live Demo
Production version: [https://yourusername.github.io](https://yourusername.github.io)

## 🛠 v1.3 Engineering Updates
- **Monthly Contributions:** Added a monthly contribution input to model DCA/accumulation phases.
- **Stop Contributing at Year:** Contributions can be halted at a specified year (0 = never stop), enabling accumulation-then-withdrawal scenarios.
- **Contrib Column:** Annual and per-period contribution totals are shown in the results and audit tables.
- **Tab Indicator:** The Investment tab shows a green dot when a contribution is active.

## 📈 Core Calculation Logic
Each period executes in this order:
1. **Periodic Contribution:** Monthly contribution (scaled to the period) is added to the balance first, so it earns interest immediately.
2. **Periodic Deduction:** Annual withdrawal targets (grown by inflation) are divided by the frequency and deducted next.
3. **Periodic Compounding:** Interest is calculated on the remaining balance.
4. **Annual Tax Settlement:** Tax is settled once per year (15% SMSF, 25% Company, or Stage 3 Personal).
5. **Purchasing Power:** Nominal balances are deflated by the inflation rate to show "Today's Dollars."

## 📁 Repository Structure
- `index.html`: Main Calculator.
- `logic.html`: Technical documentation.
- `README.md`: Project overview and history.

## 📝 Version History
- **v1.3 (Current):** Added monthly contributions with optional stop year.
- **v1.2:** Added Company Tax (25%).
- **v1.1:** Fixed frequency-adjusted withdrawal logic; removed charting library for stability.
- **v1.0:** Initial official release.
