## Lab - Create a Complex Journey in Adobe Journey Optimizer

In this exercise, you will create a multi steps real time Journey in Adobe Journey Optimizer.
We want to send investment offer to customer who just made a large deposit on their account 

After completing this exercise, Your jounrey should look like that:
![Complex Journey](../0.%20Images/Journey2_final.JPG)
The jounrey should be triggered as soon as we receive a deposit. If deposit is larger than 30k, we will inform relationship manager to contact customer. Othwerwise we will send investment offers, wait 2 weeks, and send a reminder if the money has not been invested. 
2.  Navigate to Journeys
3.  Click on “Create Journey”
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_2.png)

4.  Provide a Name and Description : Large Deposit - XX, replace XX by your attendee number. Ex: Large Deposit - 01

5.  Check “Allow Re-Entrance” as we want each customer to restart this journey each time he will make a deposit. 

6.  Click Ok.
![Complex Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/651011282df7ba12c4b26dd44547310d060ad276/0.%20Images/Complex_Journey_3.PNG)

7.  First step to design our journey is to select what will trigger this journey. Here we want to trigger the journey as soon as we receive a deposit. On the left pannel, expend "Events", drag and drop the "LargeDeposit" event. 

![Complex Journey](../0.%20Images/Journey2_step0.JPG)

8.  Expend the "Orchestration" menu on the left, then select condition.
9.  Drag it onto the Canvas after the Deposit Event.
10.  Change the Label to “Check deposit amount”, change the name of the path to "greater than 100k", then click on edit expression button

![Complex Journey](../0.%20Images/Journey2_step1.JPG)

11. Select "transaction amount" attribute. This information is part of the event, you will find it in "largeDeposit > Adobeamerica275 > Bank transaction" node. drag and drop it on the right side. enter "greater or equal than" as condition, and 100000 as value. Then click on OK.   

![Complex Journey](../0.%20Images/Journey2_step2.JPG)


12.  Click on "Add a path" button. Name is "between 10 and 100k". Then reuse the Transaction attribute as previously with condition "greater than 10000".
Note than the first path have priority over the second, so we don't need to specify "less than 100 000" 
![Complex Journey](../0.%20Images/Journey2_step3.JPG)

13.  On the left pannel, expand the action menu, select "message" and drag and drop it on the canvas after "between 10 and 100k"path. 
Change the label to "send invetment offer", then select the message "FSI -Large deposit"
![Complex Journey](../0.%20Images/Journey2_step4.JPG)

14. On the left pannel, expend the "orchestration", then drag and drop a "wait" activity after your message. Change the amount of time to 14 days. Click on Ok. 
![Complex Journey](../0.%20Images/Journey2_step5.JPG)

15.  Add a new "condition" activity after the wait. change the label to "Check if fund is still unused"
![Complex Journey](../0.%20Images/Journey2_step6.JPG)

16.  Edit the condition, select the segment "FSI - unused funds"

TO UPDATE



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
