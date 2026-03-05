# CLAUDE.md — Retirement Calculator AU

## Overview

A zero-dependency, single-file HTML application for modelling Australian retirement savings scenarios. No build step, no package manager, no external libraries — everything runs directly in the browser.

## File Structure

| File | Purpose |
|------|---------|
| [index.html](index.html) | Complete application — markup, styles, and calculation logic |
| [logic.html](logic.html) | Technical documentation explaining the calculation methodology |
| [README.md](README.md) | Project overview and version history |

## How It Works

The calculator has four input tabs (Investment, Tax, Withdrawals, Inflation) and produces an annual results table plus a per-period audit view.

Each year is calculated in this sequence:
1. **Opening balance** — principal for year 1, previous year's inflation-adjusted balance thereafter
2. **Withdrawal growth** — monthly withdrawal indexed by inflation
3. **Periodic compounding** — interest compounded at the selected frequency, withdrawals deducted each period
4. **Tax settlement** — annual interest taxed under the selected regime at year end
5. **Inflation deflation** — balance expressed in today's dollars

## Tax Regimes

| Regime | Rate |
|--------|------|
| Personal | Progressive 2024-25 AU brackets (16%–45%) + optional 2% Medicare levy |
| SMSF | 15% flat (0% in pension phase) |
| Company | 25% flat |
| No Tax | 0% |

## Technology

Vanilla HTML5, CSS3, and ES6+ JavaScript. Australian dollar formatting via `toLocaleString('en-AU')`. Mobile-optimised with `inputmode="decimal"` on numeric inputs.
