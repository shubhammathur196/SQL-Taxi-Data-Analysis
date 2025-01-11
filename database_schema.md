# Database Schema: Taxi Data Exploration

This file describes the schema of the database used in the Taxi Data Exploration project.

---

## **Tables and Columns**

### 1. App Downloads
| Column Name       | Data Type | Description                      |
|--------------------|-----------|----------------------------------|
| app_download_key   | STRING    | Unique ID of the app download    |
| platform           | STRING    | Platform (iOS, Android, Web)    |
| download_timestamp | TIMESTAMP | Time of app download            |

### 2. User Signups
| Column Name       | Data Type | Description                      |
|--------------------|-----------|----------------------------------|
| user_id           | STRING    | Unique ID of the user            |
| session_id        | STRING    | Linked to app downloads          |
| age_range         | STRING    | Age group of the user            |
| signup_timestamp  | TIMESTAMP | Time of signup                   |

### 3. Ride Requests
| Column Name         | Data Type | Description                         |
|----------------------|-----------|-------------------------------------|
| ride_id             | STRING    | Unique ID of the ride               |
| user_id             | STRING    | Linked to user signups              |
| driver_id           | STRING    | Linked to driver                    |
| pickup_location     | STRING    | Pickup coordinates                  |
| destination_location| STRING    | Drop-off coordinates                |
| request_timestamp   | TIMESTAMP | Time of ride request                |
| accept_timestamp    | TIMESTAMP | Time of driver acceptance           |
| pickup_timestamp    | TIMESTAMP | Time of pickup                      |
| dropoff_timestamp   | TIMESTAMP | Time of dropoff                     |
| cancel_timestamp    | TIMESTAMP | Time of cancellation (if applicable)|

### 4. Driver Data
| Column Name       | Data Type | Description                      |
|--------------------|-----------|----------------------------------|
| driver_id         | STRING    | Unique ID of the driver          |
| ride_id           | STRING    | Linked to ride requests          |
| acceptance_timestamp| TIMESTAMP| Time of driver acceptance        |
| completion_timestamp| TIMESTAMP| Time of ride completion          |

### 5. Transactions
| Column Name       | Data Type | Description                      |
|--------------------|-----------|----------------------------------|
| ride_id           | STRING    | Linked to ride requests          |
| purchase_amount_usd| DECIMAL   | Amount charged for the ride      |
| charge_status     | STRING    | Status (approved, cancelled)     |
| transaction_timestamp| TIMESTAMP| Time of transaction              |

### 6. Reviews
| Column Name       | Data Type | Description                      |
|--------------------|-----------|----------------------------------|
| review_id         | STRING    | Unique ID of the review          |
| ride_id           | STRING    | Linked to ride requests          |
| driver_id         | STRING    | Linked to driver                 |
| user_id           | STRING    | Linked to user                   |
| rating            | INTEGER   | Rating given by the user (0-5)   |
| free_response     | TEXT      | Free-text response by the user   |

---

## Notes
- Data types are based on the SQL database.
- The schema is provided to help understand the dataset structure.

