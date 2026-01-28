
# 🚖 Cab Booking System EDA Project

🔹 Overview

The Cab Booking System has grown rapidly as ride-hailing services have become an essential part of urban transportation. This project focuses on performing Exploratory Data Analysis (EDA) on a cab booking dataset to extract actionable insights that can help improve customer satisfaction, driver efficiency, and overall business performance.

By analyzing bookings, drivers, trips, and customer feedback, the project aims to answer key business questions and provide data-driven recommendations.

🔹 Objective

The main objectives of this project are:

1. Customer Analysis

* Identify customers with high cancellation rates

* Predict customers likely to stop using the service

2. Driver Performance Analysis

* Identify top-performing and underperforming drivers

* Analyze driver ratings vs earnings and trip patterns

3. Trip & Revenue Analysis

* Evaluate busiest routes and days

* Analyze revenue trends by cab type and trip distance

* Calculate waiting times and operational efficiency

4. Operational Insights

* Identify cancellation reasons from customer feedback

* Determine peak demand periods for optimized cab allocation

* Suggest improvements for revenue and service quality


🔹 Dataset & Schema

The project uses a relational database schema with the following tables:

1. Customers – Customer details (ID, Name, Signup Date)

2. Drivers – Driver details (ID, Name, Rating, Cab Type)

3. Bookings – Trip information (Booking Time, Trip Start/End, Status, Pickup & Dropoff, Fare, Distance)

4. Feedback – Customer feedback and cancellation reasons





## Schema Diagram:



```bash
+------------+       +-----------+       +-----------+       +---------+
| Customers  |       | Drivers   |       | Bookings  |       | Feedback|
+------------+       +-----------+       +-----------+       +---------+
| customer_id|<----->| driver_id |<----->| booking_id|<----->|booking_id|
| name       |       | name      |       | customer_id|      | rating  |
| signup_date|       | rating    |       | driver_id |      | comments|
+------------+       | cab_type  |       | booking_time|    | cancellation_reason|
                     +-----------+       | trip_start_time|
                                         | trip_end_time |
                                         | status       |
                                         | pickup_loc   |
                                         | dropoff_loc  |
                                         | fare         |
                                         | distance_km  |
                                         +-----------+

```



🔹 Analysis Performed

1. Customer Analysis

* Customers with >30% cancellations

* Predicting churn based on booking frequency and last booking date

2. Driver Analysis

* Top 5 drivers with longest trips

* Drivers with high cancellations or low ratings

* Correlation between ratings, trips, and earnings

3. Trip & Revenue Analysis

* Total revenue trends over the last 6 months

* Most popular routes (Pickup → Dropoff)

* Average waiting time by pickup location

* Revenue contribution of short vs long trips

* Comparison of Sedan vs SUV revenue

4. Operational Insights

* Most common cancellation reasons

* Weekend vs weekday booking patterns

* Recommendations for surge pricing and cab allocation


🔹 Tools & Technologies Used

* Database: MySQL / Hive / PostgreSQL

* Querying: SQL for aggregation, filtering, and analytics

* Visualization: Power BI / Tableau / Matplotlib & Seaborn

* Python Libraries: Pandas, NumPy, Matplotlib, Seaborn

* Version Control: Git & GitHub


🔹 Key Insights

* Peak demand days and routes can be optimized for better cab availability.

* Higher-rated drivers complete more trips and generate more revenue.

* Customers with frequent cancellations can be targeted for retention strategies.

* Short trips contribute significantly to revenue, while Sedans generate more earnings than SUVs in this dataset.

* Weekend bookings show higher fare patterns, suggesting potential for dynamic pricing.


🔹 Future Enhancements

* Build predictive models for customer churn and trip demand

* Implement real-time dashboards for operational monitoring

* Optimize driver allocation using ML algorithms

* Integrate dynamic pricing strategies