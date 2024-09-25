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
     - service_id: unique service identifier	
     - product_id: unique product identifier
     - promo_id: unique promo code
     - disc_dlr_amt: discount dollar amount
     - staff_id: unique personnel code	
     - salon_id: unique salon code
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
     - last_active: date campaign was last active
   - Format: CSV   
      **Note**: mock data          

----------

bookings	
----------
| data type		| column	 		      | 	
|-------------|-------------------|
| STRING	    | booking_id  		  |
| STRING	 	  | client_code		    |
| STRING	 	  | stylist        	  |
| STRING	 	  | service_code		  |
| DATE	 		  | booking_date		  |
| STRING	 	  | booking_time_mer	|
| TIME	 		  | booking_time		  |
| STRING	 	  | tod				        |

service_listings	
----------
| data type		| columns	 		      |
|-------------|-------------------|
| STRING      |	service_id        |
| BOOLEAN     |	isActive_service  |
| STRING	    | service_code      |
| STRING      |	service_desc      |
| STRING	    | service_category  |
| FLOAT	      | service_price     |
| FLOAT       |	stPrd_cost        |

product_listings
----------
| data type		| columns	 		      |
|-------------|-------------------|
| STRING      | product_id        |
| BOOLEAN     |	isActive_product  |
| STRING	    | product_code      |
| STRING	    | product_desc      |
| STRING	    | prod_supplier     |
| STRING	    | prod_brand        |
| STRING	    | prod_category     |
| FLOAT       | prod_price        |
| INT         | prod_onHand       |
| INT         | prod_min_qty      |
| INT         | prod_max_qty      |
| FLOAT       | unit_cost         |
| FLOAT       | prod_cog          |
| FLOAT       | ytd_sales         |

receipt_transactions
----------
| data type		| column	 		      | 	
|-------------|-------------------|
| STRING	    | receipt_id        |
| BOOLEAN     | payment_date      |
| STRING	    | receipt_desc      |  
| STRING	    | client_code       |   
| STRING	    | stylist           |   
| INT         | receipt_qty       |  	
| INT   	    | receipt_amount    |   
| FLOAT       | tax1              |
| FLOAT       | tax2              |
| STRING	    | payment_method    |
| STRING	    | service_id        |   
| STRING	    | promo_id          |  
| FLOAT       | disc_dlr_amt      |    
| STRING	    | staff_id          |
| STRING	    | salon_id          |
    	
cancel_noshows
----------
| data type		| column	 		       | 
|-------------|--------------------|
| STRING	    | client_code        |
| STRING	    | service_code       |
| STRING	    | stylist            |
| DATE  	 	  | booking_date       |
| STRING	    | appointment_status |
| DATE  	 	  | event_date         | 
| STRING	    | canceled_by        |
| INT   	    | notification_days  |

personnel
----------
| data type		 | column	  		      | 
|--------------|--------------------|
| STRING	     | staff_id           |
| STRING	     | preferred_name     |
| STRING	     | title              |
| STRING	     | staff_address      |
| STRING	     | staff_phone_number |
| DATE  	 	   | start_date         |
| INT   	     | years_experience   |

reviews
----------
| data type		| column	 		      | 
|-------------|-------------------|
| STRING	    | review_id         |
| INT   	    | rating            |
| STRING	    | review            |
| DATE  	 	  | review_date       |
| STRING	    | service_id        |

locations
----------
| data type		| column	 		      |
|-------------|-------------------| 
| STRING	    | salon_id          |
| STRING	    | salon_name        |
| STRING	    | salon_email       |

promotions
----------
| data type		| column	 		      | 
|-------------|-------------------|
| STRING	    |  promo_id         |
| STRING	    |  promo_name       |
| STRING	    |  discount_dlr_amt |
| STRING	    |  isActive_promo   |
| STRING	    |  last_active      |      