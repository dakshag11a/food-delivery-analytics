# Project 8: Food Delivery Operations Analytics

**Student:** Daksh Agarwal | **Student ID:** 2026b03110270 | **College:** ABES Engineering College, Ghaziabad (B.Tech ECE)
**Course:** Python, NumPy & Pandas, Five-Day Engineering Student Training (First Year, First Semester)
**Industry:** FoodTech / Logistics

## Problem
A food delivery company wants to evaluate delivery times, order outcomes, restaurant performance and city-level operations to find service improvements. This project analyses 2,000 orders (4 cities, 5 restaurants) with Core Python, NumPy and Pandas.

## Repository structure
```
/SRS/project_SRS.pdf      Software Requirements Specification (also .docx)
/src/analysis.ipynb       Notebook with all 15 tasks (Tasks 109-123), already executed
/data/08_food_delivery.csv  Dataset (2,000 rows, 10 columns)
/outputs/                 Saved result tables and recommendations
/README.md
```

## Run in Google Colab
1. Open Google Colab and choose **File > Upload notebook** (or open from GitHub), then select `src/analysis.ipynb`.
   - From GitHub: `https://colab.research.google.com/github/dakshag11a/food-delivery-analytics/blob/main/src/analysis.ipynb`
2. Run all cells (**Runtime > Run all**).
3. When asked, upload `data/08_food_delivery.csv`.

## Run locally
```
pip install pandas numpy jupyter
cd src
jupyter notebook analysis.ipynb
```
The notebook finds the dataset in `../data/` automatically.

## Tasks covered
| Task | What is done |
|---|---|
| 109 | Load and inspect the dataset |
| 110 | Missing delivery times: found 28 (1.4%), filled with the city median, flagged |
| 111 | Duplicate Order_ID check (none found) |
| 112 | Total orders and status percentages |
| 113 | Average delivery time by city |
| 114 | Top 5 restaurants by total order value |
| 115 | Average order value by restaurant |
| 116 | Peak ordering hours |
| 117 | Delivery time by order status |
| 118 | Cancellation and delay rates by city |
| 119 | NumPy median and standard deviation |
| 120 | Long deliveries using IQR |
| 121 | Fast / Standard / Delayed bands (`np.select`, checked with `pd.cut`) |
| 122 | Revenue by city and payment mode (`pivot_table`) |
| 123 | Five operational recommendations |

## Key findings (this dataset)
- 2,000 orders: 82.10% Delivered, 9.25% Cancelled, 8.65% Delayed.
- Delivery time: mean 36.06 min, median 36.0 min, standard deviation 11.33 min. City averages differ by under 1 minute.
- Pizza Point has the highest total order value; Green Bowl has the highest delay rate (10.8%).
- Peak hours are 10:00, 13:00 and 21:00 (23.1% of orders together).
- Delhi has the highest cancellation (11.11%) and delay (9.22%) rates.
- IQR upper limit is 64 min; 15 deliveries exceed it. Bands: 31.2% Fast, 49.2% Standard, 19.6% Delayed.
- Revenue (excluding cancelled orders) is about 818,713; Card is the largest payment mode.

## Assumptions and limitations
- The dataset is synthetic; findings apply to this data only.
- Revenue excludes cancelled orders. Band cut-offs (30 and 45 min) are assumptions.
- No date column, so weekday or seasonal trends are not studied.
- Correlation does not prove causation.

## Output files (`/outputs`)
`city_performance.csv`, `restaurant_ranking.csv`, `peak_hour_summary.csv`, `delay_bands.csv`, `delay_by_status.csv`, `revenue_city_payment.csv`, `recommendations.txt`
