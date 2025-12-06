# BigBasket Market Basket Analysis using Apriori Algorithm

## Project Overview
This project aims to perform Market Basket Analysis on a transactional dataset from BigBasket using the Apriori algorithm. The goal is to discover interesting association rules between different items purchased together, which can help in understanding customer purchasing behavior, improving product placement, and recommending products.

## Dataset
The dataset used is `bigbasket.csv`, which contains transactional data. Each row represents a transaction, and columns contain the items purchased in that transaction.

## Methodology
1.  **Installation**: The `apyori` library, which provides an implementation of the Apriori algorithm, was installed.
2.  **Data Loading**: The `bigbasket.csv` file was loaded into a pandas DataFrame.
3.  **Data Preprocessing**: The DataFrame was transformed into a list of lists, where each inner list represents a transaction and contains the items purchased. 'nan' values were handled by converting them to strings to be processed by the algorithm.
4.  **Apriori Algorithm**: The Apriori algorithm was applied to the preprocessed transactions with the following parameters:
    *   `min_support = 0.003`
    *   `min_confidence = 0.2`
    *   `min_lift = 3`
    *   `min_len = 2`
5.  **Results Visualization**: The generated association rules were converted into a pandas DataFrame for better readability and analysis. The rules were then sorted by 'lift' to highlight the strongest associations.

## Key Findings (Top 20 Rules by Lift)
The analysis revealed several strong association rules. The `lift` metric indicates how much more likely item Y is purchased when item X is purchased, relative to its baseline probability. A lift value greater than 1 suggests a positive correlation.

The top rules, sorted by lift, show strong co-occurrence between items such as:

-   `mineral water` and `whole wheat pasta`
-   `neckrest` and `trolly bag`
-   `kissan puree` and `paneer`
-   `pasta` and `mushroom`
-   `buns` and `french fries`
-   `chicken` and `ginger garlic paste`
-   `buns` and `chocolate`
-   `mineral water`, `maggi`, and `chocolate`

These findings can be leveraged for various business strategies, such as targeted promotions, optimizing store layouts, and creating bundled offers.
