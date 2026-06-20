# Market Basket Analysis using Apriori

## Project Overview

This project performs **Market Basket Analysis** on retail transaction data to identify products that are frequently purchased together. The analysis uses the **Apriori algorithm** to generate frequent itemsets and association rules.

The objective is to discover useful product combinations that can support cross-selling, combo offers, product placement, and recommendation strategies.

## Objective

The main objective of this project is to:

* Analyze customer transaction data
* Identify frequently bought products
* Generate association rules between items
* Understand product purchase relationships
* Support business decisions for retail sales and promotions

## Dataset

The dataset used in this project is:

```text
store_data.csv
```

The dataset contains retail transaction records, where each row represents one customer basket and each column contains an item purchased in that transaction.

## Tools and Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Mlxtend
* Jupyter Notebook

## Methodology

The project follows these steps:

1. Loaded the retail transaction dataset.
2. Cleaned transaction data by removing missing values and extra spaces.
3. Removed duplicate items within the same transaction because Apriori uses item presence rather than quantity.
4. Converted transactions into a one-hot encoded basket format.
5. Applied the Apriori algorithm to identify frequent itemsets.
6. Generated association rules using lift as the main metric.
7. Analyzed support, confidence, and lift values.
8. Exported frequent itemsets and association rules as CSV files.
9. Added observations and conclusion based on product association patterns.

## Algorithm Used

* Apriori Algorithm
* Association Rule Mining

## Key Metrics

| Metric     | Meaning                                                                |
| ---------- | ---------------------------------------------------------------------- |
| Support    | How frequently an itemset appears in all transactions                  |
| Confidence | How often the consequent is purchased when the antecedent is purchased |
| Lift       | Strength of association between items compared to random chance        |

## Key Results

| Metric                      | Result |
| --------------------------- | -----: |
| Total transactions          |  7,501 |
| Unique items                |    119 |
| Frequent itemsets generated |    257 |
| Association rules generated |    406 |
| Minimum support             |   0.01 |
| Rule metric                 |   Lift |

## Key Observations

* Market Basket Analysis helped identify products that are commonly purchased together.
* Lift was used to identify stronger product relationships beyond simple frequency.
* High-confidence rules can support product recommendation strategies.
* High-lift rules can help identify meaningful cross-selling opportunities.
* The results can be used for store layout planning, bundled offers, and promotional campaigns.

## Business Use Case

This project can help retail businesses improve:

* Product recommendations
* Combo offers
* Cross-selling strategies
* Shelf placement
* Promotional planning
* Customer basket analysis

For example, if two products are frequently purchased together, the store can place them near each other or create a bundled discount offer.

## Output Files

The project generates the following output files:

```text
mba_frequent_itemsets.csv
mba_association_rules.csv
```

## Conclusion

This project demonstrates how association rule mining can be used to analyze retail transaction data and discover product purchase patterns. The Apriori algorithm successfully identified frequent itemsets and association rules that can support retail business decisions.

The analysis is useful for understanding customer buying behavior and improving sales strategies through better product placement, recommendations, and promotional offers.
