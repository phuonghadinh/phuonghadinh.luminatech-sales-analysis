# Data

The raw transaction files are **not included** in this repository. They were provided for coursework and are too large for GitHub (about 870 MB in total).

## Files needed

| File | Contents |
|---|---|
| `2023.csv` | Sales transactions, January–December 2023 (~1.04M rows, 38 columns) |
| `2024.csv` | Sales transactions, January–December 2024 (~0.95M rows, 39 columns) |

Place both files in this `data/` folder before running the notebooks:

```
data/
├── 2023.csv
├── 2024.csv
└── README.md
```

## Key fields used

| Field | Description |
|---|---|
| `accounting_date` | Transaction date (YYYYMMDD) |
| `customer_code` | Anonymised customer identifier |
| `company_code` | Selling company; company 950 (NZD business) has no customer codes |
| `item_type` | Product type (1–9) |
| `business_chain_l1_name` | Customer's business chain |
| `order_type_code` | Order type; CRD, CRR, CDG and ZCG are credits or returns |
| `value_sales`, `value_cost` | Sales and cost in the transaction currency |
| `currency` | AUD (also coded AUS), NZD, USD, EUR |
| `value_price_adjustment` | 1 if the line had a price adjustment |
| `invoice_number` | Invoice identifier |

## Currency conversion

Sales and cost are converted to AUD with fixed rates (1 AUD = 0.65 USD, 1.13 NZD, 0.49 EUR).
