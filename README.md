# Shopify-Fall-2022-Data-Science-Intern-Challenge
Jenny Li         
Email: zl3071@columbia.edu

## Question1: Sneaker Shop AOV
### a.Think about what could be going wrong with our calculation. Think about a better way to evaluate this data. 
AOV: average order value, mean value of the data 'order_amount'. It represents the average cost of the sneaker orders.      
The unreasonably high AOV is due to some outliers up to 70,000 dollars.       
A better way to evaluate this dataset is to divide the dataset and analyze them seperately.

### bc. What metric would you report for this dataset? What's the value?
**Metrics: Mean, Standard Deviation, and Median.**      
* Firstly, the mean value is $3145, which is too high to represent the true industry.        
* Then I noticed the Standard Deviation is 41282, almost 13 times of the mean value. It means the data is every skew and there are some outliers.       
* After seperating the data into two datasets with IQR*100, I analyze two datasets seperately.  
![](/output/q1.png)  
#### (1) Small orders
After deleting the "outliers", the AOV is **302** dollars and average item number of each order is **1.99**.         
**Now it makes sense!** Most of time, customers buy 2 pairs of sneakers and pay 300 dollars for one order.
#### (2) Large orders - "outliers"
With IQR*100, there are **63** data points with value higher than $10000 that are considered as outliers.
Some of them are large order with 2000 items and the total amount added up to $70,000.        
Some are expensive purchase in the shop No.78, where one item costs 25725.
#### Median overall
To evaluate the data with outliers, I can also use median, which represents the average of the data as well.
The median of this data is $284, also makes sense to represent the average purchase level.

## Question2: SQL
See the PDF of the code.
### a. How many orders were shipped by Speedy Express in total?
![](/output/q2.1.png)

### b. How many orders were shipped by Speedy Express in total?
![](/output/q2.2.png)

### c. What is the last name of the employee with the most orders?
![](/output/q2.3.png)
