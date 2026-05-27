# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

UC Berkeley Data 100 (Spring 2026) — Principles and Techniques of Data Science. Course URL: https://ds100.org/sp26/

**User's Goal:** Build foundations for ML/algorithm engineer (算法岗) internship and research. Prioritize mathematical depth and ML theory, not just data wrangling.

**GitHub:** https://github.com/moyu222/data100.git

## Course Structure

```
lec/     — 23 lecture notebooks (lec02–lec26, missing 01/16/18)
hw/      — 7 homework assignments (hw01–hw07)
lab/     — 11 lab assignments (lab01–lab11)
proj/    — 4 projects (A1, A2, B1, B2)
disc/    — 2 discussion worksheets (disc02, disc11)
grad-proj/ — Graduate project (CV: disaster image classification)
```

## Learning Priority Tiers

### Tier 1 — Must Master
**lec10-12** Linear Regression, OLS, Normal Equation | **lec13-14** sklearn, Gradient Descent, SGD | **lec15** Feature Engineering, One-hot, Polynomial, CV | **lec17** L1/L2 Regularization (LASSO/Ridge) | **lec23-24** Logistic Regression, Cross-entropy, ROC/AUC | **projA1+A2** Full regression pipeline (Cook County housing)

### Tier 2 — Important
**lec04** Groupby, pivot, merge | **lec05** EDA | **lec19-20** Bootstrap, Confidence Intervals, Hypothesis Testing | **lec25** K-Means, Hierarchical Clustering | **lec26** PCA, SVD | **projB1+B2** Spam classification pipeline

### Tier 3 — Quick Pass
**lec02-03** Basic Pandas (reference docs as needed) | **lec06** Regex (know str.extract + re.findall) | **lec07-08** Visualization (use when needed) | **lec09** Sampling | **lec21-22** SQL (lower priority for ML roles) | **lec16, lec18** Missing materials

### Tier 4 — Bonus
**grad-proj** CV disaster image classification — can extend with PyTorch CNN for a stronger resume project

## Development Commands

All work is done in Jupyter notebooks (`.ipynb`). No build/lint/test commands.

```bash
# Start Jupyter
jupyter lab

# Run a notebook headlessly (verify it works)
jupyter nbconvert --to notebook --execute --inplace <notebook.ipynb>

# Add and push changes to GitHub
git add <files> && git commit -m "..." && git push
```

## Key Data Files by Module

- **lec04/hw03** — elections data (`elections.csv`)
- **lec05** — tuberculosis/ILI/vaccination data
- **lec10-12** — dugongs, boba tea, NBA data
- **lec13** — penguins dataset
- **lec15/hw04** — tips dataset
- **lec25** — iris dataset
- **lec26** — Fashion-MNIST, congressional votes
- **projA1/A2** — Cook County housing (>500K records, `cook_county_data/`)
- **projB1/B2** — SpamAssassin email corpus (8,348 emails)
- **grad-proj** — Disaster RGB images (hurricane, wildfire, flooding)

## Utility Modules

- `ds100_utils.py` — Shared utilities across multiple labs/hw (data loading, display helpers)
- `hw06_utils.py` — Homework 6 specific utilities
- `lab6_utils.py` — Lab 6 specific utilities
- `projA2/ds100_utils.py`, `projA2/feature_func.py` — Project A2 utilities
- `projB2/projB2_utils.py` — Project B2 utilities
- `grad-proj/data_utils.py`, `grad-proj/feature_utils.py` — Graduate CV project utilities

## Teaching Approach

When user asks to study a topic:
1. Walk through mathematical derivation first (formulas, intuition)
2. Then implement in code
3. Highlight connections to other ML topics and interview questions
4. Prefer efficiency — no verbose explanations when a concise one suffices
5. Use the `daily-report` skill when user types `/daily-report` for structured learning reviews
