> To see interactive Plotly charts, please click this [nbviewer link](https://nbviewer.org/github/shipWong/eBay-Car-Sales/blob/main/GP-004_Exploring_eBay_Car_Sales_Data.ipynb#Loading-and-exploring-the-data).

# Finding Your Dream Car — Analyzing the German eBay Car Sales

## Introduction

[_eBay Kleinanzeigen_](https://www.ebay-kleinanzeigen.de/) is a classified section of the German eBay website. In this project, we will use the vehicles dataset from _eBay Kleinanzeigen_ to analyze the classified vehicle advertisements created in Germany between 11th June 2015 and 7th April 2016.

The original dataset uploaded to Kaggle by user [orgesleka](https://www.kaggle.com/orgesleka) is no longer available on Kaggle, but it is still accessible on [data.world](https://data.world/data-society/used-cars-data). 

In this project, we use the _modified_ version of the original dataset, which was prepared by Dataquest. The modifications are as follows:

- _50,000 data points_ have been sampled from the 370,000 data points of the original dataset.
- The dataset _was uncleaned_ slightly — to make it resemble a scraped dataset before data cleaning. The original dataset on Kaggle had been cleaned.

### Project goals

The project goals are to analyze **the trend of the classified vehicles** on eBay Kleinanzeigen and the **correlations between the prices and other variables**. This project ultimately aimed to help buyers **make informed decisions** for buying vehicles on eBay Kleinanzeigen.

### Scopes

The project scope includes:

- Data cleaning
- Exploratory data analysis with visualisations

### Key results

Our project disclosed that the vehicle prices are lowly positively correlated with the vehicle registration years and lowly negatively correlated with the mileage. We also revealed that vehicles with unrepaired damage are about two-thirds cheaper than vehicles without unrepaired damage.

### Limitations

1. We [remove the entries with the vehicle registration dates from April 2016 onwards](#beyond-web-crawling), as it is illogical to have the data of the vehicles registered after the last day of the web crawling, i.e. 2016-04-07. Since the registration dates are not available, we need to remove the entries for the whole April month of 2016, which also include seven days of legitimate data.

2. There are 4,586 entries containing the [registration month of 0](#registration-month-of-0) — an incorrect value. Out of the 4,586 entries, 342 entries (or 0.723% of the total dataset) are associated with registration year 2016. Since it is impossible for us to find out whether the 342 entries are associated with the registration from April 2016 onwards (after the web crawling stops) and it is only a small proportion of data, we removed these entries to protect the accuracy of our data analysis.

3. A proportion of the [asking prices is extremely low](#outliers-in-the-minumum-prices) — some are even as low as several euros to €0. It is a strategy for the buyers to attract the bidders. However, it is challenging for us to set a reasonable lowest price limit, which still represents the realistic market price. It would be more realistic for us to analyse the sold prices, instead of the asking prices. Unfortunately, the sold prices are not available in the dataset.

4. The [outliers in the maximum prices](#outliers-in-the-maximum-prices) are true outliers, which need to be handled carefully with domain knowledge. However, it is challenging to verify them manually in a big dataset.
