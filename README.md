# Real Estate Property Price Analysis
## What this project does:
This is a data engineer project which focuses on exploring the relationship between real estate property prices and various property characteristics, as well as external factors. The primary objective is to gain insights into the factors influencing property prices and assess the accuracy of Zillow zestimates compared to actual listing prices. Additionally, the project examines the impact of factors such as inflation, Covid conditions, demographic data, and socio-economic conditions of the property's respective zipcode area.

## How this project works:
This project follows a data processing pipeline that involves data collection, processing, and visualization. A high-level summary of the architecture is shown in the diagram below.

First, relevant data is collected and compiled from various sources. This data is then stored in an **AWS S3 bucket** as **delta tables**, ensuring efficient storage and retrieval.

Next, the **Medallion Architecture** is applied to process and transform the collected data. Using **PySpark** in the **Databricks** platform, the data is structured into **bronze, silver, and gold** tables. This process involves cleaning, filtering, and aggregating the data to derive meaningful insights.

The processed data is stored back in the AWS S3 bucket, maintaining the **Delta table** format for enhanced data integrity and performance.

In the serving layer, **Power BI** is utilized to visualize the analytic findings, enabling the creation of insightful visualizations and reports.

To ensure smooth execution and monitoring of the project, **Airflow** is employed for orchestrating and scheduling the data processing pipeline. Airflow handles the automation of job workflows, allowing for efficient job execution and management.
