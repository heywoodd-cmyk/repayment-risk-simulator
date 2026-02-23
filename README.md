# Repayment Risk Simulator

## Overview

This project analyzes historical Lending Club loan performance to understand how borrower attributes translate into realized repayment behavior. The objective is not to build a predictive model, but to replicate an analytics workflow commonly used in credit, product, and risk teams: transforming operational data into interpretable signals that inform underwriting policy, segmentation strategy, and portfolio monitoring.

## Analytical Focus

Rather than asking whether risk exists, the analysis examines where risk meaningfully differentiates borrowers and where commonly used indicators lose explanatory power. The goal is to identify which variables help decision-makers separate borrowers into behaviorally distinct groups and which add redundancy.

## Data Preparation

Loan-level data from 2007–2018 were standardized and reduced into a structured analytical dataset using Python. Transformations included numeric conversion of interest rates, normalization of employment tenure, construction of an average FICO measure from score ranges, and creation of a binary repayment outcome distinguishing charged-off loans from successfully repaid loans. The resulting dataset was shaped specifically for exploratory and business intelligence analysis.

## Findings

Credit grade provides directional separation of repayment outcomes, but much of its explanatory value overlaps with underlying credit score bands. When examined alongside FICO-derived segmentation, grade appears to function more as a packaging layer than an independent signal. This suggests that downstream analytics or pricing models may benefit more from continuous credit measures than from categorical grade labels alone.

Income demonstrates a stabilizing relationship with repayment only up to a threshold. Beyond moderate income levels, default behavior does not materially improve. This indicates diminishing marginal predictive value and supports the view that repayment stress is often driven by balance sheet structure rather than raw earnings.

Purpose-based segmentation reveals greater dispersion than expected. Loans associated with discretionary consolidation or refinancing show wider outcome variance than necessity-driven borrowing categories, implying behavioral heterogeneity that is not captured by traditional credit metrics.

Credit score transitions, particularly in near-prime ranges, show sharper changes in repayment behavior than movements within already strong score bands. This has practical implications for approval cutoffs, where small shifts in eligibility criteria may alter portfolio risk more than adjustments among higher-credit borrowers.

## Interpretation

Taken together, these patterns reinforce that commonly used lending indicators are not equally informative across their full range. Some variables operate as coarse screening tools, while others carry signal only in specific intervals. Effective analytics therefore requires understanding where segmentation adds value rather than assuming monotonic relationships across all borrowers.

## Repository Contents

The repository documents the transformation pipeline in notebooks/01_eda.ipynb and provides the processed dataset used for analysis. Visualization outputs generated in Tableau are stored in reports/figures and reflect the analytical comparisons described above.

## Tools

Python (pandas, numpy) was used for data preparation within Jupyter. Tableau Public was used for exploratory visualization. Git and GitHub were used to manage reproducibility and project structure.

## Relevance

This work mirrors the exploratory phase of real-world credit analytics, where teams evaluate how borrower characteristics translate into observed behavior before formal modeling or policy changes are introduced. It demonstrates the ability to structure large datasets, interrogate segmentation logic, and communicate implications in a way that supports both technical and operational audiences.

## Author

Devante Heywood
