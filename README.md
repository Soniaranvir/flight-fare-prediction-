# Flight Fare Prediction using Linear Regression

## Overview
This project focuses on building a machine learning model to predict flight ticket prices for Indian airlines. The goal is to help EasyMyTrip, an online travel platform, optimize its pricing strategies and maximize profits through data-driven decision-making.

## Problem Statement
EasyMyTrip wants to leverage machine learning to gain insights into pricing trends and forecast flight fares. The model aims to address key questions related to airline price variations, last-minute booking surcharges, time-based price fluctuations, route-based differences, and class-wise fare differences.

### Key Considerations:
- **Price Variations Across Airlines:** Do ticket prices significantly differ among various airlines?
- **Impact of Last-Minute Bookings:** How does purchasing tickets 1-2 days before departure affect pricing?
- **Correlation between Price and Departure/Arrival Times:** Are certain flight times more expensive than others?
- **Price Variation Based on Source and Destination:** How do fares fluctuate based on travel routes?
- **Economy vs. Business Class Pricing:** What is the price gap between these two classes?

By answering these research questions, EasyMyTrip can refine its pricing model to stay competitive and attract more customers.

## Research Findings
### 1. Price Variation Across Airlines
   - Significant differences exist between airlines.
   - Air India and Vistara have the highest average fares, while AirAsia and Indigo offer more budget-friendly options.

### 2. Last-Minute Booking Impact
   - Ticket prices increase substantially when booked 1-2 days before departure, indicating a premium for last-minute travelers.

### 3. Effect of Departure/Arrival Times on Pricing
   - Evening and night departures tend to be more expensive.
   - Late-night departures and early-morning arrivals generally cost less.

### 4. Pricing Differences Based on Routes
   - Fares vary across city pairs, with Delhi-Hyderabad being the cheapest route (~17,243.94) and Chennai-Bangalore the most expensive (~25,081.85).

### 5. Economy vs. Business Class Pricing
   - Business class tickets cost significantly more than Economy class, reflecting differences in amenities and customer demand.

## Model Development
We experimented with multiple regression models, including:
- Random Forest
- Gradient Boosting
- XGBoost

After evaluation, **Random Forest** was selected due to its strong performance on both training and test datasets. Hyperparameter tuning was attempted, but the default settings provided optimal results.

### Model Performance
| Dataset | MSE | RMSE | MAE | R-Squared |
|---------|--------|---------|---------|-----------|
| Train | 1,306,991 | 1,143.25 | 438.78 | 0.99747 |
| Test | 5,568,1120 | 7,461.98 | 4,861.69 | 0.89209 |

### Cross-Validation Results
| Metric | Mean |
|--------|---------|
| MSE | 8,013,316 |
| RMSE | 2,830.57 |
| MAE | 1,166.64 |
| R-Squared | 0.9845 |

## Key Predictors
The most influential factors in predicting ticket prices were:

| Feature | Importance |
|---------|-------------|
| Class (Economy/Business) | 0.881975 |
| Flight Duration | 0.052071 |
| Days Left Until Departure | 0.020889 |

Economy class has the strongest impact, explaining 88% of fare variation. Flight duration and advance booking days also significantly influence ticket prices.

## Conclusion
Our machine learning model successfully predicts flight ticket prices, helping EasyMyTrip optimize its pricing strategies. This project provides insights into airline fare dynamics and enables data-driven decision-making to enhance profitability.

