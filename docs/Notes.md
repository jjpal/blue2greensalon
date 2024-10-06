----------

<p align="center">
  Data Type Reference for BigQuery And Snowflake
</p>

----------

[BigQuery Data Types:](https://cloud.google.com/bigquery/docs/reference/standard-sql/data-types)

- INT64: 64-bit signed integer, for storing values like product IDs, counts, or years without decimals.
- NUMERIC: Decimal data type with 38 digits of precision and 9 digits of scale, ideal for exact calculations
- FLOAT64: Double-precision decimal values, suitable for storing floating-point numbers.
- BOOL: Boolean data type, represented by keywords TRUE and FALSE, case-insensitive.
- STRING: Variable-length character data, must be quoted with single or double quotation marks.
- BYTES: Variable-length binary data, not to be used interchangeably with STRING.
- TIMESTAMP: Supports time zones (UTC) used for tracking events (employee hrs, delivery times, or visit logs)
- DATE, TIME, DATETIME: for non-modifying operators like SELECT lists, GROUP BY keys, and window functions.
- STRUCT: A container of ordered fields, each with a type and field name, used for complex data structures.
- ARRAY: An ordered list of zero or more elements of any non-ARRAY type.
- JSON: a lightweight data-interchange format (logical bytes in UTF-8 encoding of the JSON-formatted string)
- RANGE: Contiguous range between two dates, datetimes, or timestamps.
- INTERVAL: A duration of time, without referring to any specific point in time.
- GEOGRAPHY: A collection of points, linestrings, and polygons, represented as a point set, or a subset of the surface of the Earth.

[Snowflake Data Types](https://docs.snowflake.com/en/sql-reference/intro-summary-data-types)

* Numeric data types
  - NUMBER, DECIMAL, NUMERIC
  - INT, INTEGER, BIGINT, SMALLINT, TINYINT, BYTEINT
  - FLOAT, FLOAT4, FLOAT8, DOUBLE, DOUBLE PRECISION, REAL 

* String 
  - VARCHAR
  - CHAR, CHARACTER
  - STRING
  - TEXT

* Binary data types
  - BINARY
  - VARBINARY

* Logical data types
  - BOOLEAN - Currently only supported for accounts provisioned after January 25, 2016.

* Date & Time data types
  - DATE
  - DATETIME
  - TIME
  - TIMESTAMP
  - TIMESTAMP_LTZ - TIMESTAMP with local time zone; time zone, if provided, is not stored.
  - TIMESTAMP_NTZ - TIMESTAMP with no time zone; time zone, if provided, is not stored.
  - TIMESTAMP_TZ - TIMESTAMP with time zone.

* Semi-structured data types
  - VARIANT
  - OBJECT
  - ARRAY

* Geospatial data types
  - GEOGRAPHY
  - GEOMETRY

* Vector data types
  - VECTOR

----------
Data Sources
----------

[Salon original dataset](https://www.kaggle.com/datasets/frederickferguson/hair-salon-no-show-data-set?select=Receipt+Transactions0.csv)

**Future Bookings (All Clients)0.csv**
- Code  - Staff  - Service  - Date  - Time  - TimeInt

**Service Listing0.csv**
- IsActive  - Code  - Desc  - Cate  - Price  - Cost

**Product Listing (Retail0.csv)**
- IsActive  - Code     - Description  - Supplier  - Brand  - Category  - Price  - On Hand  
- Minimum   - Maximum  - Cost         - COG       - YTD    - Package

**Receipt Transactions0.csv**
- Receipt   - Date    - Description  - Client   - Staff
- Quantity  - Amount  - GST          - PST

**Client Cancellations0.csv**
- Cancel Date   - Code          - Service   - Staff
- Booking Date  - Canceled By   - Days

**No-Show Report0.csv**
- Date    - Code    - Service   - Staff

**hair_salon_no_show_wrangled_df.csv**
- Booking index  - book_tod  - book_dow - book_category   - book_staff - last_category - last_staff  
- last_day_services - last_receipt_tot  - last_dow        - last_tod   - last_noshow   - last_prod_flag
- last_cumrev       - last_cumbook      - last_cumstyle   - last_cumcolor   
- last_cumprod      - last_cumcancel    - last_cumnoshow  - noshow     - recency

Additional Data Sources (partially extracted for enrichment)
- [Maven datasets](https://www.mavenanalytics.io/data-playground)
- 

----------
#### Style Guides
[Brooklyn Data Co. SQL style guide](https://github.com/brooklyn-data/co/blob/main/sql_style_guide.md) |
[GitLab's SQL Style Guide](https://handbook.gitlab.com/handbook/enterprise-data/platform/sql-style-guide/) |
[KickStarter's SQL Style Guide](https://gist.github.com/fredbenenson/7bb92718e19138c20591) |
[SQL tips and tricks](https://github.com/ben-n93/SQL-tips-and-tricks#readme)

----------
### Big Query Setup
- Set up a GCP Account 
- Go to BigQuery 
      - Create a dataset: 
          - give the dataset an ID 
          - select the data location 
          - click create dataset button

#### Now load the dataset with data and tables - 2 options
 1] Load the individual CSVs 
   - Select Upload from Create Table From drop-down
   - Select file Browse - file format and destination information will be populated
   - Name the table same as the file (recommended) 
        - auto detect the schema 
        - click create table button

 2] SQL script
   - Select compose new query create/copy-paste scripts
	 - script to create the different tables
	 - script to create the data for the tables
   
 Note: 
- 1st option requires several clicks, less time for small practice project
- 2nd option scripts take less time to write, but will take longer for queries to execute

#### Quickstart 
[dbt Core and BigQuery Setup](https://docs.getdbt.com/guides/manual-install?step=1)

- Create a new GitHub repository 
- Create a dbt project
- Connect to BigQuery
- ...

----------
### Snowflake and dbt Setup
[Snowflake Getting Started](https://docs.snowflake.com/en/user-guide-getting-started)

[dbt and Snowflake Setup](https://docs.getdbt.com/docs/core/connect-data-platform/snowflake-setup)
