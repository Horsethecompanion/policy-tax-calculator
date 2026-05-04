# Monetary Policy "Tax" Calculator — Specification

## Core Thesis
OCR changes act as a regressive "tax" on New Zealanders — but the exposure is U-shaped across income bands:
- **Low income**: protected by benefit system / housing support. Limited direct exposure.
- **Moderate income**: MOST exposed. Too "rich" for meaningful support, but carrying debt and/or paying rising rents. Imputed rent hits them. They feel both housing price inflation AND debt servicing costs simultaneously.
- **High income**: Less exposed. Essentials are small % of spending. Investment flexibility means they can hedge in either direction.

## Income Bands
| Band | Annual Income | OCR Exposure | Support Level | Investment Flexibility |
|------|-------------|--------------|---------------|----------------------|
| Very Low | $0–30k | Minimal | High (benefits adjust) | None |
| Low | $30k–55k | Low–Moderate | Moderate (phasing out) | Minimal |
| Moderate | $55k–100k | HIGH | Minimal | Limited |
| High | $100k–180k | Moderate | None | High |
| Very High | $180k+ | Low | None | Very High |

## Exposure Factors

### 1. Rate Hike Impact (positive = cost increase)
- **Debt servicing**: mortgage holders feel increases immediately
- **Rental pressure**: landlords pass costs to tenants
- **Phase-out cliff**: moderate earners lose accommodation supplement as income rises

### 2. Rate Cut Impact (positive = cost increase, i.e. you're worse off)
- **Imputed rent**: even owner-occupiers face rising housing costs (opportunity cost of not renting)
- **Housing entry cost**: first-home buyers priced out as asset values inflate
- **Essential inflation**: food, energy, transport costs tied to housing market concentration

### 3. Government Support Phase-out
- Accommodation Supplement, Working for Families, etc. phase out as income increases
- Moderate band ($55k-100k) gets minimal support — the "squeezed middle"
- This creates a "welfare cliff" that adds to effective exposure

## Interaction Matrix
| Factor | Low Income | Moderate Income | High Income |
|--------|-----------|-----------------|-------------|
| Debt servicing | Low | HIGH | Moderate |
| Imputed rent | Low | HIGH | Moderate |
| Support phase-out | High→Moderate | Minimal | None |
| Investment flexibility | None | Limited | High |

## UI Design

### Layout
1. **Income band selector** (primary input — not exact salary)
2. **Rate direction toggle** (hike / cut / both)
3. **Results per band** — the U-curve visualization
4. **"You are here" indicator** for selected band
5. **Exposure breakdown** — which factors drive the result for your band

### Visualization
- **U-curve chart**: X-axis = income bands, Y-axis = effective "tax" (% of income)
- Bars coloured to show which exposure factors dominate
- Clear marker showing selected band

### Outputs
- Effective "tax" rate per band (% of income)
- Dominant exposure factors explained
- Narrative description of why your band is exposed this way
