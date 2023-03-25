# Airline Tracker Project

This project is a data-driven application that tracks airlines. It uses a database that is created in AWS and crawled in AWS and Redshift.

# Database Design

The database design includes seven tables:

Passengers: Contains information about Passenger name, emal, and age.
Airlines: Contains information about airlines, such as name, country.
Routes: Contains information about flight routes, such as airline, origin airport, destination airport.
Airport: contains information about airport name, city and country
Flights: contains information about departure and arrival time and date and route the airplane took.
Bookings: contains information about class, seat_number, passnger_id, and flight_ id/
pilots: contains information about name of pilots and level of experience


# Data Collection

To collect the data, Python scripts  was used to retrieve data using faker and kaggle. Afterwards data was loaded into postgres database using python scriptsand manual ingestion using DBeaver import tool. The data is then transformed and loaded into S3 using AWS Glue, which is a fully managed ETL (extract, transform, load) service.

The Glue ETL jobs use Python scripts to perform the following tasks:

Extract: Retrieve data from various sources, including airline and airport websites.
Transform: Clean, enrich, and normalize the data to fit the database schema.
Load: Insert the transformed data into the appropriate database tables.
Data Analysis
Once the data is in the database, it can be analyzed and visualized using various tools, such as SQL queries, Python scripts, and data visualization libraries.

# Deployment

The application is deployed on AWS, using the following services:

AWS Glue: For ETL jobs to populate the database.
Amazon Redshift: For the database storage and querying.
Amazon S3: For storing the data files and ETL job artifacts.

# Conclusion

This project demonstrates how AWS services can be used to build a scalable and robust data-driven application. By using Glue, Redshift, RDS,S3 we can collect, transform, store, and analyze large volumes of data with ease. The application can be extended and customized to meet specific business needs, and can serve as a foundation for more advanced data-driven applications.
