# sql-lesson

This is how to learn SQL using [BigQuery](https://console.cloud.google.com/bigquery)

![set up](bq_setup.png)

```sql
SELECT
  *
FROM
  `bigquery-public-data.usa_names.usa_1910_current`
LIMIT
  10;
 ```

```sql
SELECT
  MIN(date) AS min_date,
  MAX(date) AS max_date
FROM
  `bigquery-public-data.covid19_weathersource_com.county_day_history`;
  ```
