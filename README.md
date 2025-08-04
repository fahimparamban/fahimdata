import pandas as pd

# Load your dataset (update file name)
df = pd.read_csv("your_dataset.csv")  # or .xlsx if using Excel

# Show the first few rows
print("First 5 rows:")
print(df.head())

# Check for missing values
print("\nMissing values per column:")
print(df.isnull().sum())

# Drop duplicates
df = df.drop_duplicates()

# Drop rows with missing values
df = df.dropna()

# Save the cleaned data
df.to_csv("cleaned_dataset.csv", index=False)
print("\nCleaned data saved as cleaned_dataset.csv")

