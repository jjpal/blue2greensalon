# Data Dictionary - Tables and Elements

## Tables
- bookings
- service_listing
- product_listing
- receipt_transactions
- cancel_noshows
- personnel
- reviews
- locations
- promotions

## Tables with Corresponding Columns (enhanced datasets)
* bookings 
  - Columns:
     - booking_id: unique booking identifer
     - client_code:	unique client code
     - stylist: staff member to provide the service
     - service_code: service code for the booking
     - booking_date: date the service is scheduled to be provided
     - booking_time_mer: time the service (12-hour convention + meridiem) scheduled to be provided
     - booking_time: time (only) the service scheduled to be provided
     - tod: meridiem AM or PM
     - service_id: unique service identifier 
  - Format: CSV  

* service_listings
  - Columns:
     - service_id: unique service identifier	
     - isActive_service: Is the service activee	
     - service_code: service code for the booking	
     - service_desc: service name
     - service_category: service category descriptor	
     - service_price: price of the service (Note: price varies across stylists)
     - stPrd_cost: amount the stylist pays to the salon for professional product costs
  - Format: CSV   

* product_listings
  - Columns:
     - product_id: unique product identifier	
     - isActive_product: Is the product active	
     - product_code: product code 
     - product_desc: product description
     - prod_supplier: product supplier
     - prod_brand: product brand	
     - prod_category: product category
     - prod_price: the regular price
     - prod_onHand: the number of units on hand
     - prod_min_qty: minimum recommended product inventory	
     - prod_max_qty: maximum recommended product inventory	
     - unit_cost: the unit cost of the product
     - prod_cog: the total cost of all units
     - ytd_sales: year to date sales
   - Format: CSV   

* receipt_transactions 
  - Columns:
     - receipt_id: receipt number
     - payment_date: date of the transaction
     - receipt_desc: description of service or product name
     - client_code: unique client code
     - stylist: staff member who provided the service or sold the product
     - receipt_qty: number of services or product sold
     - receipt_amount: the total dollar amount
     - tax1: federal tax amount
     - tax2: local tax amount
     - payment_method: way client paid for service or product
     - service_id: 
     - promo_id: 
     - promo_name: 
     - disc_dlr_amt: discount dollar amount
     - staff_id: 
     - salon_id: 
   - Format: CSV   
      **Note**: enriched with additional datasets  

* cancel_noshows 
  - Columns:
     - client_code: unique client code
     - service_code: service code for the booking
     - stylist: member who was to provide the service
     - booking_date: date the service was scheduled to be provided
     - appointment_status: indicator for appointmenta that were cancelled or missed
     - event_date: date or cancellation or missed appointment
     - canceled_by: staff that received call for cancellation
     - notification_days: number of days before appointment or -1 for no-shows
   - Format: CSV   

* personnel 
  - Columns:
     - staff_id: unique personnel code	
     - preferred_name: staff member name
     - title: staff title
     - staff_address: hashed address
     - staff_phone_number: hashed phone number
     - start_date: staff start date	
     - years_experience: staff years of experience
   - Format: CSV   
      **Note**: partially extracted of original dataset and enriched with additional datasets  
      
* reviews
  - Columns:
     - review_id: unique review code
     - rating: client rating
     - review: client review
     - review_date: date of review
     - service_id: unique service identifier
   - Format: CSV   
      **Note**: enriched with additional datasets 

* locations
  - Columns:
     - salon_id: unique salon code
     - salon_name: salon name
     - salon_email: salon email
   - Format: CSV   
      **Note**: mock data     

* promotions
  - Columns:
     - promo_id: unique promo code
     - promo_name: campaign description
     - discount_dlr_amt: discount dollar amount
     - isActive_promo: Is the promotion active
   - Format: CSV   
      **Note**: mock data          


