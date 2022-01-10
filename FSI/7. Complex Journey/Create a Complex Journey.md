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

16.  Edit the condition, select the segment "FSI - unused funds", then click Ok.
![Complex Journey](../0.%20Images/Journey2_step7.JPG)

17.  ClickIf After 2 weeks the fund is not unused, maybe we can try to send other offers or try another channel. Just to keep it simple here we will just send a reminder with the same message. 
Add a message after the condition activity, then select the message "FSI - Large Deposit" again. 
![Complex Journey](../0.%20Images/Journey2_step8.JPG)

18.  This path is ready, we just need to add an "end" activity to end the jounrey after this reminder. You can find the "end" activity in the "orchestration" left menu. 
![Complex Journey](../0.%20Images/Journey2_step9.JPG)

19.  We now need to define what happens if the deposit is greater than 100k. Drag and drop a message afer the fist condition, for the second path ( deposit higher than 100k)
![Complex Journey](../0.%20Images/Journey2_step10.JPG)

20.  The message define the content we want to send, but by default it is send to your customer using their personal email address. We need to change this to use the financial advisor email address. On the right pannel when you select the message, notice the "email parameter" section. We can edit this value by clicking the "T" button on the right. 
![Complex Journey](../0.%20Images/Journey2_step11.JPG)

21. Now you can edit the value. Click on the pencil button to enter the editore, search for "financial", and select the "Financial advisor" attribute. This attribute is stored in Experience platform -> profile group -> Profile -> adobeamerica275 -> Financial details. click on OK to save. 
![Complex Journey](../0.%20Images/Journey2_step12.JPG)

22. Add an "end" activity after your mesasge. Your jounrey is now ready!
![Complex Journey](../0.%20Images/Journey2_step13.JPG)


23.  Next step is to test our jounrey before going live. Let's activate the test mode by clicking the check box on the top rubbon. 
In this mode, your journey will be triggered in real time if we receive a deposit event, but it will only work for internal profile marked as "test profile". 
![Complex Journey](../0.%20Images/Journey2_step14.JPG)


24.  We can now test the jounrey for different profile/value of deposit. Click on the "trigger an event" on the left pannel, enter the following value, then click send : 
Identification : FSI1
new account value : 20000
transaction account : AC1
transaction amount : 20000
transaction type : credit
![Complex Journey](../0.%20Images/Journey2_test1JPG.JPG)

25.  You can notice the progress of your jounrey for your test customer. The arrow becoming bold as jounrey progress
![Complex Journey](../0.%20Images/Journey2_test2.JPG)

26. For safety reason, all eail are sent to internal mail bx. You can ask presenter to check if email has been received.
27. you can trigger another event with other value if you want to test the other path, such as amount = 1200000. 

28.  END OF LAB.
