---
title: "Building advanced charts in Tableau"
time: 0

objectives:
- "How to develop advanced charts in tableau"
---

- Lollipop Chart – Let us start by adding sub-category to column shelf and sales to the row shelftwice.Select dual axis.
<img width="398" alt="Screen Shot 2022-03-21 at 6 39 38 PM" src="https://user-images.githubusercontent.com/47697537/159380372-6a98d613-4f4b-43da-a5ff-260ef524c990.png">

You will get a chart like this.

<img width="379" alt="Screen Shot 2022-03-21 at 6 40 08 PM" src="https://user-images.githubusercontent.com/47697537/159380427-cb2652fe-7562-42c5-9974-8eea4591691f.png">

Next, select bar chart from the marks card sum of sales.

<img width="431" alt="Screen Shot 2022-03-21 at 6 40 33 PM" src="https://user-images.githubusercontent.com/47697537/159380471-27b6fe42-3365-4f3e-ab01-496fd29ace4c.png">

Adjust the size of the bar as follows.

<img width="476" alt="Screen Shot 2022-03-21 at 6 41 01 PM" src="https://user-images.githubusercontent.com/47697537/159380502-7fae22e9-85e0-410b-8ac6-a421d4c9fd12.png">

<img width="461" alt="Screen Shot 2022-03-21 at 6 41 15 PM" src="https://user-images.githubusercontent.com/47697537/159380535-ea5b7de1-cd2b-4eab-9bff-6375253ce972.png">

Similarly, you can adjust the size of the bubble. To add labels to the visualization, click on marks card and select show marks label.

<img width="457" alt="Screen Shot 2022-03-21 at 6 41 40 PM" src="https://user-images.githubusercontent.com/47697537/159380571-c2aafa6a-89f2-4c96-9292-a0c5094946af.png">

To categorize it according to the category, add category from the dimensions to colors marks cardfor the sum of sales.

<img width="463" alt="Screen Shot 2022-03-21 at 6 42 07 PM" src="https://user-images.githubusercontent.com/47697537/159380611-bd4f9f46-3ba9-4f1d-a119-39dda84c4165.png">

- Word Cloud – Add sub-category to text marks cardand profits to size marks card.

<img width="430" alt="Screen Shot 2022-03-21 at 6 42 52 PM" src="https://user-images.githubusercontent.com/47697537/159380664-d625bbe6-5cc6-4941-a4a0-12506eaa247c.png">

<img width="474" alt="Screen Shot 2022-03-21 at 6 43 09 PM" src="https://user-images.githubusercontent.com/47697537/159380688-ac07a255-6712-4a15-bbf2-3b070552041f.png">

Add category to colors marks card.

<img width="427" alt="Screen Shot 2022-03-21 at 6 43 40 PM" src="https://user-images.githubusercontent.com/47697537/159380720-7a525ac4-2bce-44ac-9456-0483a2848be1.png">

- Donut Chart – Start by selecting pie in the marks cardand ship mode to color.Addsales to angle. The chart now shows the ship mode by sales.Fit the chart in entire view.

<img width="420" alt="Screen Shot 2022-03-21 at 6 44 16 PM" src="https://user-images.githubusercontent.com/47697537/159380767-db5d4011-e4f9-4a23-906a-8a5fca3a0054.png">

<img width="490" alt="Screen Shot 2022-03-21 at 6 44 33 PM" src="https://user-images.githubusercontent.com/47697537/159380790-952ae610-a30c-4c0e-81ca-bb37ea5f961d.png">

To create a donut chart,we now need to duplicate thepie chart. To do so double click on column shelf and type in 1. This will create a fake axis. Change the aggregation to minimum. And create a duplicate of the fake axis by pressing control and dragging the axis in column shelf again.

<img width="486" alt="Screen Shot 2022-03-21 at 6 45 06 PM" src="https://user-images.githubusercontent.com/47697537/159380854-f046c30c-f806-47f5-bf45-1a9f6acfdbca.png">

Increase the size of the pie chart through the size marks card. Remove ship mode from the color in the second min(1) marks card.

<img width="476" alt="Screen Shot 2022-03-21 at 6 45 35 PM" src="https://user-images.githubusercontent.com/47697537/159380891-d2a723df-f551-42b2-b2e7-2edc9ec3c433.png">

Decrease the size of the pie and change the axis to dual axis in the column shelf.

<img width="475" alt="Screen Shot 2022-03-21 at 6 46 11 PM" src="https://user-images.githubusercontent.com/47697537/159380936-56b6bf0f-0d92-4a28-a359-0d227c662824.png">

Next step is to synchronize both the axis and remove the header(uncheck the show header option).

<img width="462" alt="Screen Shot 2022-03-21 at 6 46 37 PM" src="https://user-images.githubusercontent.com/47697537/159380962-6460545d-0d49-4ea7-87dc-61c4cd05f25e.png">

Change the color of the center part as whiteand add sales to the label marks card.

<img width="451" alt="Screen Shot 2022-03-21 at 6 47 04 PM" src="https://user-images.githubusercontent.com/47697537/159381003-983626ac-23a8-456a-88f2-b338871f678e.png">

Now if we add region to the column shelf, we will have multiple donut chart.

<img width="471" alt="Screen Shot 2022-03-21 at 6 47 32 PM" src="https://user-images.githubusercontent.com/47697537/159381035-c290b90b-c4f6-491d-bc7b-9355a919e6bc.png">

- Waterfall Chart – Start by creating a calculated field which has negative profit values in it.

<img width="459" alt="Screen Shot 2022-03-21 at 6 48 02 PM" src="https://user-images.githubusercontent.com/47697537/159381074-4a227a54-afd1-403a-88bf-910a25c3d1ce.png">

Add sub-category to columnshelf, profits to row shelfand negative profits (calculated field) to the size marks card.

<img width="468" alt="Screen Shot 2022-03-21 at 6 48 29 PM" src="https://user-images.githubusercontent.com/47697537/159381115-ba3d5100-8337-4613-911e-46b9d8e6ae10.png">

From sum of profits in the rows column select running total from the quick table calculations.

<img width="480" alt="Screen Shot 2022-03-21 at 6 49 00 PM" src="https://user-images.githubusercontent.com/47697537/159381158-7464410f-3ebd-42af-ab5d-bbd0c363fd90.png">

Select Gantt Bar from the marks card.

<img width="499" alt="Screen Shot 2022-03-21 at 7 35 34 PM" src="https://user-images.githubusercontent.com/47697537/159384868-82b2aeff-c8cd-4564-a74f-38fa22f41431.png">

- Funnel Chart – Start by adding sub-category to rows shelf and sales to column.Arrange the output in descending order. Duplicate the sales in column shelf.

<img width="473" alt="Screen Shot 2022-03-21 at 7 36 48 PM" src="https://user-images.githubusercontent.com/47697537/159384959-5b8c16de-c25f-474a-a3be-889de3e8598e.png">

Click on edit axis on the first chart and select scale as reverse.

<img width="285" alt="Screen Shot 2022-03-21 at 7 37 26 PM" src="https://user-images.githubusercontent.com/47697537/159385019-c3f61759-4b06-4f11-9348-c971eb9d604c.png">

<img width="486" alt="Screen Shot 2022-03-21 at 7 37 46 PM" src="https://user-images.githubusercontent.com/47697537/159385044-9a69cf9e-3568-4d10-972e-54061aaa1ada.png">

This gives us a funnel chart.





