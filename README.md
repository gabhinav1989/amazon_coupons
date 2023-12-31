# Amazon_coupons - Python Course AI Analysis

## Problem statement from module 5(Verbatim)

### Overview

In this first practical application assignment of the program, you will seek to answer the question, “Will a customer accept the coupon?” The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not. Use the Practical Application 1 Jupyter Notebook Links to an external site.to complete this assignment.

### Data

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, passenger, etc., and then asks people whether they will accept the coupon if they are the driver. Answers given that the users will drive there “right away” or “later before the coupon expires” are labeled as “Y = 1”, and answers “no, I do not want the coupon” are labeled as “Y = 0”. There are five different types of coupons—less expensive restaurants (under $20), coffee houses, carry out and take away, bars, and more expensive restaurants ($20–$50).

### Deliverables

Your final product should be a brief report that highlights the differences between customers who did and did not accept the coupons. To explore the data, you will utilize your knowledge of plotting, statistical summaries, and visualization using Python. You will publish your findings in a public facing GitHub repository as your first portfolio piece.

## My Solution

The analysis below will try to answer the question: "Will a customer accept the coupon?"

I implemented the concepts learned so far in the course such as visualizations, probability distributions etc. to differentiate the customers who accepted the coupons while driving and those who didn't accept the coupons.

### Data used for solution

The data used for the analysis is exactly the same as what is provided. A few changes I made to the data are: 
I changed the age column to a numeric column using asType. using the below code. 

`condition1 = data['age']=='50plus'
condition2 = data['age']=='below21'
data.loc[condition1, 'age'] = 50
data.loc[condition2, 'age'] = 20
data['age'] = data['age'].astype(int)`

The coupons in the data set are categorized as shown below: 
![img.png](img.png)

Some plots of users who accepted the coupons by different categories are as follows
1. By Marital Status and Age: 
![img_1.png](img_1.png)

2. By Category and destination

![img_2.png](img_2.png)

3. By Education

![img_3.png](img_3.png)

4. By frequency of how often they go to bar.

![img_4.png](img_4.png)

### More analysis on Bar coupons itself.
1. Drivers 25 and above that go more than once
 ![img_5.png](img_5.png)
2. Drivers without kid passengers and not in specified occupations.
![img_6.png](img_6.png)
3. Drivers without kid passengers and not widowers
![img_7.png](img_7.png)
4. Drivers aged less than 30 and who go often
![img_8.png](img_8.png)
5. Lastly, Drivers with specific income category and who often go to low income restaurants.
![img_9.png](img_9.png)

### Observations:

- I observed that the bar coupons are mostly accepted by those who are less frequently visiting the bar compared to those who are visiting the bar more frequently.
- Also, drivers with lower income and whose chose less expensive restaurants didn't appear to be interested in coupons compared to all others who did.

### Next Steps: 
This data is sufficient to preform modeling as next steps.
