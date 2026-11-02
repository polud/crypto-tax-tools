# Crypto Tax Tools

Free calculators for Canadian crypto tax: pooled ACB across exchanges, superficial losses, capital gains. Each page runs entirely in the browser; nothing is uploaded.

Live site: https://polud.github.io/crypto-tax-tools/

| Calculator | What it answers | Main rule |
| --- | --- | --- |
| [ACB Pool Calculator](https://polud.github.io/crypto-tax-tools/acb-pool/) | Adjusted cost base, gain or loss per sale and per tax year when the same coin is held on several exchanges and wallets | ITA s.47 (identical properties) |
| [Superficial Loss Calculator](https://polud.github.io/crypto-tax-tools/superficial-loss/) | How much of a loss is denied after buying back within 30 days, and how much is added to cost | ITA s.54, s.40(2)(g)(i), s.53(1)(f) |

## How the numbers are computed

- Exact decimal arithmetic in the browser (no floating-point rounding in the tax figures).
- The partial superficial-loss formula is the one in CRA Technical Interpretation 2004-0073011E5: denied loss = min(S, P, B) ÷ S × L.
- Results were checked against a reference implementation on generated test cases: 312 superficial-loss cases and 512 ACB runs (4,110 trades, 264 superficial-loss events), with no differences.

## Layout

```
index.html               home page listing the calculators
acb-pool/index.html      ACB Pool Calculator (self-contained)
superficial-loss/index.html
og/                      1200×630 preview images for social cards
favicon.svg
```

Each calculator is a single self-contained HTML file. To update one, replace its `index.html` and commit; GitHub Pages republishes in a minute or two.

## Disclaimer

General information, not tax or legal advice. Check results against your own records before filing.
