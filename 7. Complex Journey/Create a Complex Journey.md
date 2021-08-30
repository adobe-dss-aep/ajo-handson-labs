## Lab - Create a Complex Journey in Adobe Journey Optimizer

In this exercise, you will create a Complex Journey in Adobe Journey Optimizer.

1.  After completing this exercise, you will create the following Journey in Adobe Journey Optimizer:
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_1.png)

2.  Navigate to Journeys
3.  Click on “Create Journey”
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_2.png)

4.  Provide a Name and Description
5.  Check “Allow Re-Entrance”
6.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_3.PNG)

7.  Change the Label to Read – “Customer Buys a Luma Item”
8.  Add a Description if you would like.
9.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_4.PNG)

10.  Click on the Message Action
11.  Drag it onto the Canvas after the Purchase Event.
12.  Add a Label and Description:  “Thanks for Your Order”
13.  Click on “Select a Message”.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_5.PNG)

14.  Click on the “Thank You Email” Message.
15.  Click Select.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_6.PNG)

16.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_7.PNG)

17.  Click on the Wait Orchestration
18.  Drag it onto the Canvas after the Message.
19.  Set Type as Duration and Amount of Time to 7 Days.
20.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_8.PNG)

21.  Click on Orchestration
22.  Add the “Condition” after the Wait Step.
23.  Click on “Add a Path” twice so that there are 3 paths total.
24.  Change the name of the Paths to “Men”, “Women” and “Other”.
25.  Click on Expression for “Men”
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_9.PNG)

26.  Click on Gender is Male.
27.  Click Ok.
28.  Click Ok.
29.  (NOTE:  Repeat for Female)
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_10.PNG)

30.  Click on Gender is Male / Gender is Female.  - and them both to the Canvas with an “AND” condition.
31.  Click Ok.
32.  Click Ok.
33.  (NOTE:  Repeat for Female)
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_11.PNG)

34.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_12.PNG)

35.  Add the Men’s Collection Email to the Men’s Path
36.  Add the Women’s Collection Email to the Women’s Path
37.  Add the Other’s Collection Email to the Other’s Path
38.  Click Ok
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_13.PNG)

39.  You Journey should now have all three email messages attached, as in the picture.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_14.PNG)

40.  Add a Reaction Event node to the Men’s Path;  Change the Label to “Opened Email”;  Click on Event and select “Email Opened”;
41.  Add a Reaction Event node to the Women’s Path;  Change the Label to “Opened Email”;  Click on Event and select “Email Opened”;
42.  Add an End Node to the Other’s Path
43.  Click Ok
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_15.PNG)

44.  Add a Wait step and combined the Men/Women’s paths;  Set the Wait for 7 Days;
45.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_16.PNG)

46.  Add a Message Action to the Canvas after the Wait step;  Select the “Special 15% Thank You” Message.
47.  Click OK
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_17.PNG)

48.  Add an End Node to your Journey.
49.  Click Publish.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_18.PNG)

50.  END OF LAB.
