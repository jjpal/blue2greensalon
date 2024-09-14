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

[Salon original dataset](https://www.kaggle.com/datasets/frederickferguson/hair-salon-no-show-data-set?select=Receipt+Transactions0.csv)

Additional Data Sources (partially extracted for enrichment)
[]()