# Capital Gains Tax (CGT) Tracker & Dashboard

A lightweight Python tool designed to track share and ETF tax parcel allocations, calculate capital gains under ATO guidelines, and render dynamic HTML summaries directly inside Jupyter Notebooks.

> **Disclaimer**  
> *This tool is a personal project built for educational and demonstration purposes only. It does not constitute financial, accounting, or tax advice. Always verify tax calculations independently or consult a registered tax agent before lodging returns with the ATO.*

---

### Overview
This notebook automates the calculation of **CGT** for Australian shares.

It imports trade history from a CSV export, tracks individual purchase parcels, applies optimal parcel selection strategies (Highest-Cost-First) and automatically applies the **50% CGT discount** for holdings held over 12 months (365 days).

---

### Key features
* Automatic CSV import; Reads buy and sell confirmations directly from broker exports.
* Chronological auto-sorting: Trades are processed in exact historical order regardless of CSV row order.
* Tax minimisation (HIFO) strategy: Allocates sales against highest cost base parcels first to reduce taxable capital gains.
* ATO myTax ready output: Prints final totals mapped directly to the **Total Current Year Capital Gains** and **Net Capital Gains** fields on myTax.

---

## Setup & Usage

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/josiefft/python-finance-projects.git](https://github.com/josiefft/python-finance-projects.git)
   cd python-finance-projects/"Tax tracker"
