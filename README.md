# Finland Crypto FIFO Tax Calculator

A single-file, client-side web app for calculating Finnish crypto capital gains tax (pääomatulovero) using the FIFO method, as required by Vero (Finnish Tax Administration).

## Features

- **FIFO calculation** — oldest purchases are treated as sold first, per KHO 2024:123
- **Hankintameno-olettama (HMO)** — acquisition cost presumption applied automatically when it reduces tax (20% for holdings under 10 years, 40% for 10+ years), calculated per FIFO lot
- **€1,000 small disposal exemption** — gains are tax-exempt when annual proceeds are €1,000 or less (TVL 48 §)
- **Capital loss tracking** — losses shown with carry-forward note (deductible for 5 years)
- **Tax breakdown** — 30%/34% split at €30,000 threshold
- **PDF export in Finnish** — print-ready report for your records or submission
- **CSV import/export** — bulk import transactions, export for backup
- **No server, no dependencies** — everything runs in the browser; data stored in localStorage

## Usage

Open `finland_crypto_fifo_calculator.html` in any modern browser. No installation needed.

1. **Transactions tab** — add each purchase and sale in EUR (including fees)
2. **Results tab** — select a tax year to see your gain/loss breakdown and estimated tax
3. **Export** — generate a Finnish-language PDF report or export your transactions as CSV

### Crypto-to-crypto swaps

Trading one cryptocurrency for another is a taxable event in Finland. Enter it as:
1. A **sell** of the coin you gave up, at its EUR market value on the day of the swap
2. A **buy** of the coin you received, at the same EUR value

### CSV import format

```
type,date,asset,amount,total_eur,notes
buy,2022-01-15,BTC,0.5,15000,Coinbase
sell,2023-06-10,BTC,0.2,8000,
```

## Disclaimer

This tool provides estimates only. Tax rules can change and individual circumstances vary. Always verify your figures and report gains and losses in OmaVero under **Pääomatulot → Luovutusvoitot ja -tappiot**. Keep all records for 6 years.
