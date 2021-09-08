## Lab - Create a Basic Journey in Adobe Journey Optimizer

In this exercise, you will create a Basic Journey in Adobe Journey Optimizer.
We want to boost sales by proposing a coupon to silver members, and help them to reach Gold. 

1.  Navigate to Journeys
2.  Click on “Create Journey”
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_1.png)

3.  Provide a Name and Description : Coupon Journey XX. Replace XX by your attendee number. 
4.  Unclick “Allow Re-Entrance” as we want to run this campaing only once.
5.  Click Ok.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_2.png)

6.  To start the Journey, drag the “Read Segment” Orchestration Node onto the Canvas.
7.  The Canvas is in the middle of the screen.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_3.png)

8.  Click on the Label of the Read Segment.  Change the label to “Silver Loyalty Members”.
9.  Click on the pencil in the Segment.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_5.png)

10.  From the Choose Segment applet, select “Silver Loyalty Members”.
Change the Namespace to "Email". The namespace is used to identify profile, this is specially used for proofing. It will be easier to retrieve  aprofile by his email address. 
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Journey1_namespace.JPG)

11.  Click Save.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_5.png)

12.  Drag the “Condition” Orchestration Node after the Read Segment.
13.  Give it a Name of “Check preferred channel”.
14.  The type should be “Data Source Condition”
15.  In the Path, select Email optin as the Condition.  Add a name “Email Optin”. 
To select the condition, browse ExperiencePlatform > ProfileFieldGroup > profile > optInOut > channels, or search for "email"
Drag and drop the element "email" to the right side, then select "in"
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Jounrey1_condition.JPG)

16. Optional : You can add path for SMs, push, etc. 

17. Select "Show path for other cases than the one(s) above" and give a name "other

18.  Click OK.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_6.png)

19.  Drag the Message Action onto the Canvas on Path 1.
20.  Drag the End Node onto the Canvas on Path 2.
21.  For the Message Action, give it a name 10% Off Email.
22.  Click on the “Select a Message”
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_7.png)

23.  Click on the “Luma coupon Email” Message. Or select Luma coupon Email XXX if you have create your own in the previous exercice.

24.  Click Select.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_8.png)

25.  Click Ok.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_9.png)

26.  Add an End Node to the end of the Journey.
27.  Give it a Label of “End of Journey”.
28.  Click OK.
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Basic_Journey_10.png)

29. Your journey is now Ready. We can test it. Click on "test" in the top menu.
By selecting "test" mode, your journey can be triggered for internal "test profile".

30. In the left side, you can trigger the jounrey for one single profile or up to 100 profiles. Clic on :single profile at a time. 
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Journey1_test1.JPG)

31. Still on the left menu, select "trigger profile entrance". Enter an email address of a test profile. We have created a test profile for you. Use hol_XXX@gmail.svpoc.io where you replace XXX by your attendee number ex :   hol_001@gmail.svpoc.io 
![Basic Journey](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/96de49783d41b9e93724aa08aa6ccd5f3c0f42c9/0.%20Images/Journey1_test2.JPG)

32. You journey is triggered for this profile. You will see path taken by your profile and the email will be received in our web mail box. 
Ask presetenter to check the email if you don't have access. 

29.  END OF LAB
