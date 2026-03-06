# Savings & Retirement Calculator AU (v1.6)

A high-precision, mobile-responsive web application for financial projections within the Australian tax landscape. Version 1.6 adds an interactive balance chart below the results table.

## 🚀 Live Demo
Production version: [https://yourusername.github.io](https://yourusername.github.io)

## 🛠 v1.6 Engineering Updates
- **Balance Chart:** Added a Canvas-based line chart below the results table showing inflation-adjusted ending balance per year. No external libraries — pure Canvas 2D API. Redraws automatically on input changes and theme toggles. HiDPI/retina-aware via `devicePixelRatio`.
- **Dark / Light Theme Toggle:** Added a moon/sun button in the page header to switch between dark and light themes, with the preference persisted in `localStorage`.
- **Summary Tax Label:** The summary bar now shows "No tax" as plain text (no amount) when the No Tax regime is selected, and displays the full label + compact amount for all other regimes.

## 🛠 v1.5 Engineering Updates
- **Merged Tax & Inflation Tab:** Combined the separate Tax and Inflation tabs into a single "Tax & Inflation" tab for a simpler, more compact UI — especially beneficial on mobile devices.
- **Unified Indicator:** The "Tax & Inflation" tab now shows the active-input green dot when either a non-zero tax regime or a non-zero inflation rate is set.

## 🛠 v1.4 Engineering Updates
- **Compact Summary:** Ending Balance and Total Tax in the summary bar now display in abbreviated K/M format (e.g. $1.23M) for quick scanning.
- **Row Colour-Banding:** Table rows are tinted green when the inflation-adjusted balance grew year-on-year, red when it declined.
- **Sticky Headers:** The results table header row stays visible while scrolling vertically within the results panel.
- **Sticky Year Column:** The Year column sticks to the left edge when scrolling horizontally on small screens.
- **Milestone Rows:** Every 5th year (Yr 5, 10, 15…) is emphasised with a bolder top border for easy navigation.

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
- **v1.6 (Current):** Canvas balance chart, dark/light theme toggle, improved summary tax label.
- **v1.5:** Merged Tax and Inflation tabs into a single "Tax & Inflation" tab for simplified mobile-friendly UI.
- **v1.4:** Output presentation improvements — compact summary (K/M), colour-banded rows, sticky headers, sticky Year column, milestone row markers.
- **v1.3:** Added monthly contributions with optional stop year.
- **v1.2:** Added Company Tax (25%).
- **v1.1:** Fixed frequency-adjusted withdrawal logic; removed charting library for stability.
- **v1.0:** Initial official release.
