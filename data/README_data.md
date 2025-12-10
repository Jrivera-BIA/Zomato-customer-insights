# Data Overview

The original project used two CSV files provided as part of the TripleTen Business Intelligence program.  
For privacy and licensing reasons, the raw data files are **not included** in this repository.

## Tables

### `users` table (user-level demographics)

- `user_id` – unique user identifier  
- `Age` – user age (integer)  
- `Gender` – categorical  
- `Marital_Status` – categorical  
- `Occupation` – categorical  
- `Monthly_Income` – binned income category  
- `Educational_Qualifications` – categorical  
- `Family_size` – integer  

### `orders` table (transaction-level data)

- `order_id` – unique order identifier  
- `user_id` – links to `users.user_id`  
- `order_date` – date of the order  
- `sales_amount` – revenue for the order  
- `sales_qty` – quantity/items in the order  
- `restaurant_id` – restaurant identifier  

If you’d like to recreate this analysis yourself, you can plug in any similar user/order dataset 
(or a synthetic dataset) that follows this schema.
