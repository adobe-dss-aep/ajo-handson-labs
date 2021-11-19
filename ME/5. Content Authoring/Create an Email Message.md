## Lab - Create an Email Message in Adobe Journey Optimizer

In this exercise, you will create an Email Message in Adobe Journey Optimizer, to save time we will start from a message template by duplicating an existing message.  This message will be used to encourage people to upgrade their plan from free to paid. 

1.  Navigate to Messages in the AJO Environment by clicking on “Messages” from the Left Menu
2.  Click to open the "M&E Template" Message; then click the "Duplicate" button
3.  Update the message name to be "Media Premium Trial Email XX"; replace XX with your attendee number
4.  Click "Duplicate"
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_2.png)

5. You will arrive in the Message screen, where we will be able to modify property, check preview, and - later - publish the message. We first need to define the content and subject line. 

6.  Click on the subject line
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_4.png)

7.  Click on the canvas and type “Hey”
8.  On the left panel, Use the search attributes to find “First Name” – Click the + Sign to add it to the Subject.  Finish the Subject with “Here’s a Special Offer for You!”
9.  Click Save
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_5.png)

10.  Notice the Subject is now populated.
11.  Click on the blue bar to open the Email Designer
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_6.png)

12.  From the "Structure Components" menu in the left nav, click on the 1:1 Column
13.  Drag it onto the Canvas underneath the logo and again underneath the CTA button
14.  Click Save
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_8.png)

15.  Open the "Content Components" menu in the left nav
16.  Add an Image in the top 1..1 Component slot
17.  Add an Offer Decision in the second 1..1 Component slot
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_9.png)

18.  Click on the Image component, select "Browse" to pick an image from the asset repository
19.  Click on the "Media" folder and select an image of your choice
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_10.png)

20.  Click on the Offer Decision component
21.  Click on “Select Offer Decision” in the component properties on the right
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_11.png)

22.  Select Email Image Placement
23.  Select the Offer Decision "Media Offer"
24.  Click “Add”
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_12.png)

25.  Notice the component shows the Offer
26.  Also notice the Offer Preview has 3 versions
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_13.png)

27.  Switch to the component settings on the right menu; update the padding to be 0
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_14.png)

28.  Click Save

29.  Now, let's insert the customers first name into the text content; Place your cursor next to the word "Dear", a menu bar will appear hovering over the compoent.
30.  Click the personalization icon on the right of the menu
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_15.png)

31.  On the left panel, Use the search attributes to find “First Name” – Click the + Sign to add it to the content. 
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_16.png)

32.  Click on Save

33.  Now let's update the CTA destination link, click on the button and add "https://www.adobedemo.com/binji/upgrade" to the link setting
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_17.png)

34.  Click Save

35. At any point of time, even before publishing, you can check the preview of your email and send a proof. 
In your email, click on "Preview"
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_1.png)

36. In the preview screen, you can select test profile for which you can see the preview. The email will be personalized based on those profile. 
We have some test profiles which you can use, first select "Email" as the Identity Namespace, then search for the following email addresses to add them: 
media1@gmail.svpoc.io
media2@gmail.svpoc.io
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_2.png)

37. Click now on "preview", then select a test profile to see if personalisation works. 

![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_3.png)

38. You can also send a proof. Select one or multiple test profile, then add your personal email address on the top edit box. then click on "send proof". You can add multiple adddresses if you want to test rendering on gmail, hotmail, etc.

![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_4.png)

39.  Click Publish. 
If your message is not published, you will be allowed to select it in a journey, but the journey will not be functional until the message is published.  
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_18.png)


40.  END OF LAB.
