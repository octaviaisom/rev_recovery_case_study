# Revenue Recovery Analysis for a Consumer Electronics Retailer

## Diagnosing revenue underperformance across customer activity, product mix, and category-level recovery opportunities
This project is a business analytics case study focused on diagnosing revenue underperformance for a consumer electronics retailer. The analysis investigates what changed in the retailer’s revenue engine, identifies the strongest drivers of decline, and translates those findings into strategic recovery recommendations.

My goal for this project was to show not only technical abilities, but strategic judgment: knowing what to analyze, what not to overstate, and how to turn complex data into decisions leaders can act on.

---

## Project Links

* **Executive Presentation:** [View the final presentation in Canva](https://canva.link/o7swu74xurhe1vx)
* **Source Data:** [Maven Analytics' Gllobal Electronica Retailer dataset](https://mavenanalytics.io/data-playground/global-electronics-retailer) (adjusted as described below)
* **Technical Notebook:** `main.ipynb`

---

## Executive Summary

A consumer electronics retailer experienced an abnormal revenue decline and needed to understand what was preventing recovery. The analysis focused on whether the issue was tied to profitability, customer activity, purchase behavior, or product mix.

The main finding was that the revenue decline was **more activity-driven than margin-driven**. Revenue and gross profit both declined by roughly 21% versus the historical baseline, while gross margin remained essentially flat. This suggested the business was not primarily facing a profitability issue. Instead, fewer active customers and fewer orders were the stronger signals.

The clearest recovery opportunity was **Home Appliances**. This category showed severe declines across revenue, customers, orders, quantity sold, subcategory performance, and Q4 momentum. Historical Home Appliances customers were also largely inactive in 2025, suggesting a potential reactivation and cross-sell opportunity.

###

---


## Dataset Source and Analytical Reframing

#### Date Shift

The source data for this project came from [Maven Analytics](https://mavenanalytics.io/data-playground/global-electronics-retailer). The dataset includes transaction-level sales data across orders, customers, products, stores, and product categories.

For this case study, I made a deliberate decision to shift the dates forward by five years to modernize the business framing (2016-2021 → 2021-2026). The underlying transaction patterns were preserved. Only the ```order_date``` was adjusted.

This choice was made because the original timeframe could easily lead to a COVID-centered interpretation. While that is a valid analytical path, I did not want the project to default to a broad “COVID caused the decline” explanation. That framing felt less useful for demonstrating deeper business analysis because it risks treating the external event as the answer before fully investigating what actually changed inside the business.

#### Store-Level Insights

The dataset includes both online and in-store purchases, along with store-level information. However, store performance was not a primary focus of this analysis.

That was an intentional scope decision as well. The dataset did not include enough supporting operational context to responsibly diagnose store-level performance, such as foot traffic, staffing, local market conditions, or inventory availability.

Rather than overextend the analysis into areas the data could not fully support, I focused the case study on the areas where the data was strongest.

---

## Tools and Technologies


| Tool / Technology    | How it was used                                                                      |
| -------------------- | ------------------------------------------------------------------------------------ |
| **Python**           | Data preparation, analysis, metric creation, and visualization                       |
| **Pandas**           | Data cleaning, joins, aggregations, baseline comparisons, and analytical tables      |
| **NumPy**            | Metric calculations, conditional logic, and numerical handling                       |
| **Matplotlib**       | Custom visuals for trends, scorecards, category comparisons, and executive reporting |
| **Jupyter Notebook** | Technical workflow, analysis documentation, and reproducible logic                   |
| **Visual Studio Code** | Code development, notebook editing, project organization |
| **Canva**            | Final presentation design and hosting                                      |
| **GitHub**           | Repository hosting, project documentation, and portfolio sharing                     |
|                      |                                                                                      |


### AI Usage Disclosure

For this project, AI  supported coding efficiency and with standardizing comments/documentation. I used AI only to accelerate execution while maintaining full responsibility for the logic, conclusions, and final deliverables.

---

## Repository Structure

```text
rev-recovery-case-study/
│
├── README.md
│
├── main.ipynb.md
│
├── data/
│   ├── customers.csv
│   ├── orders.csv
│   ├── products.csv
│   └── stores.csv
│   └── exchange_rates.csv
│   └── data_dictionary.csv
│
├── exports/
│   └── charts/
│       ├── p1/
│       ├── p2/
│       ├── p3/
│       └── pressure_tests/
│
```
