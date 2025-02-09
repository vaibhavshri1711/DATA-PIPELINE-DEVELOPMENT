# TASK-1: DATA-PIPELINE-DEVELOPMENT

COMPANY: CODTECH IT SOLUTIONS

NAME: GHODKE VAIBHAVSHRI VISHWANATH

INTERN ID: CT12IBE

DOMAIN: DATA SCIENCE

DURATION: 8 WEEEKS

MENTOR: NEELA SANTOSH

The task at hand involves creating a data processing pipeline using Python, specifically leveraging libraries such as Pandas and Scikit-learn. The goal is to load a dataset, preprocess it, and then save the transformed data for further analysis or modeling. Below, I will break down the steps involved in this task, explaining each part in simple terms.

Step 1: Importing Libraries
The first step is to import the necessary libraries. We use:

Pandas: This library is great for data manipulation and analysis. It allows us to work with data in a tabular format (like spreadsheets).
Scikit-learn: This is a powerful library for machine learning in Python. It provides tools for preprocessing data, building models, and evaluating them.

Step 2: Loading Data
Next, we define a function called load_data that takes a file path as an argument. 
This function uses Pandas to read a CSV file and return it as a DataFrame.
A DataFrame is like a table where we can easily access and manipulate our data.

Step 3: Preprocessing Data
Once we have our data loaded, we need to preprocess it. 
This is crucial because raw data often contains missing values, categorical variables, and different scales of numerical values. 
The preprocess_data function handles this by:

Separating Features and Target: We split the data into features (the input variables) and the target (the output variable we want to predict).

Identifying Data Types: We identify which columns are categorical (like names or categories) and which are numerical (like age or salary).

Setting Up Transformers: We create two pipelines:
For numerical data, we use an imputer to fill in missing values with the mean of the column and then scale the data to have a mean of 0 and a standard deviation of 1.
For categorical data, we also use an imputer to fill in missing values, but we replace them with the most frequent value.
After that, we apply one-hot encoding, which converts categorical variables into a format that can be provided to machine learning algorithms.
Combining Transformers: Finally, we combine these transformers into a single ColumnTransformer that applies the appropriate transformations to the respective columns.

Step 4: Creating a Pipeline
After preprocessing, we create a function called create_pipeline that takes the preprocessor as an argument.
This function creates a pipeline that includes the preprocessing steps.
A pipeline is a way to streamline the process of transforming data and training models, ensuring that the same transformations are applied consistently.

Step 5: Saving Transformed Data
We also define a function called save_transformed_data that takes the transformed data and an output path.
This function saves the transformed data back to a CSV file.
It ensures that the directory for the output file exists before saving.

Step 6: Main Function
The main function is where everything comes together. Here’s what it does:

1.File Paths: It defines the input and output file paths.
2.Loading Data: It calls the load_data function to read the data from the specified file.
3.Preprocessing: It calls the preprocess_data function to prepare the data for analysis.
4.Creating the Pipeline: It creates a pipeline using the preprocessor.
5.Fitting and Transforming: It fits the pipeline to the data and transforms it. This step applies all the preprocessing steps we defined earlier.
6.onverting to DataFrame: After transformation, it converts the transformed data back into a DataFrame for easier handling.
7.Saving the Data: Finally, it saves the transformed data to the specified output file.

OUTPUT:

![Image](https://github.com/user-attachments/assets/17024e24-dc8d-404c-893a-dba0ab16e596)
