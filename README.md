# 591 Rental Analysis Project

This is a project that utilizes web scraping techniques to collect rental data of Taichung city from [591 rental website](https://rent.591.com.tw/?region=8), and performs regression analysis on the rental data collected from Taichung city. The regression methods used in this project are decision tree and random forest.

## Table of Contents

- [Background](#background)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Background

The 591 rental website is one of the most popular rental platforms in Taiwan. This project aims to help renters better understand and predict rental prices. The project used crawler technology to collect 4841 rental data from the platform and perform regression analysis on the rental data collected from Taichung city. The regression methods used in this project are decision tree and random forest, which are widely used machine learning algorithms for regression analysis. 

This project uses features such as the number of square meters of the house, location, the floor, whether pets are allowed, whether parking is included, etc. to predict the rental price([see detail](https://github.com/EvanRuan0401/rent-of-house-regression/blob/main/Taichung/Analysis_Report/Regression.ipynb)). Since the methods used in the project are all tree models, in order to avoid the tree growing too large and making the model difficult to explain, the goal of this project is to find a model that is highly explanatory and can be read by anyone to help all demanders of rental have a clear understanding of the rental market in Taichung City. Give models the features of a house, then model will output the result of the rental and everyone can simply know how much rent is likely to cost each month.

## Installation

To run this project, you will need to have Python 3.x installed. You can clone this repository to your local machine using the following command:

```bash
git clone https://github.com/EvanRuan0401/rent-of-house-regression.git
```

Then, install the required packages by running the following command in the project directory:

```bash
pip3 install -r requirements.txt
```

## Usage

To collect rental data from 591 website, you can run the [tc_get_591_data.ipynb](https://github.com/EvanRuan0401/rent-of-house-regression/blob/main/Taichung/Taichung_591crawler/tc_get_591_data.ipynb) script. This script will scrape the cleaned rental data from the 591 website and store it in [tc_cleaned_Rent_591.csv](https://github.com/EvanRuan0401/rent-of-house-regression/blob/main/Taichung/Taichung_591crawler/tc_cleaned_Rent_591.csv) file.

To do exploratory data analysis(EDA) on the rental data, you can run the [tc_EDA.ipynb](https://github.com/EvanRuan0401/rent-of-house-regression/blob/main/Taichung/Analysis_Report/tc_EDA.ipynb) script. This script will generate some simple rental analysis reports and visualize them. In addition, some data cleaning work has been done in this file to ensure the next step(regression analysis) can work. The cleaned data store in [updated_tc_Regression.csv](https://github.com/EvanRuan0401/rent-of-house-regression/blob/main/Taichung/Analysis_Report/updated_tc_Regression.csv) file.

To perform regression analysis on the rental data, you can run the [Regression.ipynb](https://github.com/EvanRuan0401/rent-of-house-regression/blob/main/Taichung/Analysis_Report/Regression.ipynb) script. Regression analysis using decision tree and random forest methods, and output the analysis results.

## License

This project is licensed under the MIT License - see the [LICENSE file](https://github.com/EvanRuan0401/rent-of-house-regression/blob/main/LICENSE) for details.