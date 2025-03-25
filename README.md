# HR Data Analysis using PySpark
This project demonstrates the use of Apache Spark with PySpark for analyzing HR data, performing data exploration, transformation, and model building. The dataset used in this project is from Kaggle's "Human Resources Data Set," which is used for employee performance and salary analysis.

## Requirements
To run the project, you will need the following Python libraries:

- pyspark==3.1.2
- findspark
- kagglehub

You can install the required packages using the following commands:

```bash
pip install pyspark==3.1.2 -q
pip install findspark -q
```

## Setup and Initialization
1. Importing Libraries: The necessary libraries for Spark and data manipulation are imported, including pyspark.sql, kagglehub, and other essential functions.
2. Initialize Spark Session: Spark session is initialized to create a connection to the Spark cluster.
3. Dataset Loading: The dataset is downloaded using kagglehub.dataset_download and read into a PySpark DataFrame.

## Data Exploration
1. Schema and Data Overview:
  - Display the schema of the dataset.
  - Show the first 3 rows for quick inspection.

2. Check for Duplicates and Null Values:
  - Count the number of duplicate rows and drop them.
  - Identify columns with null values and drop them.

## Data Transformation
1. Add New Columns:
  - A new column "PermanentEmployee" is added with the value "yes".

2. Data Selection:
  - Columns for numerical analysis are selected, including MaritalStatusID, GenderID, and others.

## Exploratory Data Analysis (EDA)
1. Summary Statistics:
  - Display summary statistics for selected columns.

2. Unique Values:
  - Show distinct values for columns such as "PerformanceScore" and "GenderID".

3. Filter Data:
  - Filter data based on specific conditions like performance score or absence.

## Data Manipulation
1. Salary Adjustments:
- Increase salary by 10% for employees with "Exceeds" performance score.
- Deduct 5% from employees with more than 19 absences.

2. Date Transformations:
- Convert DateofHire and DateofTermination into date format.
- Calculate the tenure of employees by subtracting the hiring date from the termination date.

## Aggregation & Grouping
1. Group by Department: Show average salary, min/max salary, and average employee satisfaction per department.

2. Employee Satisfaction Count: Show the count of employees based on satisfaction levels.

## Sorting and Caching
1. Sorting:
  - Show employees sorted by tenure.

2. Caching:
  - Cache the DataFrame to improve performance in future actions.

## Joins, Partitioning, and Repartitioning
Joins can be performed between DataFrames, and the data can be partitioned or repartitioned for efficient parallel processing.

## Exploding
- Explode an array column (Language) into separate rows.

## Feature Engineering
- Vector Assembly: Assemble the selected columns into a feature vector for model building.

## Model Building
1. Linear Regression: Train a linear regression model to predict employee salaries based on the features.

2. Model Evaluation: Evaluate the model using R-Squared and RMSE (Root Mean Squared Error).

## Stopping the Spark Session
After all tasks are completed, the Spark session is stopped to release resources.

```python
spark.stop()
```

## Running the Project
To run the project:
1. Install dependencies.
   
2. Run the Python script for data exploration, transformation, and model building.

3. Review the output for insights, model evaluation metrics, and data analysis.

## License
This project is licensed under the Raza Mehar License. See the LICENSE.md file for details.

## Contact
For any questions or clarifications, please contact Raza Mehar at [raza.mehar@gmail.com].
