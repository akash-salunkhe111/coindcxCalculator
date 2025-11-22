# CoinDCX Spot Charges Calculator

Simple browser-based tool for figuring out the real take-home profit from a CoinDCX spot trade after maker/taker fees, GST, and India’s 30 % tax on crypto gains. Built with plain HTML/CSS/JS so you can run it anywhere—no build step required.

## Features
- Breaks down target exit price, gross profit, total trading fees, GST, pre-tax profit, tax owed, and final net profit.
- Shows ROI both before and after the 30 % tax.
- Uses Indian currency formatting via `Intl.NumberFormat`.
- Mobile-friendly layout with live updates as you type.

## Fee & Tax Assumptions
- Regular CoinDCX user (not VIP).
- Spot taker fee: `0.50 %` per side (buy and sell).
- GST: `18 %` applied only to the sum of trading fees.
- Profit tax: `30 %` applied when post-fee profit is positive.

If your fee tier differs (maker rebates, VIP levels, etc.), adjust the constants in `index.html`.

## Usage
1. Open `index.html` in any modern browser (double-click the file or serve it via a static host).
2. Enter the INR amount you plan to deploy and the percentage profit target.
3. Review the breakdown card to see actual profits after every deduction.

## Initial Prompt (Cursor)
```
https://coindcx.com/fees/amp 

write a program with only js, html, css for calculating charges on input price for coindcx

consider all fees and charges

add an input for percentage profit

for eg - 

if user enters 100

and percentage profit is 10%

then you should calculate how much user will make after substracting all fees

also subtract 30% tax on profit, consider only spot, no futures and options

I am attaching fee structure as image, calculate only for normal user, not vip
```

## Model & Tools
- Model: `GPT-5.1 Codex`
- Environment: Cursor (macOS)

## Development
No dependencies beyond a browser. If you want live reload while iterating:
```bash
cd /Users/akash.salunke/Desktop/coindcxCalculator
npx serve .
```
Then open the provided localhost URL.

Contributions welcome—feel free to open an issue or PR with improvements (more fee tiers, downloadable results, etc.).
# coindcxCalculator
