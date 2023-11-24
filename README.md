import pandas as pd
import numpy as np

# Assuming 'data.csv' contains your dataset
data = pd.read_csv('data.csv')

# Descriptive Statistics
print("Descriptive Statistics:")
print(data.describe())

# Calculating Mean, Median, and Standard Deviation
column_of_interest = data['Column_Name']  # Replace 'Column_Name' with the column you're interested in
mean_value = np.mean(column_of_interest)
median_value = np.median(column_of_interest)
std_deviation = np.std(column_of_interest)

print(f"Mean: {mean_value}")
print(f"Median: {median_value}")
print(f"Standard Deviation: {std_deviation}")

# Correlation Matrix
correlation_matrix = data.corr()
print("\nCorrelation Matrix:")
print(correlation_matrix)
