## Lab - Create a Basic Journey in Adobe Journey Optimizer

In this exercise, you will create a Basic Journey in Adobe Journey Optimizer.

1.  Navigate to Journeys
2.  Click on “Create Journey”
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_1.png)

3.  Provide a Name and Description
4.  Unclick “Allow Re-Entrance”
5.  Click Ok.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_2.png)

6.  To start the Journey, drag the “Read Segment” Orchestration Node onto the Canvas.
7.  The Canvas is in the middle of the screen.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_3.png)

8.  Click on the Label of the Read Segment.  Change the label to “Silver Loyalty Members”.
9.  Click on the pencil in the Segment.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_4.png)

10.  From the Choose Segment applet, select “Silver Loyalty Members”.
11.  Click Save.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_5.png)

12.  Drag the “Condition” Orchestration Node after the Read Segment.
13.  Give it a Name of “Female Customers”.
14.  The type should be “Data Source Condition”
15.  Click on “Add a Path”, so there are two paths visible.
16.  For the First Path, select Female Customers as the Condition.  Add a name “Female Customers”
17.  For the Second Path, select “NOT” Female Customers as the Condition.
18.  Click OK.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_6.png)

19.  Drag the Message Action onto the Canvas on Path 1.
20.  Drag the End Node onto the Canvas on Path 2.
21.  For the Message Action, give it a name 10% Off Email.
22.  Click on the “Select a Message”
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_7.png)

23.  Click on the “10% Off Coupon” Message.
24.  Click Select.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_8.png)

25.  Click Ok.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_9.png)

26.  Add an End Node to the end of the Journey.
27.  Give it a Label of “End of Journey”.
28.  Click OK.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_10.png)

29.  END OF LAB
