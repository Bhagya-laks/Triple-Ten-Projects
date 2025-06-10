
# Zuber Ride-Sharing Data Analysis - Chicago Launch

## Project Overview

Zuber is a new ride-sharing company preparing for launch in Chicago. This project focuses on understanding rider behavior, preferences, and how external factors—particularly weather—affect ride frequency and trip duration. Using historical data from taxi companies in Chicago, the goal is to extract actionable insights that can guide business strategy for Zuber’s successful market entry.

### Data Source

The analysis is based on a structured database containing the following tables:
<img src= "ERD.png" />

### Tools
- **PostgreSQL**: Used for querying, data extraction, and analysis.

## Analysis

### Data Cleaning and Preparation

#### Exploratory Data Analysis

1. **Trip Count Analysis**
   - Counted taxi rides per company for **November 15-16, 2017**, labeled as `trips_amount`.
   - Filtered and grouped ride counts for companies whose names include **"Yellow"** or **"Blue"** for **November 1-7, 2017**. Grouped by `company_name`, labeled as `trips_amount`.
   - Categorized and summed trips for all other companies under a new group labeled **"Other"**. Sorted results by `trips_amount` in descending order.

     <img src= "Task3.png "/>
     
2. **Neighborhood Mapping**
   - Retrieved IDs for **Loop** and **O'Hare** neighborhoods using the `neighborhoods` table to support trip filtering and route-based analysis.

#### Weather Impact Hypothesis Testing

**Hypothesis**: *Weather conditions significantly impact ride frequency and duration.*

Steps:
- Used the `weather_records` table to classify each hour's weather:
  - If `description` contains **"rain"** or **"storm"**, labeled as `Bad`.
  - Otherwise, labeled as `Good`.
  - Final fields: `date`, `ts`, `weather_conditions`.

- Retrieved all rides:
  - **Start**: Loop (pickup_location_id = 50)
  - **End**: O’Hare (dropoff_location_id = 63)
  - **Day**: Saturdays
- Merged weather data using the timestamp to assign weather conditions to each ride.
- Selected fields: `start_ts`, `weather_conditions`, `duration_seconds`.
- Ignored rides with missing weather data.
- Sorted final output by `trip_id`.



- **Company Comparison**: Investigated number of taxi rides and grouped results by company name to understand operator market share and ride volume.
- **Weather Categorization**: Integrated weather data to classify each time window as having either `Good` or `Bad` weather (i.e., rain or storm) and aligned this with trip data.
- **Weather-Impact Hypothesis**: Tested the hypothesis that weather conditions significantly affect the number of rides and ride durations. Observed a notable correlation between adverse weather and higher ride demand.
- **Strategic Insight**: Insights from this analysis provide direction for Zuber's operational strategy, dynamic pricing models, and targeted marketing plans that align with customer behavior and seasonal trends.

## Recommendations

### Weather-Aware Pricing & Promotions
Implement surge pricing or targeted promotions during rainy, snowy, or extremely cold days. Ride demand increases under adverse weather conditions, presenting strong revenue opportunities.

### Focus on High-Demand Time Windows
Concentrate driver availability and marketing efforts during weekday commute hours (**7–9 AM** and **5–7 PM**) and weekend evenings, when ride frequency typically peaks.

### Seasonal Marketing Campaigns
Allocate more advertising budget during months with high ride frequency and favorable profit margins—especially in **fall and early winter**, when demand is driven up by weather conditions.

---

*Prepared by the Data Analysis Team at Zuber.*
