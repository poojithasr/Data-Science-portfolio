# A/B Testing Analysis on E-Commerce Conversion Rates

This repository contains a complete analysis of an A/B test conducted on an e-commerce website to evaluate the performance of a new webpage compared to the existing one. The project uses statistical methods to determine whether the new page improves conversion rates and provides actionable recommendations based on the results.

---

## Dataset

The dataset used for this experiment is sourced from Kaggle. 
It contains the following key columns:  
- `user_id` : Unique identifier for each user  
- `group` : Experiment group assignment (`control` or `treatment`)  
- `converted` : Binary conversion indicator (1 = converted, 0 = not converted)  
- `timestamp` : Datetime of user interaction
- `landing_page` : Whether the page is old or new

A large e-commerce company has a new webpage designed with the intention to increase their current conversion rates of 12% by 0.5% or more. Using the dataset, we will run the A/B testing experiment and provide recommendation whether to implement the new page or keep the old page.

## Project Objectives

1. **Compare conversion rates** between the control and treatment groups.  
2. **Assess statistical significance** using a two-proportion z-test and confidence intervals.  
3. **Evaluate sample size and power** to detect business-relevant differences (Minimum Detectable Effect, MDE).  
4. **Provide actionable recommendations** for the business regarding the new webpage.

## Tools and Libraries

- Python 3.x  
- Pandas  
- NumPy  
- SciPy (`stats` module)  
- Statsmodels (`stats.proportion` and `stats.power`)  
- Matplotlib / Seaborn (optional for visualization)  

## Usage

1. Clone the repository:

```bash
git clone https://github.com/poojithasr/Data-Science-portfolio.git
cd Data-Science-portfolio
cd "AB_testing"

