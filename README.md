# Air Quality Data Sampling Analysis

## Project Overview

This project focuses on exploring **sampling techniques** applied to a dataset on air quality, specifically analyzing carbon monoxide—a major air pollutant. Proper sampling techniques are essential when working with large datasets to improve the efficiency and accuracy of analysis. In this project, I perform random sampling with replacement, apply the central limit theorem, and compare sampling distributions to population metrics.

The dataset includes information from over 200 sites, identified by their state, county, city, and local site names. My analysis focuses on understanding how sampling affects the accuracy of the air quality index (AQI) and the insights drawn from the sampled data.

## Table of Contents

- [Introduction](#introduction)
- [Tools Used](#tools-used)
- [Project Structure](#project-structure)
- [Data Exploration and Statistical Tests](#data-exploration-and-statistical-tests)
  - [Step 1: Imports](#step-1-imports)
  - [Step 2: Data Exploration](#step-2-data-exploration)
  - [Step 3: Statistical Tests and Sampling](#step-3-statistical-tests-and-sampling)
  - [Step 4: Results and Evaluation](#step-4-results-and-evaluation)
- [Key Insights](#key-insights)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [References](#references)

## Introduction

Air quality, particularly carbon monoxide levels, is a critical environmental factor affecting public health. In this project, I analyze data from multiple air quality monitoring sites to better understand how sampling techniques can be applied to extract meaningful insights from large datasets. The analysis involves sampling the AQI (Air Quality Index) and applying the central limit theorem to compare sample and population means.

The analysis addresses the following key questions:
- How does sampling with replacement affect the mean AQI compared to the population?
- What insights can I draw from the sampling distribution compared to the actual population distribution?
- How does the central limit theorem apply to this dataset?

## Tools Used

- **Pandas**: For data manipulation and exploration.
- **NumPy**: For numerical operations.
- **Matplotlib**: For data visualization.
- **Statsmodels**: For statistical analysis.
- **SciPy**: For additional statistical functions.

## Project Structure

The project is divided into four main steps:
- **Step 1: Imports**: Importing necessary libraries for data manipulation and analysis.
- **Step 2: Data Exploration**: Examining the dataset structure, generating descriptive statistics, and understanding the AQI column.
- **Step 3: Statistical Tests and Sampling**: Performing sampling with replacement, applying the central limit theorem, and comparing sample means to population means.
- **Step 4: Results and Evaluation**: Visualizing the sampling distribution and analyzing the standard error of the mean.

## Data Exploration and Statistical Tests

### Step 1: Imports
I begin by importing the required libraries:
- Pandas for data manipulation.
- NumPy for numerical operations.
- Matplotlib for data visualization.
- Statsmodels and SciPy for statistical tests.

### Step 2: Data Exploration
I load and explore the dataset to understand its structure and the characteristics of the `aqi` (Air Quality Index) column. Key questions addressed:
- What does the AQI column represent?
- What are the descriptive statistics, including the mean and count of the AQI column?
- Are there missing values in the AQI column?

### Step 3: Statistical Tests and Sampling
I sample 50 observations from the dataset with replacement using the `sample()` function, setting a random seed for reproducibility. The goal is to:
- Compare the sample mean to the population mean.
- Apply the **central limit theorem** by taking 10,000 samples and calculating their mean.
- Compute the standard error of the AQI mean based on the samples.

I visualize the sampling distribution using histograms and analyze the relationship between the sample mean, population mean, and the central limit theorem.

### Step 4: Results and Evaluation
I plot a histogram of the sampling distribution and compare the sample mean to the population mean. Additional vertical lines indicate:
- The mean of the sample.
- The mean of the means from the 10,000 samples.
- The population mean.

## Key Insights

- The mean AQI of the sample closely matches the population mean, validating the central limit theorem.
- The sampling distribution follows a normal distribution as predicted by the central limit theorem.
- The standard error helps quantify the variability of the sample mean from the population mean.
- Air quality, measured through AQI, is generally satisfactory across sampled observations.

## Conclusion

This project demonstrates the importance of **random sampling** and its relationship to the **central limit theorem** when analyzing large datasets. Through this analysis, I validated that a small sample size can be representative of a larger population, provided that sampling is done correctly. Furthermore, this work highlights the need for further investigation into regions with unhealthy carbon monoxide levels to allocate resources effectively.

## How to Run

1. **Clone the repository**:

    ```bash
    git clone <https://github.com/MahmoudKhaled98/Air-Quality-Data-Sampling-Analysis.git>
    ```

2. **Install the required dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Jupyter notebook**:

    ```bash
    jupyter notebook
    ```

## References

- [Pandas Documentation](https://pandas.pydata.org/)
- [NumPy Documentation](https://numpy.org/)
- [Matplotlib Documentation](https://matplotlib.org/)
- [Statsmodels Documentation](https://www.statsmodels.org/)
- [SciPy Documentation](https://scipy.org/)
