# Monetary Policy "Tax" Calculator — Specification

## Core Thesis
In Aotearoa's modern economy, wealth is increasingly held in assets rather than productivity. When the Reserve Bank changes the OCR, it doesn't create inflation — but in an economy structured around asset ownership, its effects are **highly regressive**. This calculator shows roughly what the OCR "tax" — the increase in essential living costs caused by OCR changes — amounts to for different income bands.

**The tool does NOT claim:**
- That OCR changes cause inflation
- That all inflation is OCR-manufactured

**The tool DOES show:**
- That the OCR mechanism, as a transmission belt for economic adjustment, redistributes costs regressively
- That moderate-income households bear the highest "tax" because they can't avoid essential cost exposure, have no meaningful government support, and can't flex investments to benefit from both directions

## Key Framing
- **OCR ≠ inflation.** The RBNZ uses OCR to target an inflation rate that is itself partly a product of how the economy is structured.
- **OCR mechanism ≠ neutral.** The transmission of OCR changes into essential living costs falls regressively.
- **The "tax" =** % increase in essential costs per 1% OCR change, expressed as % of annual income.

## Actual Stats NZ HLPI Data (2024 — Income Quintiles)

Expenditure weights by income quintile (Stats NZ HLPI, 2024):

| Category | Q1 (Lowest 20%) | Q2 | Q3 (Moderate) | Q4 | Q5 (Highest 20%) |
}|----------|----------------|----|----|----|----|
| Food | 21.2% | 20.0% | 19.9% | 18.8% | 17.9% |
| **Housing** | **27.9%** | **30.7%** | **24.2%** | **20.0%** | **16.7%** |
| Transport | 10.4% | 11.8% | 12.5% | 13.9% | 14.1% |
| Health | 3.5% | 3.0% | 3.2% | 2.6% | 2.9% |
| Communication | 3.7% | 3.6% | 3.4% | 3.1% | 2.7% |
| **Essential Total** | **66.7%** | **69.1%** | **63.2%** | **58.4%** | **54.3%** |
| Alcohol & Tobacco | 6.0% | 4.8% | 4.9% | 4.9% | 4.7% |
| Recreation | 7.3% | 6.7% | 7.2% | 8.6% | 9.6% |
| Interest payments | 2.6% | 3.5% | 7.2% | 9.9% | 10.6% |

**Key findings:**
- Q2 has the HIGHEST essential spending burden (69.1%) and HIGHEST housing weight (30.7%) — not Q3 as initially hypothesised
- Q3 (moderate, $55k–$100k) follows at 63.2% essential spending, 24.2% housing
- Q2 likely captures first-home buyers at their most stretched: small deposits, short fixed-rate mortgages, support phasing out
- Housing weight in HLPI = rent only; actual OCR exposure for owners includes mortgage costs (excluded from CPI)


## Income Bands (Updated)
| Band | Annual Income | Quintile | Essential Spending | Housing Weight | Support | Investment Flex | OCR Tax/100bp |
|------|-------------|----------|-------------------|----------------|---------|-----------------|-------------|
| Very Low | $0–30k | Q1 | 66.7% | 27.9% | High | None | ~0.8% |
| Low | $30k–55k | Q2 | **69.1%** | **30.7%** | Phasing out | Minimal | ~1.6% |
| Moderate | $55k–100k | Q3 | 63.2% | 24.2% | Minimal | Limited | ~1.4% |
| High | $100k–180k | Q4 | 58.4% | 20.0% | None | High | ~0.8% |
| Very High | $180k+ | Q5 | 54.3% | 16.7% | None | Very High | ~0.3% |

## The CPI Gap — Why This Matters

**Official CPI excludes mortgage costs.** Only rent is included in the housing component. This is methodologically correct (CPI measures consumption, not wealth), but it creates a systematic blind spot:

- ~60% of NZ households are owner-occupiers
- Mortgage payments are directly determined by the OCR (via the banking system's lending rates)
- When OCR rises → mortgage rates rise → actual household costs rise
- This rise is NOT reflected in official CPI inflation figures

**Result:** The true OCR "tax" on owner-occupier households is never fully measured. For Q2/Q3 households with heavy mortgage debt, the gap between measured inflation and actual cost burden is largest.

## Exposure Factors

### 1. Debt Servicing (🏦)
- Mortgage holders feel rate changes immediately in payment amounts
- Renters feel indirectly via landlord cost pass-through
- Moderate band: high debt relative to income, most exposed

### 2. Imputed Rent / Housing Cost Risk (🏠)
- Even owner-occupiers face the "imputed rent" of their housing — if they had to rent their home, what would it cost?
- Rate cuts inflate this imputed cost (house prices rise = renting is more expensive)
- Rate hikes reduce it (house prices fall, but debt servicing costs rise)

### 3. Social Safety Net (🛡️)
- Government support (accommodation supplement, Working for Families) cushions some groups
- Moderate band: mostly phased out, no cushion

### 4. Investment Flexibility (📊)
- High income can shift investments: bonds benefit from rate hikes, equities/property from rate cuts
- Moderate income: some savings but limited ability to hedge both directions

### 5. Market Concentration / Essential Services (⚡)
- Privatised essential services (power, insurance, internet) raise prices regardless of OCR direction
- Because market concentration means "inflation" gets passed on even when input costs fall
- Evidence: residential electricity prices up 79% since 1990 (post-privatisation) — Geoff Bertram, *How Neoliberalism Doubled the Price of Electricity*
- Moderate band is most exposed (can't avoid, can't switch, no negotiating power)

## Data Sources
- **Stats NZ HLPI 2024** — differential expenditure weights by income quintile, incorporated directly into model coefficients (source file: `hlpi-weights.csv`)
- **Geoff Bertram (2021)**: "How Neoliberalism Doubled the Price of Electricity" — residential electricity prices +79% since 1990 post-privatisation
- **RBNZ** — historical OCR data, house price responsiveness to rate changes
- **RBNZ servicing test** — ~$140k income needed to service $1.2M mortgage at 2.5%
- **Note:** coefficients are now calibrated to actual Stats NZ HLPI 2024 quintile data
