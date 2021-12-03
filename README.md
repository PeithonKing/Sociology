# Perception of Scientists: A Sociological Analysis

## About
This repository contains the data analysis conducted for the H133 Introduction to Sociology course, taught by Professor Pranay Kumar Swain. The project explores public perceptions of scientists, examining the intersection of ethics, educational requirements, and the perceived role of science in society. By transforming qualitative survey responses from 312 participants into a quantitative dataset, the analysis attempts to uncover hidden correlations between how people define an "ideal scientist" and their views on scientific ethics and professional priorities.

## Technical Details
The project is implemented in Python, utilizing a data science stack consisting of Pandas for manipulation and Matplotlib/Seaborn for visualization. 

The technical workflow is divided into three main phases:
1. **Data Refinement**: Raw survey data is cleaned and normalized. A mapping system is established where each unique text response is assigned an integer ID, stored in `summary.json`. This allows the qualitative data to be treated as discrete variables for mathematical analysis.
2. **Statistical Analysis**: The analysis employs correlation matrices and pair-plots to identify linear relationships between different survey dimensions. 
3. **Relational Mapping**: Beyond simple correlation, the project uses a custom relation function to calculate the frequency of response pairs. This allows for the analysis of conditional distributions across the 13 survey questions, effectively mapping the "sociological profile" of the respondents.

![Analysis Output](output.png)

## Execution
To reproduce the analysis, ensure you have Python 3 installed along with the following dependencies:

```bash
pip install pandas matplotlib seaborn
```

The analysis is spread across several Jupyter Notebooks:
- `refine.ipynb`: Run this first to process `data.csv` and generate `refined.csv` and `summary.json`.
- `analysis.ipynb`: The main analysis pipeline where correlations and relation matrices are computed.
- `verify.ipynb`: Used for sanity checks and specific query validations on the refined dataset.

The `summary.json` file should be used as a lookup table to translate the integer results in the CSV files back into their original textual meaning.