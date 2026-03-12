# Canadian Export Risk Analysis
### Identifying High-Risk Markets for Canadian Exporters
**Stefan Vlajich | 2026**

## Overview
This project looks at Canadian export data across four industries to 
figure out which destination markets pose the most risk for Canadian 
exporters. Trade volume data is combined with World Bank governance 
indicators to build a composite risk score for each market.

🔗 [View Interactive Dashboard](<https://public.tableau.com/app/profile/stefan.vlajich/viz/CanadianExportRiskAnalysis-SV2026/CanadianExportRiskAnalysis>)

[![Canadian Export Risk Dashboard](https://public.tableau.com/static/images/Ca/CanadianExportRiskAnalysis-SV2026/CanadianExportRiskAnalysis/1.png)](https://public.tableau.com/views/CanadianExportRiskAnalysis-SV2026/CanadianExportRiskAnalysis)

## Central Question
**Which Canadian export markets carry the highest risk-adjusted exposure, 
and where is that risk growing?**

## Key Findings
- Mexico, China, Brazil, India, and Saudi Arabia show the highest 
risk-adjusted scores, meaning Canada has significant trade exposure 
in markets with weak governance indicators
- Saudi Arabia shows an improving governance trend, falling below the 
risk threshold by 2023
- Peru shows a worsening governance trend, particularly relevant for 
Canadian agricultural exporters
- The model places the US, UK, Japan, Germany, and Australia in the 
low-risk category, which lines up with expectations and validates 
the scoring approach

## Dashboard
Built in Tableau Public with three interactive views:
- **Export Map** -> Canadian exports by destination country and industry
- **Risk Scoring Model** -> Export volume vs composite risk score, 
organized into four quadrants
- **Risk Trend Analysis** -> Risk score trends for Canada's highest-risk 
markets from 2019 to 2023

🔗 [View Interactive Dashboard](<https://public.tableau.com/app/profile/stefan.vlajich/viz/CanadianExportRiskAnalysis-SV2026/CanadianExportRiskAnalysis>)

## Data Sources
| Source | Description | Years |
|--------|-------------|-------|
| Trade Data Online (ISED) | Canadian domestic exports by industry and destination country | 2019-2023 |
| World Bank Worldwide Governance Indicators | Six governance dimensions by country | 2019-2023 |

## Methodology

### Composite Risk Score
The risk score pulls from two components:

**1. Governance Risk Score (60% weight)**
An average of six World Bank governance indicators, inverted so that 
a higher score means higher risk:
- Control of Corruption
- Government Effectiveness
- Political Stability and Absence of Violence
- Regulatory Quality
- Rule of Law
- Voice and Accountability

**2. Export Volatility (40% weight)**
Coefficient of variation (standard deviation divided by mean) of 
export values over the study period. This captures how much a trade 
relationship fluctuates year to year.

### Filters
- Only markets where Canada exports at least $10 million CAD annually
- Four industries: Agriculture, Mining and Oil and Gas, 
Utilities, Manufacturing

## Tools
- **Tableau Public** -> Dashboard and visualization
- **Python (pandas)** -> Data cleaning and country name standardization
- **Microsoft Excel** -> Data preparation

## Files
- `canada_trade_exports.csv` — Cleaned trade data from ISED
- `world_governance_indicators.csv` — World Bank governance scores
- `canadian_export_risk_analysis.twbx` — Tableau packaged workbook
