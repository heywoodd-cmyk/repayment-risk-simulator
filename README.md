# Repayment Risk Simulator

## Overview

The Repayment Risk Simulator is an analytical study of consumer loan performance using historical Lending Club data from 2007 through 2018. The purpose of this project is to examine how borrower characteristics relate to repayment outcomes and to translate those relationships into interpretable insights that resemble the work performed by credit risk and portfolio analytics teams.

This project intentionally emphasizes structured analysis and communication rather than predictive modeling. The goal is to demonstrate how raw financial data can be transformed into decision-support intelligence that is accessible to both technical practitioners and business stakeholders.

## Objective

The analysis investigates a central question: which borrower attributes are most strongly associated with elevated repayment risk, and how can those relationships inform credit evaluation and portfolio strategy.

## Data and Preparation

The source dataset consists of Lending Club loan-level records. Because the original file is large, it is not stored in the repository. Instead, the workflow documents how the data were processed to create a clean analytical dataset suitable for business intelligence tools.

Using Python with pandas and numpy, the raw data were standardized, filtered, and engineered into a structure designed for interpretation. Interest rates were converted to numeric form, employment length was normalized into consistent categories, and an average FICO score was derived from the provided score ranges. A binary risk indicator was created to distinguish loans that defaulted or were charged off from those that were fully repaid. Columns that added noise without analytical value were removed so that the resulting dataset reflects variables typically examined in underwriting and monitoring contexts.

The resulting file, stored as data/processed/bi_ready_dataset.csv, is optimized for visualization and exploratory analysis rather than machine learning workflows.

## Analytical Approach

The project evaluates repayment behavior across three core dimensions: assigned credit grade, borrower income, and credit score quality. These dimensions reflect how lending institutions segment risk in practice and provide a transparent view of how borrower profiles translate into observed outcomes.

The analysis was conducted in Tableau using the engineered dataset. Visualizations were designed to highlight distributional differences, directional relationships, and areas of concentration rather than to produce forecasts. The intent is to support reasoning, comparison, and explanation.

## Key Findings

Credit grade exhibits a clear monotonic relationship with default frequency, indicating that internal grading frameworks meaningfully differentiate borrower risk. Income shows a stabilizing effect on repayment outcomes, though its protective value diminishes beyond middle-income levels, suggesting that income alone is not a sufficient underwriting signal. Credit score demonstrates the strongest sensitivity, with repayment performance improving substantially as borrowers move from subprime into near-prime ranges, underscoring the pricing and risk implications of relatively small score changes.

## Repository Structure

The repository contains the processed analytical dataset, the notebook that documents the transformation steps, and exported Tableau figures used to communicate results. The notebook located in notebooks/01_eda.ipynb provides a reproducible record of data preparation. Visualization outputs are stored in reports/figures and correspond directly to the insights discussed in this document.

## Tools and Environment

All preparation and transformation steps were performed in Python within a Jupyter environment. Visualization and exploratory analysis were completed in Tableau Public. Version control and project organization were managed with Git and GitHub.

## Relevance

This project reflects the type of work conducted by analytics teams in financial services, fintech, and risk management functions. It demonstrates the ability to structure large datasets, engineer interpretable variables, and communicate analytical findings in a manner that supports operational and strategic decision-making.

## Author

Devante Heywood

