# Manipulating_Orders_Dataset_With_PySpark

## Overview  
This project involves cleaning and transforming of (`orders_data.parquet`) using **PySpark** to ensure data consistency and improve its usability. The following steps describe the transformations and cleaning processes applied.

## Cleaning and Transformation Steps  

1. **`order_date`**  
   - **Original:** Timestamp  
   - **Changes:**  
     - Removed orders placed between **12am and 5am** (inclusive).  
     - Converted from **timestamp** to **date** format.

2. **`time_of_day`** (New Column)  
   - **Description:** Categorizes the order time into periods of the day:  
     - **"morning"**: 5am - 12pm  
     - **"afternoon"**: 12pm - 6pm  
     - **"evening"**: 6pm - 12am  

3. **`product`**  
   - **Changes:**  
     - Removed rows where product contains **"TV"** (discontinued product).  
     - Converted all product names to **lowercase**.

4. **`category`**  
   - **Changes:**  
     - Converted all category values to **lowercase**.

5. **`purchase_state`** (New Column)  
   - **Description:** Extracted the **US state** from the `purchase_address` field.

---

## Dependencies  
- **Python 3.x**  
- **PySpark**  
- **pandas** (optional, for additional validation)  
