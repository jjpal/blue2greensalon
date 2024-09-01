# Data Dictionary - Data Sources and Elements

## Tables
- bookings
- service_listing
- product_listing
- receipt_transactions
- cancel_noshows
- personnel
- reviews
- locations

## Tables with Corresponding Columns (enhanced datasets)
* bookings table
    - Columns:
     - Booking_ID: unique booking identifer
     - Client_Code:	unique client code
     - Stylist: staff member to provide the service
     - Service_Code: service code for the booking
     - Booking_Date: date the service is scheduled to be provided.	
     - Booking_Time: time the service is scheduled to be provided.

* service_listings
    - Columns:
     - Service_ID: unique service identifier	
     - IsActive_Service: Is this an active service?	
     - Service_Code: service code for the booking	
     - Service_Desc: service name
     - Service_Category: service category descriptor	
     - Service_Price: price of the service. (Note: price varies across staff)
     - StPrd4Sv_Cost: the amount the staff pays to the salon for professional product costs.

* product_listings
    - Columns:
     - Product_ID
     - IsActive_Product	
     - Product_code	
     - Product_Description
     - Prod_Supplier
     - Prod_Brand	
     - Product_Category
     - Product_Price
     - Prod_OnHand
     - Prod_Min	
     - Prod_Max	
     - Unit_Cost
     - Prod_COG
     - YTD_Sales


