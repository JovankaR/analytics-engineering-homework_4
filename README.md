# analytics-engineering-homework_4
Codespaces for Homework 4

# Homework 4 

```sql

SELECT pickup_zone,
SUM(revenue_monthly_total_amount) AS total_revenue
FROM `data-warehousing-486717.nytaxi.fct_monthly_zone_revenue` 
WHERE service_type='Green'
AND EXTRACT (year FROM revenue_month)=2020
GROUP BY pickup_zone
ORDER BY total_revenue DESC;



SELECT SUM(total_monthly_trips) AS total_number
FROM `data-warehousing-486717.nytaxi.fct_monthly_zone_revenue` 
WHERE service_type='Green'
AND EXTRACT (year FROM revenue_month)=2019 and extract (month FROM revenue_month)=10;



SELECT COUNT(*) FROM `data-warehousing-486717.nytaxi.fhv_tripdata` 
WHERE dispatching_base_num IS NOT NULL

```
# Screenshot

![dbt models](pics/bq_models.png)

