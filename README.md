```markdown
# Synthetic Data Generation for Two Tables with Foreign Key Relationship

This code demonstrates how to generate synthetic data for two tables with a foreign key relationship using BigFrames and Gemini. 

## Overview

The code generates synthetic data for two tables: `customers` and `orders`. The `orders` table has a foreign key relationship with the `customers` table, referencing the `customer_id` column.

The data generation process involves the following steps:

1. **Define the schema for each table:** The schema defines the columns, data types, and descriptions for each table.
2. **Generate synthetic data for the `customers` table:** BigFrames and Gemini are used to generate a Pandas DataFrame containing synthetic customer data based on the defined schema.
3. **Generate synthetic data for the `orders` table:** BigFrames and Gemini are used to generate a Pandas DataFrame containing synthetic order data based on the defined schema. The `customer_id` column in the `orders` table is populated with values referencing existing customer IDs from the `customers` table.
4. **Print the generated DataFrames:** The generated `customers` and `orders` DataFrames are printed to the console.

## Requirements

* BigFrames
* Gemini
* Faker

## Usage

1. Install the required packages:
```bash
pip install bigframes google-cloud-aiplatform faker pandas
```
2. Set the `PROJECT_ID` variable in the code to your Google Cloud Project ID.
3. Run the code:
```bash
python generate_synthetic_data.py
```

## Output

The code will output two Pandas DataFrames: `customers_df` and `orders_df`. These DataFrames contain the generated synthetic data for the `customers` and `orders` tables, respectively.

## Note

The number of rows generated for each table can be adjusted by modifying the `desired_num_rows` and `batch_size` variables in the code.

## Example

The generated `customers` DataFrame might look like this:

| customer_id | Name | Email |
|---|---|---|
| 1 | John Smith | john.smith@example.com |
| 2 | Jane Doe | jane.doe@example.com |
| ... | ... | ... |

The generated `orders` DataFrame might look like this:

| order_id | customer_id | order_date | order_amount |
|---|---|---|---|
| 1 | 1 | 2023-11-20 | 100.00 |
| 2 | 2 | 2023-11-21 | 50.00 |
| ... | ... | ... |


## Disclaimer

This code is intended for demonstration purposes only. The generated synthetic data may not be representative of real-world data.
```
