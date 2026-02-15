# Savings & Retirement Calculator AU (v1.0)

A mobile-responsive web application designed to project long-term financial growth within the Australian tax landscape. This tool accounts for compound interest, inflation-adjusted withdrawals, and various tax regimes including SMSF and Personal Stage 3 brackets.

## 🚀 Live Demo
You can access the calculator here: [https://yourusername.github.io](https://yourusername.github.io)

## 🛠 Features
- **Monthly Compounding Engine:** Calculates interest and withdrawals on a monthly basis for higher precision.
- **Inflation Adjustment:** 
  - Deflates the ending balance to show "Today's Dollars" (Purchasing Power).
  - Automatically grows withdrawal amounts annually to keep up with the cost of living.
- **Australian Tax Integration:**
  - **SMSF:** 15% concessional tax with a toggle for Pension Phase (0%).
  - **Personal:** Current 2024-25 Stage 3 Tax Brackets with an optional 2% Medicare Levy.
- **Audit Tool:** A built-in "Monthly Breakdown" feature to verify the math for any specific year.
- **Mobile First Design:** Tabbed interface optimized for iOS and Android devices.

## 📈 Calculation Logic
The engine follows a strict order of operations each month:
1. **Withdrawal First:** Funds are removed at the start of the period.
2. **Interest Second:** Interest is calculated on the *remaining* balance.
3. **Annual Tax:** Tax is settled at the end of each 12-month cycle.
4. **Deflation:** The final annual balance is adjusted by the inflation rate before starting the next year.

## 📁 Repository Structure
- `index.html`: The main application (HTML5, CSS3, Vanilla JavaScript).
- `logic.html`: Detailed documentation of the mathematical formulas and sequence.
- `README.md`: Project overview and setup instructions.

## 📝 Version History
- **v1.0 (Current):** Official release with tabbed UI, green status indicators, and inflation-linked withdrawal growth.
- **v0.5-Beta:** Initial testing of Stage 3 tax logic and monthly compounding.

## ⚖️ License
This project is for educational and illustrative purposes only. It does not constitute financial advice.
