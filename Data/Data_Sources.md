# Data Sources

## Primary Dataset — NYC Citi Bike Trips
This project uses the publicly available NYC Citi Bike Trips dataset hosted on Google BigQuery.

**Access the dataset here:**
[bigquery-public-data.new_york_citibike](https://console.cloud.google.com/bigquery?ws=!1m4!1m3!3m2!1sbigquery-public-data!2snew_york_citibike)

> The raw trip data is not uploaded here due to its size. Use the BigQuery link above to access the full dataset.

---

## Secondary Dataset — Zip Code Table
A custom zip code reference table (`zip_codes.csv`) is included in this folder.
It maps station IDs to zip code, neighborhood, and borough — used to enrich the trip data during the SQL JOIN step in BigQuery.
