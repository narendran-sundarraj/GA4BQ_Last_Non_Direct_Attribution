# GA4-BigQuery Last Non-Direct Attribution

This project helps you implement a **Last Non-Direct Attribution Model** using **Google Analytics 4 (GA4)** data in **BigQuery**. It uses SQL queries to pull session-level data and attribute conversions based on the most recent non-direct session.

## Purpose

This repo contains SQL queries that allow you to:
- Retrieve session data with traffic source and medium parameters.
- Implement a **Last Non-Direct Attribution Model**.

## Queries

## 1. **sessions_with_traffic_source_and_medium.sql**

This query retrieves all session-level data along with the traffic source, medium, and campaign information for a given date range.

- **[All sessions_with_traffic_source.sql](./sessions_with_traffic_source_and_medium.sql)**

## 2. **get_last_non_direct_attribution.sql**

This query pulls the last non-direct attribution data from the all-session table, ranks sessions by time, and returns the most recent non-direct session's traffic source and medium.

- **[last_non_direct_attribution.sql](./get_last_non_direct_attribution.sql)**

## How to Use

1. **Set up your BigQuery environment** and connect it to your GA4 dataset.
2. **Use the queries from this repository**
3. **Update the table names** in the queries to reflect your actual GA4 export table names.
4. **Run the queries**:
   - First, run the **sessions_with_traffic_source_and_medium.sql** query to extract session data and save it to a new BigQuery table.
   - Then, run the **get_last_non_direct_attribution.sql** query to retrieve the last non-direct session attribution from the results stored in the new BigQuery table.
