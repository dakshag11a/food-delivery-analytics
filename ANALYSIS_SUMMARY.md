# 📊 Analysis Summary Report

**Project 8: Food Delivery Operations Analytics**
**Student:** Daksh Agarwal | **Roll No:** 2026b03110270
**College:** ABES Engineering College, Ghaziabad (B.Tech ECE, 1st Year)

---

## Key Findings from the Dataset (2,000 Orders)

### 1. Order Status Distribution
| Status | Count | Percentage |
| :--- | :--- | :--- |
| Delivered | 1,642 | 82.10% |
| Cancelled | 185 | 9.25% |
| Delayed | 173 | 8.65% |

### 2. Delivery Time Statistics
| Metric | Value |
| :--- | :--- |
| Mean | 36.06 minutes |
| Median | 36.00 minutes |
| Standard Deviation | 11.33 minutes |
| IQR Outlier Threshold | > 64 minutes (15 orders) |

### 3. City-Level Performance
| City | Avg. Delivery Time | Cancellation Rate | Delay Rate |
| :--- | :--- | :--- | :--- |
| Delhi | 35.65 min | **11.11%** | **9.22%** |
| Faridabad | 36.07 min | 7.57% | 7.57% |
| Gurugram | 36.54 min | 9.52% | 8.33% |
| Noida | 36.00 min | 9.19% | 8.55% |

> Delhi is the primary operational bottleneck (highest cancellation and delay rates).

### 4. Top Restaurants by Revenue
| Rank | Restaurant | Total Order Value |
| :--- | :--- | :--- |
| 1 | Pizza Point | ₹2,02,159.89 |
| 2 | Green Bowl | ₹1,89,623.29 |
| 3 | Urban Bites | ₹1,81,800.76 |

> Green Bowl has the highest delay rate (10.80%) despite being second in revenue.

### 5. Peak Ordering Hours
Peak demand occurs at **10:00**, **13:00**, and **21:00** — together accounting for **23.1%** of all orders.

### 6. Delivery Time Bands (SLA Classification)
| Band | Rule | Orders | Share |
| :--- | :--- | :--- | :--- |
| Fast | ≤ 30 min | 624 | 31.2% |
| Standard | 31–45 min | 984 | 49.2% |
| Delayed | > 45 min | 392 | 19.6% |

---

## 5 Operational Recommendations
1. Focus on reducing long-tail deliveries (19.6% exceed 45 min) rather than city-wide averages.
2. Add extra rider capacity at 10:00, 13:00, and 21:00 (peak hours carry 23.1% of demand).
3. Set city-wise weekly targets for Delhi (11.11% cancellations, 9.22% delays).
4. Coordinate with Green Bowl to shorten preparation and handover time (10.8% delay rate).
5. Flag deliveries exceeding 64 minutes for automatic dispatch review (15 outlier orders).
