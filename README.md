# Minimum Wages and Employment in the Fast-Food Industry

A replication and extension of Card and Krueger's (1994) landmark study on the employment effects of New Jersey's 1992 minimum wage increase on the fast-food industry.

# **Executive Memo: What Happens to Jobs When the Minimum Wage Goes Up?**

Rashelle Belokon  
March 2026

## **The Bottom Line**

Raising New Jersey's minimum wage by 19% in 1992 did not reduce employment at fast-food restaurants as previous economic theory dictated, but rather increased it. My replication of a landmark economics study, along with an original extension examining which types of stores were most affected, confirms that the job losses predicted by textbook economic theory did not materialize in this case.

## **What Was Studied**

On April 1, 1992, New Jersey raised its minimum wage from $4.25 to $5.05 per hour. Neighboring Pennsylvania kept its minimum at $4.25. Economists David Card and Alan Krueger surveyed 410 Burger King, KFC, Wendy's, and Roy Rogers restaurants in both states before and after the increase to measure what happened to employment. I replicated their analysis and then extended it to ask: *did the effect differ depending on the type of restaurant?*

## **How The Effect of the Minimum Wage Was Isolated**

The central challenge in policy evaluation is separating cause from coincidence. If employment changed in New Jersey after the wage increase, how do we know it was because of the policy and not because of other confounding factors? Card and Kreuger addressed this by choosing two states to sample data from with very similar baseline characteristics. New Jersey and eastern Pennsylvania share the same regional economy, the same fast-food chains, and the same consumer base. The only thing that changed on April 1, 1992 was the minimum wage in New Jersey. By comparing employment trends at restaurants on both sides of the border, we can isolate the causal effect of the wage increase from everything else that was happening at the time. 

Economists call this a "difference-in-differences" design, but the intuition is simply: same conditions, one treatment, compare the outcomes. A similar example that may be familiar is in any basic science experiment that one would do in school; you have a control group which represents your baseline before applying a change, then you have your experimental group to which you apply a change. Then, you are successfully able to see the isolated impact of that change since all other factors are held constant between your groups.

## **What Was Found: The Extension**

My original extension asked whether the employment effect was the same everywhere, or whether it varied depending on the restaurant's chain, ownership, size, or location within New Jersey. We measured each store's "wage gap" (the percentage raise it needed to comply with the new minimum) and tested whether the relationship between that gap and employment growth differed across store types.

The figure below summarizes the results. Each row shows the estimated employment effect of the minimum wage for a specific subgroup of stores, with a dot representing the best estimate and a horizontal line showing the range of statistical uncertainty (95% confidence interval). If the line crosses zero, we cannot confidently distinguish the effect from no effect. If it falls entirely to the right of zero, the wage increase was associated with employment *gains* for that group with 95% certainty, a common statistical baseline for determining whether we can confidently reject the previous economic intuition.

[Plot file](./output/hte_forest_plot.png)

*Figure: Estimated effect of the NJ minimum wage on FTE employment by store characteristic. Each point represents the GAP coefficient (the employment change associated with the proportional wage increase needed to reach $5.05) for a specific subgroup, estimated from separate interaction models with clustered standard errors. The dashed vertical line marks zero (no employment effect). Confidence intervals that do not cross zero indicate statistically significant effects. All models control for chain identity and ownership structure.*

**Three takeaways from this figure:**

1. No subgroup shows job losses. Every single estimate is either positive or statistically indistinguishable from zero. The conventional prediction that higher wages lead to fewer jobs finds no support in any slice of the data.

2. Larger stores gained the most. Restaurants that were already above the median size before the policy change experienced the strongest employment growth. This was the single most statistically significant finding in our extension (p \= 0.004), and it makes intuitive sense: bigger stores had more minimum-wage workers and thus more room for the policy to affect hiring.

3. The result is not driven by one region or one chain. The effect is broadly similar across North, Central, and South Jersey, and across franchise and company-owned stores. This rules out the concern that our finding is just an artifact of one booming local economy or one chain's expansion strategy.

## **Implications for Policy and Business**

These findings carry direct implications for stakeholders weighing the costs and benefits of minimum wage increases:

**For policymakers considering minimum wage legislation:** This evidence suggests that moderate minimum wage increases do not automatically destroy jobs in low-wage industries. The fear that a higher wage floor will trigger mass layoffs is not supported by this data. Policymakers should weigh the substantial benefits to workers (higher incomes, reduced turnover) against employment risks that did not materialize in this case. That said, these results apply to a specific case context and care should be taken in interpreting these results in terms of much larger increases or different labor markets.

**For business operators in low-wage industries:** The evidence indicates that restaurants absorbed the higher wage primarily through modest price increases rather than through workforce reductions. Operators facing a minimum wage increase should plan for cost pass-through to consumers and potential adjustments to scheduling and staffing mix, rather than assuming that layoffs are the only viable response. The finding that larger stores benefited most suggests that establishments with scale may be better positioned to absorb wage mandates.

**For future research:** The significant heterogeneity by store size and chain identity suggests that the employment effects of minimum wages are not one-size-fits-all. Future evaluations should examine how firm characteristics mediate the impact of wage policies, rather than focusing solely on average effects.

## **Methodological Note**

This analysis replicates Card and Krueger (1994), published in *The American Economic Review*, using the authors' original public-use dataset. The heterogeneous treatment effects extension, forest plot visualization, and this memo were developed with the assistance of Claude (Anthropic, claude.ai), used as a collaborative coding and writing tool. All analytical decisions and interpretations were reviewed and directed by the project author.



## Original Study

**Card, D., & Krueger, A. B. (1994).** Minimum Wages and Employment: A Case Study of the Fast-Food Industry in New Jersey and Pennsylvania. *The American Economic Review*, 84(4), 772–793.

The original paper exploits the April 1, 1992 increase in New Jersey's minimum wage from $4.25 to $5.05 per hour, using fast-food restaurants in eastern Pennsylvania (where the minimum wage remained at $4.25) as a control group. The authors surveyed 410 Burger King, KFC, Wendy's, and Roy Rogers restaurants in two waves — before (February–March 1992) and after (November–December 1992) the policy change — and found no evidence that the higher minimum wage reduced employment.

## Project Overview

This project has two parts:

### Part 1: Replication

A faithful replication of the core empirical results from Card and Krueger (1994), including:

- **Summary statistics** of key variables across New Jersey and Pennsylvania stores (Table 2)
- **Difference-in-differences estimates** of the effect of the minimum wage on full-time-equivalent (FTE) employment (Table 3)
- **Reduced-form regression models** for employment changes using the New Jersey dummy and the initial wage gap variable, with clustered standard errors (Table 4)

### Part 2: Extension — Heterogeneous Treatment Effects

An original extension examining how the employment effect of the minimum wage varies across store characteristics not explored in the original paper. The analysis interacts the GAP variable (proportional wage increase needed to reach $5.05) with four dimensions of heterogeneity:

1. **Chain identity** — Burger King, KFC, Roy Rogers, and Wendy's, testing whether the employment response differed across chains
2. **Ownership structure** — Company-owned vs. franchisee-owned stores
3. **Initial store size** — Above- vs. below-median FTE employment in wave 1
4. **Geographic subregion within New Jersey** — North, Central, South, and Shore regions

For each dimension, the extension estimates interaction models with clustered standard errors, computes subgroup-specific GAP effects using the delta method, and reports joint F-tests for heterogeneity. Results are presented in a forest plot of heterogeneous treatment coefficients with 95% confidence intervals.

#### Key Extension Findings

- **Initial store size** is the strongest moderator: larger stores experienced significantly greater employment gains (GAP × Large coefficient = 33.36, p = 0.004), consistent with the original paper's observation that proportional effects were concentrated among bigger establishments.
- **Chain identity** shows jointly significant heterogeneity (F-test p = 0.003), driven primarily by KFC stores, which had a weaker employment response — possibly reflecting their smaller average size and different labor mix.
- **Ownership structure** and **NJ subregion** show no statistically significant heterogeneity, reinforcing the original paper's identification strategy by suggesting the positive employment effect was not driven by idiosyncratic regional demand shocks or a particular ownership type.
- The core conclusion — no evidence of employment losses from the minimum wage increase — holds across every subgroup examined.

## Repository Structure

```
├── README.md
├── data/
│   ├── 01_Data_Cleaning.ipynb                  # Preliminary data cleaning code
│   └── raw/
│       └── public.dat                          # Original Card & Krueger survey data
│       └── check.sas                           # Original Card & Krueger data cleaning
│       └── codebook                            # Original Card & Krueger codebook
│       └── read.me                             # Original Card & Krueger readme
│       └── survey1.nj                          # Original Card & Krueger survey information
│       └── survey2.nj                          # Original Card & Krueger survey information
├── notebooks/
│   ├── 02_Replication_Analysis.ipynb           # Replication (Python/Colab)
│   └── 03_Extension_and_Results.ipynb          # Heterogeneous treatment effects extension
├── output/
│   ├── hte_forest_plot.png                     # Forest plot of heterogeneous effects
└── docs/
    └── Card_Krueger_1994.pdf                   # Original paper
```

## Data

The dataset is sourced from Card and Krueger's original survey of 410 fast-food restaurants. The public-use dataset is available through the [Card and Krueger data archive](https://davidcard.berkeley.edu/data_sets.html).

### Key Variables

| Variable | Description |
|---|---|
| `STATE` | 1 = New Jersey, 0 = Pennsylvania |
| `CHAIN` | Restaurant chain (1 = BK, 2 = KFC, 3 = Roy Rogers, 4 = Wendy's) |
| `CO_OWNED` | 1 = company-owned, 0 = franchisee-owned |
| `EMPTOT` | FTE employment in wave 1 (full-time + managers + 0.5 × part-time) |
| `EMPTOT2` | FTE employment in wave 2 |
| `DEMP` | Change in FTE employment (wave 2 − wave 1) |
| `WAGE_ST` | Starting wage in wave 1 |
| `WAGE_ST2` | Starting wage in wave 2 |
| `GAP` | Proportional wage increase needed to reach $5.05 (0 for PA and NJ stores already ≥ $5.05) |
| `NORTHJ`, `CENTRALJ`, `SOUTHJ`, `SHORE` | NJ subregion indicators |
| `PMEAL`, `PMEAL2` | Price of a full meal in waves 1 and 2 |
| `CLOSED` | 1 = store permanently closed by wave 2 |

## Methodology

### Replication

The primary identification strategy is a **difference-in-differences** design comparing employment changes at New Jersey restaurants (treatment) to Pennsylvania restaurants (control). An alternative within-state comparison uses the **initial wage gap** — the proportional raise required for a store to comply with the $5.05 minimum — as a continuous treatment intensity measure. Standard errors are clustered at the store level.

FTE employment is defined as: `FTE = full-time workers (including managers) + 0.5 × part-time workers`. Employment at permanently closed stores is set to zero; temporarily closed stores are treated as missing in the baseline specification.

### Extension

The heterogeneous treatment effects analysis estimates models of the form:

```
ΔE_i = α + β₁·GAP_i + β₂·(GAP_i × X_i) + γ·X_i + δ·Controls_i + ε_i
```

where `X_i` represents each store characteristic (chain dummies, ownership, size, or region). The total GAP effect for each subgroup is computed as `β₁ + β₂`, with standard errors derived via the delta method to properly account for covariance between the base and interaction terms. All models include chain and company-ownership controls with standard errors clustered by store.

## Requirements

- Python ≥ 3.8
- Key packages: `pandas`, `numpy`, `statsmodels`, `scipy`, `matplotlib`

Install dependencies:

```bash
pip install pandas numpy statsmodels scipy matplotlib
```

## How to Run

```bash
# Clone the repository
git clone https://github.com/belokonr/Minimum-Wage-Project
cd Minimum-Wage-Project

# Run the replication (or open in Google Colab / Jupyter)
jupyter notebook notebooks/02_Replication_Analysis.ipynb

# Run the heterogeneous treatment effects extension
jupyter notebook notebooks/03_Extension_and_Results.ipynb
```

## AI Tools Acknowledgment

The heterogeneous treatment effects extension (`03_Extension_and_Results.ipynb`), the forest plot visualization, the executive summary of extension findings, and this README were developed with the assistance of **Claude** (Anthropic, claude.ai). Claude was used as a collaborative coding and writing tool to design the interaction model specifications, implement the delta method for subgroup effect estimation, generate the forest plot, and draft documentation. All analytical decisions and interpretations were reviewed and directed by the project author.

## References

- Card, D., & Krueger, A. B. (1994). Minimum Wages and Employment: A Case Study of the Fast-Food Industry in New Jersey and Pennsylvania. *The American Economic Review*, 84(4), 772–793.
- Card, D., & Krueger, A. B. (1993). Minimum Wages and Employment: A Case Study of the Fast Food Industry in New Jersey and Pennsylvania. NBER Working Paper No. 4509.
- Katz, L. F., & Krueger, A. B. (1992). The Effect of the Minimum Wage on the Fast Food Industry. *Industrial and Labor Relations Review*, 46(1), 6–21.

## License

This project is for educational purposes only. The original data and study are the intellectual property of the original authors.
