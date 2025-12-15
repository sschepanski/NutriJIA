# NutriJIA – Feasibility, Safety, and Exploratory Clinical Analysis of a Nutritional Intervention

## Introduction

Nutritional interventions in pediatric and adolescent populations are increasingly explored as low-threshold strategies to support health, development, and disease management. However, before clinical effectiveness can be meaningfully interpreted, careful evaluation of **feasibility, adherence, and safety** is essential—particularly in vulnerable or developing populations.

The NutriJIA project investigates a structured nutritional intervention compared to a control condition, with repeated measurements at baseline and post-intervention. The study places primary emphasis on **feasibility and safety**, while exploratory analyses examine potential clinical signals.

This repository contains the full analytical workflow for the NutriJIA data, focusing on transparent, reproducible, and methodologically sound evaluation of feasibility, safety parameters, and exploratory clinical outcomes.

## Objectives

### Primary Objectives (Feasibility & Safety)

The primary aim of this analysis is to assess whether the nutritional intervention is **feasible and safe**. Specifically, we evaluate:

- **Adherence** to the intervention protocol
- **Safety markers**, including:
  - Body weight and BMI
  - Vitamin B12
  - Transferrin saturation
  - Zinc
  - Beta-carotene
- Changes in safety-relevant parameters from **baseline to post-intervention**
- Between-group differences (intervention vs. control) with baseline adjustment

These outcomes are treated as **primary**, reflecting the pilot and feasibility-oriented nature of the study.

### Secondary Objectives (Exploratory Clinical Analyses)

Secondary analyses are exploratory and hypothesis-generating, aiming to:

- Examine preliminary clinical effects beyond safety
- Explore group differences in selected outcomes after baseline adjustment
- Identify trends that may inform sample size planning and endpoint selection for future confirmatory trials

All secondary analyses are explicitly labeled as exploratory and interpreted accordingly.

## Methodological Overview

The NutriJIA analysis follows a longitudinal observational/interventional framework with repeated measures. Key methodological components include:

- Data cleaning, preprocessing, and harmonization of visit-level data
- Explicit handling of baseline (visit 0) and post-intervention (follow-up) measurements
- Definition of adherence and safety endpoints based on clinical thresholds and distributional properties
- Between-group comparisons using baseline-adjusted models (e.g., ANCOVA-style regression)
- Transparent reporting of missing data patterns
- Sensitivity and robustness checks where appropriate

The analytical emphasis is on **clarity, interpretability, and reproducibility**, rather than overfitting or confirmatory inference.

All analyses are performed in Python, following reproducible research principles.

## Project Structure

- **`data/`**: Contains the dataset used in the analysis.
- **`scr/`**: R scripts for data exploration, preprocessing, modeling, and assumption testing.
- **`graphs/`**: Figures and visualizations produced during the analytical workflow.

## Scripts

- **Analysis.ipynb**: This script conducts the core statistical analyses.

## Acknowledgements

Statistical analysis and methodological development were conducted by **Dr. Steven Ngandeu Schepanski.**

## Getting Started

1. **Clone this repository:**

   ```bash
   git clone https://github.com/sschepanski/NutriJIA.git
   ```
2. **Set up your enviornment using the provided requirement file:**
   ```bash
   pyenv local 3.11.3
   python -m venv .venv
   source .venv/bin/activate
   pip install --upgrade pip
   pip install -r requirements.txt
   ```
3. **Run the provided notebooks in the `scr/` directory for data preprocessing, model training, and evaluation.**

## Contributions

This project analysis was conducted by **Dr. Steven Ngandeu Schepanski**. It is part of the manuscript by Ngoumou et al.

## License

This project is licensed under the MIT License.