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

- Basic Calculations - Basic calculations can further be divided into Row-level calculations and aggregate calculations.

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

- Aggregate calculations

- Generally, adding any measure to row or column shelf aggregates the measure. But we can create calculated field and perform aggregation on the rows in the data source.Let’s count the number of customers. This aggregation will give the count of customers against the dimension we choose in the visualization. Let us add region to the row shelf, profits,and the calculated field (Count_Customer) to the column shelf.

<img width="700" alt="Screen Shot 2022-03-19 at 7 00 38 PM" src="https://user-images.githubusercontent.com/47697537/159142461-4e4b8bb6-8532-46f5-8b47-40f7babcf2ed.png">

The visualization gives the profits across region and count of customers for each region.

<img width="700" alt="Screen Shot 2022-03-19 at 7 01 11 PM" src="https://user-images.githubusercontent.com/47697537/159142469-9b890154-988f-444a-a1b8-0c5e94ca700a.png">


- Level of Detail expression

Allows calculations at data source as well as visualization level(just like basic calculations). But provides more control over the level of granularity. The level of detail could be high-level details (less granularity, summary, more aggregated) or low-level details (more granularity, more details, less aggregated). To understand the how the high-level/low-level details work, let us take an example-

- Drag the sales to the text marks card.We can see the sumof sales of all the products. This has less granularity and more aggregation. This gives the high-level picture of sales for the orders table.

<img width="504" alt="Screen Shot 2022-03-21 at 6 15 44 PM" src="https://user-images.githubusercontent.com/47697537/159378209-d51e87ac-1585-4507-898f-a11c2be4e743.png">

- Add region to the row column shelf. This adds a level of details because now we are viewing the sum of sales across the 4regions.This has added a little more granularity and little less aggregation as compared to the first step.

<img width="614" alt="Screen Shot 2022-03-21 at 6 17 39 PM" src="https://user-images.githubusercontent.com/47697537/159378450-e7c8ab12-96ac-429f-b3ec-907a618280ab.png">

- Add states to the row shelf. This is a more granular visualization as compared to step 2. So, we started from a high-level visualization in step 1 and kept adding more details to reach to a low-level detail visualization.

<img width="535" alt="Screen Shot 2022-03-21 at 6 18 54 PM" src="https://user-images.githubusercontent.com/47697537/159378514-2d887ac7-f692-4905-ad1a-841f5e8a597f.png">

There are 3 types of LOD expressions:
- Fixed 
- Exclude
- Include

Fixed expression is independent of view. When we use exclude expression, it is like removing some dimensions from the view. When we use include expression, it is like adding dimensions to the view. 
Syntax –{Type of expression [Dimension list] : Aggregate}
- 1. Fixed –It returns a scalar value. It is independent of the dimensions in the view. Let us create a fixed expression field. Start by adding sum of sales to the text marks card. 

<img width="497" alt="Screen Shot 2022-03-21 at 6 20 29 PM" src="https://user-images.githubusercontent.com/47697537/159378664-55981cba-243c-4079-b60c-33e372c4306c.png">

Next, create a calculated field with the fixed expression for sum of sales.

<img width="444" alt="Screen Shot 2022-03-21 at 6 20 59 PM" src="https://user-images.githubusercontent.com/47697537/159378729-c4e4c316-da25-4db2-8acc-2bc301be8fc5.png">

<img width="644" alt="Screen Shot 2022-03-21 at 6 21 33 PM" src="https://user-images.githubusercontent.com/47697537/159378773-506558f5-15f7-434c-8385-d1d91e43a29b.png">

We created a grand total field in the measures. Double click on the fieldfrom the measures.

<img width="555" alt="Screen Shot 2022-03-21 at 6 22 26 PM" src="https://user-images.githubusercontent.com/47697537/159378854-fdea7457-2ab7-4b9d-986e-907ed6c808c1.png">

This gives us the grand total and sales. Move the measure names from rows shelf to column and add region to rows shelf.

<img width="514" alt="Screen Shot 2022-03-21 at 6 22 53 PM" src="https://user-images.githubusercontent.com/47697537/159378889-05d63f79-52d0-4d11-b847-80b27a67fcdc.png">

Here we are viewing sales across all the regions. Now remove region and add category from the dimensions. We can see that the grand total is the same irrespective of the whatever dimension we add to the row shelf. The fixed grand total value is independentof the dimensionsas the calculation does not contain any dimension. Let us try and add filter on the region. We can see that, even if we unselect some of the regions the grand total is unaffected.

<img width="795" alt="Screen Shot 2022-03-21 at 6 23 38 PM" src="https://user-images.githubusercontent.com/47697537/159378947-cb9bb3b0-ce5e-4d77-847f-4a19167f0878.png">

Exclude LOD –This type of calculation is sensitive to dimensions. Exclude does not return a scalar value (unlike fixed LOD), it returns an aggregated value.It gives dimension in the view minus what is in the expression.Let’s create some visualization using exclude calculation.

<img width="534" alt="Screen Shot 2022-03-21 at 6 24 12 PM" src="https://user-images.githubusercontent.com/47697537/159378995-83fbaf30-7ddd-4e06-bd0d-55a0607ad6ac.png">

In the above visualization, we exclude region, so now if we add region to the filter, the grand total will change when we select/unselect some regions.

<img width="696" alt="Screen Shot 2022-03-21 at 6 24 46 PM" src="https://user-images.githubusercontent.com/47697537/159379032-8d63b3a7-9d6c-44ee-a816-e90b6ad53bd3.png">

Let us add another dimension to the row shelf and observe the values. The exclude calculations values are now changed. Adding another dimension has affected the calculation values. We can add more than one dimension in the exclude LOD calculation. Edit the exclude calculation and add category and sub-category to the exclude calculation. Remove region.

<img width="323" alt="Screen Shot 2022-03-21 at 6 25 35 PM" src="https://user-images.githubusercontent.com/47697537/159379108-3fccdd37-a43c-4ea1-ab31-948647cd05f5.png">

IncludeLOD –These calculations will include dimensions in the view and the dimension mentioned in the include expression.The results are aggregated.Let uscreate a table calculation to understand the topic.We create the calculated fieldas follows. We are including sub-category in it.

<img width="411" alt="Screen Shot 2022-03-21 at 6 26 25 PM" src="https://user-images.githubusercontent.com/47697537/159379200-c70968d4-523e-41cc-bf90-edc80909e265.png">

Now add the calculated fieldthat we created. 

<img width="412" alt="Screen Shot 2022-03-21 at 6 27 10 PM" src="https://user-images.githubusercontent.com/47697537/159379274-77b81db5-6b37-43ff-9f77-854ddd1f0604.png">

Now the visualization shows maximum of sum of sales as the total for each category. Now we remove sub-category from the row shelf.

<img width="393" alt="Screen Shot 2022-03-21 at 6 27 58 PM" src="https://user-images.githubusercontent.com/47697537/159379337-393712c1-dd70-44e6-b099-2dad05f24ccf.png">

So now we don’t have sub-category in the visualization but since it is a part of the calculated field, we still have the max sum of sales of the sub-category for every category.

- Table Calculations
Table calculations are the transformation that you apply to the values in the visualization. They are calculated based on what is present in the visualization.So, basically when we create a visualizationand then add the table calculation. They are added on top of the aggregated function used in visualization.
Three things that will affect the table calculations are 
– Layout
- Direction/ addressing
- Scope/ partitioning
Let us start with creating a visualization to understand it better. Add Region to the row shelf and order date to the column shelf. Add sum of sales to the text marks card.Click on totals in the analytics tab to get the grand total.

<img width="392" alt="Screen Shot 2022-03-21 at 6 33 10 PM" src="https://user-images.githubusercontent.com/47697537/159379800-0de2f3ed-9052-4885-ad20-59d8d3203016.png">

Now when we click on sum of sales, we can see a quick table calculation option. And we have all the commonly used table calculations like running total, percent total etc. So,we are applying aggregation/calculationto the already existing aggregation in the visualization. Select percent of total from the options.

<img width="379" alt="Screen Shot 2022-03-21 at 6 33 49 PM" src="https://user-images.githubusercontent.com/47697537/159379850-86758355-bd37-4724-b7d9-4df5e881afa6.png">

<img width="413" alt="Screen Shot 2022-03-21 at 6 34 06 PM" src="https://user-images.githubusercontent.com/47697537/159379897-ba34ecd2-dc8f-4c1c-ba3f-0d5832b41f9a.png">

After applying percent of total, the original values in the table are changed to the percent values. Now let us see how the three aspects of table calculation –layout, direction and scope affect the calculation.

Table calculations are sensitive to the layout of the visualization. If we add another dimension let us say sub-category to row shelf and try and move the region dimension from row to column shelf, we see that the values in the tables change.Next, we can see that the percent of total is being calculated from left to right. 

That means the calculation is sensitive to the direction of consideration.We can have the calculation from left to right or from top to bottom. To change the direction, we can select an option as follows.We can also see options like cell, order date and region which gives us the scope/partition for the calculation.

<img width="355" alt="Screen Shot 2022-03-21 at 6 35 02 PM" src="https://user-images.githubusercontent.com/47697537/159379954-b3828899-722e-4bd5-9768-ef932a782413.png">


































