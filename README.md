# Diabetes-Prediction
Disease Prediction
Diabetes Dataset Analysis and Data Cleaning Process

Firstly, we download the Diabetes CSV file from Google and upload it to Google Colab. Then, we import the Pandas library and read the CSV file using the read_csv() function. We copy the file path by clicking on the three dots next to the uploaded file and paste it into the read_csv() function.

After loading the dataset, we use the head() function to display the first few rows of the dataset (or head(10) to display the first 10 rows). We use the tail() function to display the last few rows. The shape attribute is used to find the total number of rows and columns in the dataset. The info() function provides information about the dataset, such as the data types and non-null values. The columns attribute is used to display the names of all the columns, and the describe() function is used to obtain the statistical summary of the numerical data.

This completes the first step, which is loading and analyzing the dataset.

In the second step, we clean the data. First, we use the isnull().sum() function to check the number of missing (null) values in each column. Then, we use the value_counts() function to count the occurrences of values in a particular column, such as the Diabetes column.

Next, we create a list named cols that contains all the column names except the Diabetes column. We use (df[cols] == 0).sum() to count the number of zero values in these columns because, in this dataset, zero values in some columns represent missing data.

After that, we import the NumPy library and replace all zero values with NaN using the replace() function. We again use isnull().sum() to check the number of missing values.

Finally, we use a for loop to fill the missing values in each column with the median value of that column. After filling the missing values, we use isnull().sum() once again to verify that all missing values have been handled successfully.
