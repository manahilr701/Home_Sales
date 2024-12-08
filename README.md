# Home Sales Data Analysis with PySpark

This project leverages **PySpark SQL** to analyze home sales data. The analysis includes creating temporary views, querying data for insights, caching tables, and optimizing performance using Parquet files.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Tasks and Queries](#tasks-and-queries)
- [Results](#results)
- [License](#license)

---

## Project Overview

The **Home Sales Analysis** project uses SparkSQL to answer specific questions about a dataset of home sales. The key focus is on leveraging PySpark for:
- Querying and aggregating data efficiently.
- Enhancing performance through caching.
- Working with Parquet files for storage optimization.

---

## Technologies Used
- **Python** (3.10+)
- **Apache Spark** (3.4.0 or higher)
- **PySpark**
- **Parquet**

---

## Setup Instructions

1. **Install Prerequisites**
   - Ensure that Java (JDK 11 or 17) is installed:
     ```bash
     java -version
     ```
   - Install Apache Spark:
     - Using [Homebrew](https://brew.sh/):
       ```bash
       brew install apache-spark
       ```
     - Or manually download from the [Apache Spark website](https://spark.apache.org/downloads.html).

2. **Clone the Repository**
   ```bash
   git clone https://github.com/manahilr701/Home_Sales.git
   cd Home_Sales
```

## Install Python Dependencies

To get started, install the required Python packages:
```bash
pip install findspark pandas pyarrow fastparquet
```

## Run the Notebook

1. Launch Jupyter Notebook or JupyterLab:
   ```bash
   jupyter notebook
   ```
2. Open Home_Sales.ipynb and execute the cells sequentially.

# Tasks and Queries

### 1. Load and Explore the Data
- Read the dataset into a Spark DataFrame.
- Display the first few rows to understand its structure.

### 2. Create Temporary View
- Create a temporary table from the DataFrame for querying using SQL.

### 3. SQL Queries
- **Average Price of 4-Bedroom Houses by Year**:  
  Calculate the average price for houses with 4 bedrooms, grouped by the year they were sold.

- **Average Price of 3-Bedroom, 3-Bathroom Houses by Year Built**:  
  Determine the average price for houses with 3 bedrooms and 3 bathrooms for each year they were built.

- **Average Price of Specific Homes by Year Built**:  
  Query for houses with 3 bedrooms, 3 bathrooms, 2 floors, and living area ≥ 2,000 sqft.

- **Average Price by View Rating**:  
  Calculate the average price per "view" rating for homes with an average price ≥ $350,000.

### 4. Caching and Optimization
- Cache the temporary table to enhance query performance.
- Compare the runtime of cached vs. uncached queries.

### 5. Parquet Partitioning
- Partition the data by the `date_built` field and save it in Parquet format.
- Reload the Parquet data and query it for the same insights.

---

## Results

The queries and their results provide insights such as:
- Trends in home prices over the years.
- Correlations between home features (e.g., bedrooms, bathrooms, square footage) and price.
- The impact of "view" ratings on home prices.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
