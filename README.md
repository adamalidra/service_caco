# service_caco
CACO Calculator — Service Specific Conditional ACO

## Structure

This is a static HTML-only project (no build step required).

| File | Description |
|------|-------------|
| `index.html` | Landing page — links to both calculator versions |
| `index-v1.html` | **v1** — Original calculator with seller-configured target option |
| `index-v2.html` | **v2** — ACD / Net-Invoice calculator (newer flow) |

## Calculator Versions

### v1 (`index-v1.html`)
The original calculator. Uses a direct baseline spend as the starting point.
- Enter the customer's current annual Azure spend (baseline)
- Choose auto target (1.20× baseline, $20K minimum) or seller-configured target
- Plan 4 milestones with target spend and ACO amounts
- Validates against program floor and milestone ordering rules

### v2 (`index-v2.html`)
Adds Azure Commitment Discount (ACD) support. The ACO math is based on the net invoice after ACD is deducted from gross consumption.
- Enter gross consumption and optional ACD (percentage or fixed amount)
- Net invoice = gross − ACD becomes the billing baseline for ACO
- Auto or seller-configured target mode
- Same 4-milestone planning table with ACD-aware baseline

## Usage

Open `index.html` in a browser to see the landing page and select a version, or open either version directly.
