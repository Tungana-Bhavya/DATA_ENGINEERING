## Scenario 2: Customer Data Cleaning and Validation using SQL

An e-commerce company receives customer registration data from multiple sources. Some customer records contain missing mandatory information due to:</br>

- Customers skipping fields</br>
- Source system issues</br>
- Incomplete file uploads</br>

The data engineering team must clean customer data and validate that mandatory fields are available.

### 1.0 Objective

- Detect missing customer values.
- Standardize missing values.
- Remove invalid customer records based on business rules.
- Validate cleaned customer data.

### 1.1 Business Rules</br>
#### 1.1.1 Email Rules
- Email cannot be NULL.
- Email cannot be empty.
- Email cannot contain only spaces.
- Email cannot contain placeholder values.
- Email should not contain leading\trailing spaces.

#### 1.1.2 Phone Rules
- Phone cannot be NULL.
- Phone cannot be empty.
- Phone cannot contain only spaces.
- Phone cannot contain placeholder values such as "NULL", "N/A", "NA", "NaN", "NONE", "UNKNOWN".

### 1.2 Cleaning Steps
- Remove leading and trailing spaces from string columns.
- Convert empty values ("") into NULL.
- Convert blank values (spaces only) into NULL.
- Convert placeholder values ("NULL", "N/A", "NaN", "NONE") into NULL.
- Standardize missing values into a common format.

### 1.3 Validation
- Check mandatory fields after cleaning.
- Validate that Email and Phone fields are available.
- Identify valid and invalid customer records.
- Separate valid records and rejected records.

### 3.0 Key Learnings
- Identified missing and inconsistent values through data profiling.
- Cleaned and standardized empty, blank, and placeholder values.
- Applied Email and Phone validation rules based on business requirements.
- Performed a customer data cleaning and validation workflow using SQL.
- Improved customer data quality through data cleaning and validation.
