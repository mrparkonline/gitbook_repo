# Common Data Types in SQL

### **String Data Types**

* **CHAR(size)**: Fixed-length string. The size parameter specifies the length of the string. Example: `CHAR(10)`.
* **VARCHAR(size)**: Variable-length string. The size parameter specifies the maximum length of the string. Example: `VARCHAR(255)`.
* **TEXT**: Variable-length string with a maximum length of 65,535 characters.

### **Numeric Data Types**

* **INT**: Integer data type. Example: `INT`.
* **FLOAT**: Floating-point number. Example: `FLOAT`.
* **DECIMAL(p, s)**: Fixed-point number. The `p` parameter specifies the total number of digits, and the `s` parameter specifies the number of digits after the decimal point. Example: `DECIMAL(10, 2)`.

### **Date and Time Data Types**

* **DATE**: Stores date values in the format `YYYY-MM-DD`.
* **TIME**: Stores time values in the format `HH:MI:SS`.
* **DATETIME**: Stores date and time values in the format `YYYY-MM-DD HH:MI:SS`.
* **TIMESTAMP**: Stores a timestamp value that includes both date and time.

### Reasons to Choose the Proper Data Type for your Columns

1. **Storage Efficiency**: Using the appropriate data type ensures that storage space is used efficiently. For example, using `CHAR(255)` for a field that only needs to store a two-character state code would waste space.
2. **Data Integrity**: The right data type helps maintain data integrity by ensuring that only valid data is stored. For instance, using a `DATE` type for a birthdate field ensures that only valid dates can be entered.
3. **Performance**: Proper data types can improve query performance. Numeric operations on `INT` fields are faster than on `VARCHAR` fields, and indexing is more efficient with appropriate data types.
4. **Validation**: Data types provide a level of validation. For example, a `DECIMAL(10, 2)` type ensures that a price field always has two decimal places.
5. **Readability and Maintenance**: Using the correct data type makes the database schema more readable and easier to maintain. It clearly communicates the kind of data expected in each field.
