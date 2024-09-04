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
     - IsActive_Service: Is the service activee?	
     - Service_Code: service code for the booking	
     - Service_Desc: service name
     - Service_Category: service category descriptor	
     - Service_Price: price of the service. (Note: price varies across staff)
     - StPrd4Sv_Cost: the amount the staff pays to the salon for professional product costs.

* product_listings
  - Columns:
     - Product_ID: unique product identifier	
     - IsActive_Product: Is the product active?	
     - Product_code: the product description	
     - Product_Description: the product supplier
     - Prod_Supplier: the product supplier
     - Prod_Brand: the product brand	
     - Product_Category: the product category
     - Product_Price: the regular price
     - Prod_OnHand: the number of units on hand
     - Prod_Min: minimum recommended product inventory	
     - Prod_Max: maximum recommended product inventory	
     - Unit_Cost: the unit cost of the product
     - Prod_COG: the total cost of all units.
     - YTD_Sales: year to date sales

* receipt_transactions
  - Columns:
     - Transaction_Receipt_ID: receipt number
     - Payment_Date:  date of the transaction.
     - Receipt_Description:  service or product name
     - Client_Code: unique client code.
     - Stylist:  staff member who provided the service or sold the product.
     - Receipt_Quantity: number of services or product sold.
     - Receipt_Amount: the total dollar amount.
     - tax1: Federal tax amount.
     - tax2: local tax amount.
     - Payment_Method: way client paid for service or product

* cancel_noshows
  - Columns:    
     - Code: unique client code
     - Service: service code for the booking
     - Staff: staff member who was to provide the service
     - Booking_Date: date the service was scheduled to be provided
     - Event_Date: date or cancellation or missed appointment
     - Appointment_Status: indicator for appointmenta that were cancelled or missed
     - Canceled_By: staff that received call for cancellation
     - Notification_Days: number of days before appointment or -1 for no-shows

* personnel
 - Columns:
  -   

* reviews
 - Columns:
  -   

* locations
 - Columns:
  -   
