---
title: "Performing Calculations in Tableau"
time: 0

objectives:
- "How to perform calculations in tableau"
---

Sometimes, the data lacks some fields that are necessary for analysis. In that case, we can createa new field(column)by performing desired calculations. Those fields are called calculated fields.The calculated field could be a row level calculated field or a column level calculated field.This new calculated field created is saved to the data source. 

The 3 broad categories of calculations include 
– Basic Calculations
- Level of Detail (LOD) expressions
- Table Calculations

- a.Basic Calculations
Basic calculations can further be divided into Row-level calculations and aggregate calculations.

1.Row level Calculations –When we apply row level calculation, results are generated for every line in the datasource.

Let us see few examples –Transform/Split –Using split we can split strings and perform string manipulation. Click on customer name, transform, and split. This will split the customer’s name in two fields (first name, last name).

<img width="483" alt="Screen Shot 2022-03-19 at 6 56 20 PM" src="https://user-images.githubusercontent.com/47697537/159142359-5b8e8a16-f0dc-475b-beb9-410156b214dd.png">

<img width="599" alt="Screen Shot 2022-03-19 at 6 56 38 PM" src="https://user-images.githubusercontent.com/47697537/159142365-170ac92c-3f76-406f-a360-28a19e51b3ba.png">

We can also splitthe string based on a delimiter/separator.Let us split the order id column to obtain only the numbers in the id.

<img width="501" alt="Screen Shot 2022-03-19 at 6 57 08 PM" src="https://user-images.githubusercontent.com/47697537/159142377-7b7536ba-2c51-45b4-ad37-d6ead6ac1613.png">

The column has a delimiter ‘-‘  in the format. We specify that as the delimiter. Next, we want all the numbers in the id which are at the end of the string. We  select split off lastoption.A new calculated field has been created with the number string of the order id for each row in the data source.

<img width="629" alt="Screen Shot 2022-03-19 at 6 57 46 PM" src="https://user-images.githubusercontent.com/47697537/159142388-d67d0855-663a-461e-8046-59efd47f4cd6.png">

Finding strings/pattern -We can also spot substring or strings in the column. We will try to see product ids string that contains “TA” in it. Create a new calculated fieldwhich mentions the keyword contains. This will search for all the rows containing TA as a part of the string and returns a true value for them.

<img width="691" alt="Screen Shot 2022-03-19 at 6 58 17 PM" src="https://user-images.githubusercontent.com/47697537/159142403-b1adad08-526f-40ec-87db-d2bb9a7ed76a.png">


<img width="621" alt="Screen Shot 2022-03-19 at 6 58 46 PM" src="https://user-images.githubusercontent.com/47697537/159142417-da0f7a46-0969-46f2-818e-f8a7c4442fb9.png">

If/Else Conditional Calculation –Let us create a calculated field to see if the sales are profitable or not. 

<img width="674" alt="Screen Shot 2022-03-19 at 6 59 19 PM" src="https://user-images.githubusercontent.com/47697537/159142427-ba75c901-7638-4193-9e4f-b66b43589416.png">

<img width="629" alt="Screen Shot 2022-03-19 at 6 57 46 PM" src="https://user-images.githubusercontent.com/47697537/159142388-d67d0855-663a-461e-8046-59efd47f4cd6.png">

We add order id to the row shelf and profits to text marks card. Next, we add the calculated field created to the row shelf. The output is as shown.

<img width="621" alt="Screen Shot 2022-03-19 at 6 59 43 PM" src="https://user-images.githubusercontent.com/47697537/159142441-adb0a639-b644-471f-8ecc-14d1e6f9a28a.png">

<img width="629" alt="Screen Shot 2022-03-19 at 6 57 46 PM" src="https://user-images.githubusercontent.com/47697537/159142388-d67d0855-663a-461e-8046-59efd47f4cd6.png">

- 2.Aggregate calculations

– Generally, adding any measure to row or column shelf aggregates the measure. But we can create calculated field and perform aggregation on the rows in the data source.Let’s count the number of customers. This aggregation will give the count of customers against the dimension we choose in the visualization. Let us add region to the row shelf, profits,and the calculated field (Count_Customer) to the column shelf.

<img width="700" alt="Screen Shot 2022-03-19 at 7 00 38 PM" src="https://user-images.githubusercontent.com/47697537/159142461-4e4b8bb6-8532-46f5-8b47-40f7babcf2ed.png">

The visualization gives the profits across region and count of customers for each region.

<img width="700" alt="Screen Shot 2022-03-19 at 7 01 11 PM" src="https://user-images.githubusercontent.com/47697537/159142469-9b890154-988f-444a-a1b8-0c5e94ca700a.png">




