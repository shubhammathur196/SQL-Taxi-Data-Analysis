# Taxi Data Exploration

This project demonstrates the exploration and analysis of a real-world taxi service dataset using SQL. The goal is to uncover insights about user behavior, operational efficiency, and business performance using structured queries.

---

## Objectives
1. Analyze user behavior across the customer funnel:
   - From app downloads to ride completions.
   - Identifying drop-offs and conversion rates.
2. Determine peak demand times and popular locations.
3. Evaluate platform usage (iOS, Android, Web).
4. Provide actionable insights for optimizing taxi operations.

---
For detailed database schema, refer to [data_structure.md](database_schema.md).


## Dataset Overview
The dataset is sourced from a real-world taxi service database. It includes the following components:

### 1. **App Downloads**
- Fields: `app_download_key`, `platform` (iOS/Android/Web), `download_timestamp`.

### 2. **User Signups**
- Fields: `user_id`, `session_id` (linked to app downloads), `age_range`, `signup_timestamp`.

### 3. **Ride Requests**
- Fields: `ride_id`, `user_id` (linked to signups), `pickup_location`, `dropoff_location`, `request_timestamp`, `accept_ts`, `pickup_ts`, `dropoff_ts`, `cancel_ts`.

### 4. **Driver Data**
- Fields: `driver_id`, `ride_id` (linked to ride requests), `acceptance_timestamp`, `completion_timestamp`.

### 5. **Transactions**
- Fields: `ride_id` (linked to ride requests), `purchase_amount_usd`, `charge_status` (approved, cancelled), `transaction_ts`.

### 6. **Reviews**
- Fields: `review_id`, `ride_id` (linked to ride requests), `driver_id`, `user_id` (linked to requesters), `rating` (0 to 5), `free_response` (text review).

---

## Tools Used
- **SQL**: For data querying and analysis.
- **Real Database Connection**: Connected to a live database for extracting and analyzing data.

---

## Analysis Summary
Key insights derived from the dataset include:

1. **Customer Funnel Analysis**
   - Calculated conversion rates from app download to ride completion.
   - Identified major drop-off points in the user journey.

2. **Peak Time Analysis**
   - Analyzed ride requests by hour and day to determine peak demand times.

3. **Platform Insights**
   - Evaluated platform usage to identify the most popular channels (iOS/Android/Web).

4. **Location Trends**
   - Mapped pickup and drop-off locations to identify high-demand areas.

---

## How to Use This Repository
1. Clone the repository to your local machine.
2. Use the included documentation to understand the dataset structure.
3. Modify queries or dataset for additional insights.

---
![Alt text](https://images.spr.so/cdn-cgi/imagedelivery/j42No7y-dcokJuNgXeA0ig/1b13ef4a-bdb0-45e0-914b-f46f74895552/Metrocar_car/w=1080,quality=90,fit=scale-down")

## Disclaimer
This project uses a real-world dataset accessed via a live database connection. All data has been used responsibly and without violating any privacy or confidentiality agreements.
