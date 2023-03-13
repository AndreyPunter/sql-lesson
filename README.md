# SQL lessons at [Northeastern](https://www.nulondon.ac.uk/) Skills Bootcamp

This is a repository with notes on how to learn SQL using [BigQuery](https://console.cloud.google.com/bigquery)

## Steps to start using BigQuery without listing your bank card

1. Sign up to [Google Cloud console](https://console.cloud.google.com/) wiht your personal email (NU London student emails will not work for some reason)
2. 

## The setup

![set up](bq_setup.png)

## The queries to try

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

```sql
SELECT count(artist_end_date) as artists_who_died
FROM
  `bigquery-public-data.the_met.objects`;
  ```

```sql
SELECT (count(artist_end_date)/count(*))*100 as artists_who_died
FROM
  `bigquery-public-data.the_met.objects`;
  ```

```sql
SELECT
  region,
  COUNT(object_number) AS count_objects
FROM
  `bigquery-public-data.the_met.objects`
GROUP BY
  region
ORDER BY
  count_objects DESC;
```
