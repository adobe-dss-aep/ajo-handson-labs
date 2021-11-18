## Lab - Create a Real-time Journey in Adobe Journey Optimizer

In this exercise, you will create a Real time Journey in Adobe Journey Optimizer.
We want to encourage customers to upgrade from free to premium plans by offering them a 7 or 30 day free trial. We'll send the offer when we know they have just watched the first episode of a series and need to upgrade to a premium account in order to access the rest of the episodes. 

1.  Navigate to Journeys
2.  Click on “Create Journey”
![Basic Journey](../0.%20Images/Basic_Journey_1.png)

3.  Provide a Name and Description : Premium Trial Journey XX. Replace XX by your attendee number. 
4.  Unclick “Allow Re-Entrance” as we want to send this offer only once per customer.
5.  Click Ok.
![Basic Journey](../0.%20Images/Basic_Journey_2.png)

6.  To start the Journey, drag the "Segment Qualification” Event Node onto the Canvas.
7.  Click on the Label and update it to "Just watched free episode"
8.  Select the segment you created earlier today "Free subscriber who watched episode1 -XX"
![Basic Journey](../0.%20Images/Basic_Journey_3.png)

9.  Now from the "Orchestration" panel, drag a "Wait" activity and connect it to the segment qualification node.
10.  Update the duration and label for the wait event to be 2 hours 
![Basic Journey](../0.%20Images/Basic_Journey_4.png)

10.  Now pull in a "Condition" activity and set the label to "Have they upgraded?" - we want to check that they haven't upgraded during the 2 hours that we have waited.  
11.  Then update the "Path1" label to be "Yes" and tick the box "Show path for other cases than the ones above" and label this "No"
![Basic Journey](../0.%20Images/Basic_Journey_5.png)

12.  Now click to add an expression, in the left menu search for "M&E", you should see a segment called "M&E Paid Subscribers"
13.  Drag the segment into the expression and leave the setting as "segment membership is true"  
14.  Click "Ok".
![Basic Journey](../0.%20Images/Basic_Journey_6.png)

15.  Add an "end" activity to the "Yes" branch and click Ok - we don't want to message anyone who has upgraded already.
![Basic Journey](../0.%20Images/Basic_Journey_7.png)

16.  From under the "Actions" menu on the left, drag a "Message" activity to the canvas and connect it to the end of the "No" branch.
17.  Update the label of the message to "Send Premium Trial Offer"
![Basic Journey](../0.%20Images/Basic_Journey_8.png)

18.  Select the message you created in the previous exercise and add it to the activity.  We could add paths for SMS, push, etc. but for this journey we will keep it simple and just use email.  
![Basic Journey](../0.%20Images/Basic_Journey_9.png)

19.  Click OK.
20.  Drag another "End" activity to complete the journey.
Your journey should now lool like : 
![Basic Journey](../0.%20Images/Basic_Journey_10.png)

21. Your journey is now Ready. We can test it before publishing it. Click on "test" in the top menu.
By selecting "test" mode, your journey can be triggered for internal "test profile".

22. In the left side, you can overide the time that any wait activities pause for to enable easier testing.  By default it is 10seconds.  This means our journey will only wait for 10 seconds after the segment qualification event before continuing instead of waiting for 2 hours.   
23. You can now trigger the journey for a single test profile at a time.  
![Basic Journey](../0.%20Images/Journey1_test1.png)

24. Still on the left menu, select "trigger event". Enter one of the following ECID values according to your attendee number:

Attendee 01: 48703955349127266004164859492197811621 

Attendee 02: 48703955349127266004164859492197811622 

Attendee 03: 48703955349127266004164859492197811623 

Attendee 04: 48703955349127266004164859492197811624 

Attendee 05: 48703955349127266004164859492197811625 

Attendee 06: 48703955349127266004164859492197811626 

Attendee 07: 48703955349127266004164859492197811627 

Attendee 08: 48703955349127266004164859492197811628 

Attendee 09: 48703955349127266004164859492197811629

![Basic Journey](../0.%20Images/Journey1_test2.png)

25. Your journey is triggered for this profile. You will see path taken by your profile and the email will be received in our web mail box. 

![Basic Journey](../0.%20Images/Journey1_test3.png)

Ask presetenter to check the email if you don't have access. 

![Basic Journey](../0.%20Images/Journey1_test4.png)


26.  END OF LAB
