# Pricing Experimentation and Margin Optimization

> Executive decision-support portfolio project using synthetic data.

**Interactive beta:** https://akhan303.github.io/Pricing-Experimentation-Margin-Optimization/

![Illustrative pricing experiment preview](docs/project-preview.png)

## Business objective

Help commercial and finance leaders evaluate pricing actions without treating margin improvement as a single-variable decision. The framework tests the relationship among price, customer response, volume, revenue and gross-margin dollars so leadership can distinguish a promising pricing move from a risky one.

## Corrected experiment design

The current notebook assigns each customer to Treatment or Control **before the pre-period** and preserves that assignment across both pre and post periods. This persistent assignment is required for a valid Difference-in-Differences design and replaces the earlier draft structure in which group identity was only populated in the post period.

The synthetic experiment includes:

- 2,000 customers: 1,000 Retail and 1,000 Distributor
- 16,000 customer-week observations
- Four pre-period weeks and four post-period weeks
- A 5% treatment price increase
- Retail elasticity assumption of -1.8
- Distributor elasticity assumption of -1.2
- Control customers with unchanged price

## Analytical capabilities

- Treatment and control performance comparison
- Pre/post segment-level price, demand, revenue and gross-margin views
- Welch statistical significance testing
- Difference-in-Differences estimation
- Price-elasticity diagnostics
- Interactive scenario analysis in the public beta
- Decision-ready interpretation and governance limits

## Executive result from the synthetic experiment

Under the modeled assumptions, the 5% price increase reduces demand enough that gross-margin dollars decline rather than improve. The effect is more pronounced in Retail, where demand is more elastic, than in Distributor.

The conclusion is not that price increases are inherently unattractive. The decision lesson is that pricing actions should be tested by segment and evaluated on contribution, volume and customer response before broad rollout.

## Governance and privacy

This project is built entirely with synthetic data. It contains no employer, client, customer, product, pricing or transaction information. Statistical significance is not treated as a standalone rollout decision; commercial context, customer response, competitive conditions and qualified human judgment remain necessary.

## Run the notebook

1. Install the packages in `requirements.txt`.
2. Open `Pricing_Experimentation_&_Margin_Optimization.ipynb`.
3. Run the notebook from top to bottom to reproduce the corrected experiment, analysis and visuals.

## Technology and analytical methods

Python, pandas, NumPy, SciPy, statsmodels, matplotlib, seaborn, controlled experimentation, Welch t-tests, Difference-in-Differences, price elasticity, scenario analysis.

---

Created by [Aftab Khan](https://www.linkedin.com/in/aftabparvezkhan/) as part of a finance, data, analytics and AI decision-intelligence portfolio.