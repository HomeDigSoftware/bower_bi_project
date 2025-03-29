

The first step after I loaded the tables 

*************************
 Address => 
 change the type on 	
 city_id& address_id => 
 whole number
remove  address 2 col empty 
**************************
category =>
last_update col change the type to date because all the time stamps were the same so are the date but i left it for now
****************
 city => 
 change the type on  
 country_id  => 
 whole number
	
*********************
 Customer => 
change the type on  
 store_id &  address_id => 
 whole number

********************
film  => 
change the type on  
  rental_duration & length  => 
 whole number
last_update col change the type to date because all the time stamps were as the same so are the date 

 removed => fulltext & language_id  column 
 ***fulltext was corrupted 
 ***language_id has one value and we removed the language table so it's unnecessary 

***********************
film_category =>
 change the type on 	 
 film_id & category_id => 
 whole number
last_update col change the type to date because all the time stamps were the same, and so are the date but I left it for now

***********************
inventory =>	 
change the type on 
 film_id & store_id => 
 whole number

***********************	
Payment & rental  =>
change the type on 
staff_id & customer_id => 
whole number

***********************	
staff  =>
 change the type on   
 store_id & address_id => 
 whole number
removed => picture column 
	
***********************	
store  => 
 change the type on  
 manager_staff_id & address_id => 
 whole number
****************************
dim_date => 
change all the dates columns to date to lose the time stamp 


********************************************************************************************************************************************

merge =>  film & film_category & category 

**********************************************************************
I choose the range for the column level_of_income 
low under 8000
medium up to 15000
and high 15000 to MAX 
I did not want the high-income level to be too dense 
**********************************************************************
merge
 dim_film & 
dim_customr &
fact_rental 
complete b, c, d, e, f, g.
need to finish task 1 merge the stuff and the store tables 
I deleted the merge in fact_rental need to fix it 

**********************************************************************
Created the star model and finished the 1 ' 2 '3 ' 4 sections 
section 5: A
 I added a 
rental_hour & return_hour columns 
rental_return_days_diff calc the days between rental and return dates 
didn't have an idea for another one or something better  
**** 
5: B
created a calculate column with prefix OR and 000 
