---
title: "Relationships in Tableau"
time: 0

objectives:
- "How to build relationships in tableau"
---

- Tableau allows combining more than one table from the dataset. There are two ways in which we can accomplish this –joining the tables or establishing relationship between the tables.Establishing a relationship is more flexible as compared to joins is because you do notneed the specify the join type. Tableau creates a relationship based on matching column names or existing key constraints. It adjusts the join and preserves the LOD (level of detail) of the data. Relationships are dynamic, tables are not merged at data source level but are joined automatically, based on fields in use. The difference between joins and relationship is that –when you create a relationship, the tables are combined at the logical layer whereas when you create a join tables are combined at the physical level. Hence relationships are flexible,and joins are static.

<img width="709" alt="Screen Shot 2022-03-19 at 5 40 39 PM" src="https://user-images.githubusercontent.com/47697537/159140885-c1ae412a-68c5-4497-ba56-e85be4bc2b8d.png">

- Let us start building relationships.Start by importing data in Tableau. The Data Source page will have all the tables from the uploaded dataset.

<img width="719" alt="Screen Shot 2022-03-19 at 5 41 24 PM" src="https://user-images.githubusercontent.com/47697537/159140895-6570c101-9ac2-4bf8-8aba-05bc754ab877.png">

- Now drag the first table that you require on the canvasand you will see all the rows and columns populated.Drag the second table and you can see a connection between the two tables. You have now established a relationship between two tables.

<img width="760" alt="Screen Shot 2022-03-19 at 5 42 03 PM" src="https://user-images.githubusercontent.com/47697537/159140919-6aaf4728-eb88-4260-936f-957e123ce5f4.png">

- The relationship is created by connecting common columns from both the tables. You can add more fields/columns you want to connect.The performance options include selecting cardinalityand referential integrity. If you are unsure about any of the parameters,you can stick to the defaults.

<img width="555" alt="Screen Shot 2022-03-19 at 5 42 59 PM" src="https://user-images.githubusercontent.com/47697537/159140935-3765ffe0-4e7c-4ad2-9373-d90f85f4b6f7.png">

<img width="502" alt="Screen Shot 2022-03-19 at 5 43 30 PM" src="https://user-images.githubusercontent.com/47697537/159140941-4623c555-6572-4a2e-9fc8-76a95cf08fee.png">

- You can establish relation between multiple tables.

<img width="526" alt="Screen Shot 2022-03-19 at 5 43 58 PM" src="https://user-images.githubusercontent.com/47697537/159140949-135e0f01-c0da-4b6e-ae98-a67c847a9acb.png">

- Suppose you have two tables, employee table with employee_id as the primary key, employee_names, employee_address and employee_hiredate and department table with department_id, department_name and worker_id.Now in these two tables, employee_id and worker_id columns are the same, but they have different column name. In that case, you will have to choose the columns you want to join on. That is,you will have to select employee_id and worker_id to establish the connection.

- Now, let us say you want to create a join rather than a relationship. In that case double click on the orders table. This will give you access to the physical layer. Now drag the table you want to join.

<img width="526" alt="Screen Shot 2022-03-19 at 5 45 28 PM" src="https://user-images.githubusercontent.com/47697537/159140967-3f4cb2b5-ee93-47f0-b0f9-76190aad5cf3.png">

- To change the type of join, click on the join icon (venn diagram) and you will have all the join options. 

<img width="565" alt="Screen Shot 2022-03-19 at 5 46 33 PM" src="https://user-images.githubusercontent.com/47697537/159140994-eac30cc9-be36-439a-8228-567ec4a2012a.png">

- Let us look at all the measures and dimensions populated after we have established the relationship.We can see that the measures and dimensions have been split up table-wise.

<img width="555" alt="Screen Shot 2022-03-19 at 5 47 17 PM" src="https://user-images.githubusercontent.com/47697537/159141009-9d3ae77c-43d7-4f0b-acbd-c8193e9ecd39.png">

- Whereas if we perform join, we can see all the dimensions from both the tables and all the dimensions from both the tables.

<img width="445" alt="Screen Shot 2022-03-19 at 5 47 49 PM" src="https://user-images.githubusercontent.com/47697537/159141022-5a2f7622-97d9-4d29-ad94-b60302b611db.png">





