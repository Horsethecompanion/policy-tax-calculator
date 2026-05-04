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

## Income Bands
| Band | Annual Income | OCR Exposure | Support Level | Investment Flexibility |
|------|-------------|--------------|---------------|----------------------|
| Very Low | $0–30k | Minimal | High (benefits adjust) | None |
| Low | $30k–55k | Low–Moderate | Moderate (phasing out) | Minimal |
| Moderate | $55k–100k | HIGH | Minimal | Limited |
| High | $100k–180k | Moderate | None | High |
| Very High | $180k+ | Low | None | Very High |

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
- Stats NZ Household Living-costs Price Indexes (HLPIs) — differential inflation by income quintile
- Stats NZ Household Income and Housing Cost Statistics (HES/HILS)
- RBNZ research on monetary policy distributional effects
- Geoff Bertram (2021): "How Neoliberalism Doubled the Price of Electricity"
- Note: coefficients are calibrated to thesis; actual HLPI weight data by quintile should be incorporated for precision
