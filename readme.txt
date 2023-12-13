Welcome to Driveby Coupn accpetance analytics


How to load the project ?

Project contains of the following:

- Checkout the entire folder
- Run Jupyter on prompt.ipynb
- Load the data 
- Run each section as you go through the file.
- At any point, you can either update the exisitng or add new sections to try other comparisons
- Required files:
---- prompt.ipynb
---- data/coupons.csv
- Jupyter File Location:
- https://github.com/hubgmail12/berkeley/blob/main/prompt.ipynb


Will a Customer / Driver  Accept the Coupon?


Overview

The goal of this project is to use the techniques learnt in the first 5 Modules of the course to dtermine if there is any relationship between the data collected and customer coupon acceptanace. 

Where is the Data come from?

This data comes from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. 

How the Data is presented?

Data has column 'Y' If the driver accepted the coupon, the value for Y is 1, and if they did not accept the answer is no and presented with 0.

Coupon types is recieved by driver based on the driver's proximately , they can recieve either of these coupon types on their phones:

df['coupon'].unique()
array(['Restaurant(<20)', 'Coffee House', 'Carry out & Take away', 'Bar',
       'Restaurant(20-50)'], dtype=object)


How do we go about this?

1 - As any other project, load the data, check variety of the head, tail or middle of the datset, and just visually inspect, although this may not be a lot of help, you at least have a data in your mind.

2- determine how your good your dataset is for what you want to do. You also may determine that you may not need some data.

3. I suggest runing df.info() so you can see data types

4. What I find useful, is just to quickly using panda fucntions and look for nulls, I also find it very useful to search for data that has different charctersets such as letters and numbers,... using string searches

5. In this case, in this project, you can find how I used different methods to create a new column using fiter, fix existing columns and change the type to integer

6. Once I do the first set of cleanup , I typically create a copy of the original dataFrame. You really do not need to do this, but there were a couple of times that I dropped columns or changed the data in a way that it was not reversible and I had to start from beginning. so this is just for me, so after cleaning the data that I thoguht I would use in the project, then i copied and used the copy going forward.

7. my data cleaning included, creating a new column for income range and used lower income to create the column so I can search on, ..

8. I also changed the ag column. I changed the string 50 plus to 50 and lower then 21 to 20. This allows me to do better searches and easier.

9. in addition I did additional clean up of another clumns and dropped another column which had no use

10, I also merged 2 columns since the data could be stored in the single column, I have the details in the file with proper comments so it can be followed.

11. I also find it very useful to have comments and also ensuring your print statements are clear, so anyone knows what you were trying to do.



My evaluation based on the project:

Bar:
- Bar Coupons acceptance has been more common among younger crowd
- Also out of those, those who went to bar less, seems to have accepted the bar coupon more.
- More males than feamles accepted the coupon
- Having kids or occupation, did not seem to have an impact on acceptance

#Coffe House:
#- Income range, you can see the lower income range accepted the coffee coupon more
#- Similar to the Bar, younger crowd seems to have accepted the coupon more.
#- Similar to Bar, those who went to the coffee shop more often did not accept as many as those who went less
#- One interseting thing was the education that surprised me was education, but after comparing ratio, it seems like those with some high shool, they actually accept almost 50% more eventhough their population size is small


You have the opportunity to examine this, or continue using other categories and other experiements.

-Enjoy



