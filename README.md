# Apache-Spark-ETL

The focus was on two major aspects: advanced ETL (Extract, Transform, Load) operations and implementing an iterative algorithm.

In the first part, I handled ETL processing of data files. The dataset, sourced from Loudacre's mobile network, comprised device status information like ID, current status, location, etc. I tackled the challenge of varying data formats due to acquisitions from different networks. The data, riddled with inconsistencies in field delimiters, required a meticulous approach to load, parse, and standardize. My key tasks included identifying the correct delimiter, filtering malformed records, and extracting vital fields like date, device model, ID, and geolocation coordinates. I then saved the cleansed data into HDFS, ensuring it was in a uniform, comma-delimited format.

The second part of the project was even more intriguing, where I implemented a k-means clustering algorithm on this processed data. The goal was to group devices based on their geolocation, providing insights into device distributions. I chose a set value of 'K' for the number of clusters and defined a convergence distance to decide the completion of the algorithm. The iterative process involved mapping each coordinate to the nearest cluster point, reducing the dataset to sum coordinates and count points per cluster, and recalculating cluster centers.
