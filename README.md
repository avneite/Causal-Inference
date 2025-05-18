# Causal Inference Assignments Portfolio

This repository contains a curated collection of assignments completed for the **Causal Inference** course (Spring 2025) at the University of Minnesota. Each assignment applies a distinct causal inference method to a real-world dataset, emphasizing careful assumption checking, statistical interpretation, and actionable insights.

The analyses were conducted in **R** and emphasize a blend of experimental and quasi-experimental designs. All assignments were completed in collaboration with Harshal Sable.

---

## Contents

| File | Title | Key Methods |
|------|-------|-------------|
| Assignment-1.pdf | Reddit Gold Experiment & Balsakhi Education Program | T-tests, Linear Regression |
| Assignment-2.pdf | Digital Ad Attribution at Star Digital | Logistic Regression, Power Analysis, Cost-Effectiveness |
| Assignment-3.pdf | Natural Experiment: Google Ad Suspension | Difference-in-Differences |
| Assignment-4.pdf | Directed Search, Policy Intervention, and Ad Ranking | Propensity Score Matching, Synthetic Control, Regression Discontinuity |

---

## Assignment Summaries

### Assignment-1 – Experimental and Observational Inference

**Part 1: Reddit Gold Experiment**  
We tested whether receiving Reddit Gold causally increases user posting behavior. After confirming covariate balance using t-tests across tenure, premium user status, and post history, we fit linear models to test treatment effects. We also examined interaction effects for new users and assessed the plausibility of SUTVA.

**Part 2: Balsakhi Remedial Education Program**  
Using education data from Indian schools, we tested the impact of the Balsakhi tutoring intervention on math and language scores. We confirmed randomization by checking baseline score balance and conducted post-intervention t-tests. The analysis also included a discussion of potential SUTVA violations due to spillover effects.

---

### Assignment-2 – Digital Advertising Effectiveness

**Context:** Star Digital wanted to measure the effect of online display advertising on user purchases across six websites.

- We balanced an initially skewed test-control split through stratified sampling.
- Logistic regression showed that ad exposure led to a statistically significant increase in purchase probability (~12% lift).
- We evaluated the marginal effect of ad impressions and assessed cost-per-conversion for Sites 1–5 vs. Site 6.
- Despite Site 6 showing weaker statistical impact, it was more cost-efficient. We recommended a budget-balanced strategy.

---

### Assignment-3 – Difference-in-Differences (DiD) on Google Ads

**Context:** A technical glitch halted Google’s branded search ads for three weeks.

- We treated this as a natural experiment and applied DiD using Bing/Yahoo/Ask as controls.
- A naïve pre-post comparison showed no effect, but DiD revealed a 67.3% **causal decline** in traffic attributable to ad suspension.
- We validated assumptions through parallel trends testing (both visually and statistically).
- An ROI correction was calculated by adjusting for substitution effects (organic vs. paid traffic), leading to a more conservative ROI estimate than naive methods.

---

### Assignment-4 – Multi-Method Causal Inference

**Question 1: Directed Search & Sales (Propensity Score Matching)**  
We tested whether directed search behavior (e.g., users with intent) leads to higher sales. Using PSM on behavioral and demographic variables, we found:
- Directed search leads to significantly higher promoted sales (+218%) and overall sales (+185%).
- Interestingly, non-promoted sales decreased, suggesting more focused purchasing behavior.

**Question 2: California Cigarette Tax (Synthetic Control)**  
We estimated the effect of the 1989 tax on cigarette consumption. A synthetic control was constructed from other U.S. states to match pre-1989 sales trends. A clear post-1989 drop in California’s actual sales supported the tax’s effectiveness.

**Question 3: Ad Rank and Click-Through Rate (Regression Discontinuity)**  
We applied an RDD using bid differences between first and second-ranked ads. Being ranked first causally increased CTR by ~15.8 percentage points. Assumptions like continuity and local randomization were discussed and visually verified.

---

## Author

**Avnee Satija**  
MSBA Candidate, Carlson School of Management  
Collaborated with: Harshal Sable  
Course: Causal Inference (Spring 2025) – University of Minnesota
