## Lab - Create a Complex Journey in Adobe Journey Optimizer

In this exercise, you will create a multi steps real time Journey in Adobe Journey Optimizer.
We want to Send investment offer to customer who just made a large deposit on their account 

After completing this exercise, Your jounrey should like that:
![Complex Journey](../0.%20Images/Journey2_final.JPG)

2.  Navigate to Journeys
3.  Click on “Create Journey”
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_2.png)

4.  Provide a Name and Description : Purchase Journey - XX, replace XX by your attendee number. Ex: Purchase Journey - 01

5.  Check “Allow Re-Entrance” as we want each customer to restart this journey each time he make a purchase. 

6.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_3.PNG)

7.  First step to design our journey is to select when a customer will enter this journey. Here we want to trigger the journey as soon as we receive a "purchase" from our web site. On the left pannel, expend "Events", drag and drop the "LumaPurchase" event. 

![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey2_step0.JPG)

8.  Add a Description.
9.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_4.PNG)

10.  Expend the "Action" menu on the left, then select message. 
11.  Drag it onto the Canvas after the Purchase Event.
12.  Add a Label and Description:  “Thanks for Your Order”
13.  Click on “Select a Message”.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_5.PNG)

14.  Click on the “Thank You Email” Message. This message has been prepared for you and contains personalisation based on purchase. 
15.  Click Select.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_6.PNG)

16.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_7.PNG)

17.  Click on Orchestration on the left menu and select "wait"
18.  Drag it onto the Canvas after the Message.
19.  Set Type as Duration and Amount of Time to 2 minutes. In reality we will use something like 7 days but for the demo we don't want to wait. 
20.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_8.PNG)

21. After 7 days, we want to send an email asking to post a product review. Go to "action", select message and drag and drop it in the canvas after the wait. 

22. Select "rate your product" message
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey2_message2.JPG)

23.  Click on "Events" menu on the left
24.  Drag and drop the "segment qualification" after the wait.
Here we want to continue the jounrey only if and when our customer post a review. For this we will use the segment created previously "Product Review fulfilled"
25.  Select the segment you have previously created "product review fulfilled - XX"
26.  Let "behaviour" as "enter, define a timeout to 7 days. We can eventually add a path for timeout if you want to send a reminder.
By doing so, the profile will go to next step as soon as he posts a review, and if he doesn't after 7 days the jounrey will end for him.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey2_condition.JPG)

27. Finally we want to send the coupon, then end the jounrey. Drag and drop another message, then select "Luma coupon email"
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey2_message3.JPG)

28. Add an "end" activity after your message

29. Your journey is now ready. We can now test it. Enable your journey for testing. 
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey2_proof1.JPG)

30. We can trigger a journey manually, but it would be complex to provide all product informations. So let's use our web site. 
Go to our web site. Ensure you are loged in. If not, login with email address of your test profile.
It should be something like hol2_uXX@gmail.svpoc.io. Replace XX by your attendee number. If you work on another sandbox than hol2, replace it as well by your sandbox number. ex : hol1_u01@gmail.svpoc.io

31. Browse a product, click on add to cart
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey2_addToCart.JPG)

31. proceed to check out
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey2_checkout0.JPG)
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey2_checkout.JPG)

32. Provide soem random value fo shipping address, then checkout. 

33. Your purchase has been completed! Journey Optimiser will detect it, and trigger the jounrey if your profile is a "test profile" 

34.  END OF LAB.
