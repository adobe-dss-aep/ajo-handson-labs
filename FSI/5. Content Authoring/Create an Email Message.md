## Lab - Create an Email Message in Adobe Journey Optimizer

In this exercise, you will create an Email Message in Adobe Journey Optimizer, to save time we will start from a message template by duplicating an existing message.  This message will be used to propose some investment offer to people who just made a large deposit on their account. 

1.  Navigate to Messages in the AJO Environment by clicking on “Messages” from the Left Menu
2.  Click to open the "FSI Template" Message; then click the "Duplicate" button
![Message](../0.%20Images/message1.JPG)

3.  Update the message name to be "FSI - Large Deposit Email XX"; replace XX with your attendee number
4.  Click "Duplicate"
![Message](../0.%20Images/message2.JPG)

5. You will arrive in the Message screen, where we will be able to modify property, check preview, and - later - publish the message. We first need to define the content and subject line. 

6.  Click on the subject line
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_4.png)

7.  Click on the canvas and type “Hi”
8.  On the left panel, Use the search attributes to find “First Name” – Click the + Sign to add it to the Subject.  Finish the Subject with “Find the best investment option for you”
9.  Click Save
![Message](../0.%20Images/message5.JPG)

10.  Notice the Subject is now populated.
11.  Click on the blue bar to open the Email Designer, or the "email editor" button on the right side
![Message](../0.%20Images/message6.JPG)

12.  Select an asset to display in the first block, for example "Bank banner" in FSI asset folder
![Message](../0.%20Images/messageAsset1.JPG)
![Message](../0.%20Images/messageAsset2.JPG)

13.  On the left pannel, select "content component", drag and drop the "offer decision component" in the cavas
![Message](../0.%20Images/message9.JPG)

14.  Click on the "select offer decision" button, select "image email" placement, then select the "FSI Invetment" decision.
![Message](../0.%20Images/message10.JPG)

15.  Notice the component shows the Offer
16.  Also notice the Offer Preview has 3 versions. You can select different offers to see the preview 
![Message](../0.%20Images/message11.JPG)

17.  Switch to the component settings on the right menu; update the padding to be 0
![Message](../0.%20Images/message12.JPG)

18.  Click Save

19.  Now, let's insert the customers first name into the text content; Replace the text by "Dear, ..." Place your cursor next to the word "Dear", a menu bar will appear hovering over the compoent.
20.  Click the personalization icon on the right of the menu
![Message](../0.%20Images/message15.JPG)

21.  On the left panel, Use the search attributes to find “First Name” – Click the + Sign to add it to the content. 
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_16.png)

22.  Click on Save

23. At any point of time, even before publishing, you can check the preview of your email and send a proof. 
In your email, click on "Preview"
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_1.png)

36. In the preview screen, you can select test profile for which you can see the preview. The email will be personalized based on those profile. 
We have some test profiles which you can use, first select "Email" as the Identity Namespace, then search for the following email addresses to add them: 
fsi1@gmail.com
fsi2@gmail.com
fsi3@gmail.com
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_2.png)

37. Click now on "preview", then select a test profile to see if personalisation works. 

![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_3.png)

38. You can also send a proof. Select one or multiple test profile, then add your personal email address on the top edit box. then click on "send proof". You can add multiple adddresses if you want to test rendering on gmail, hotmail, etc.

![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_4.png)

39.  Click "Close" to exit the preview screen, and then exit the Email Designer by clicking on the arrow on the top right. 
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/emailPreview_5.png)

40.  Now click the "Publish" button to publish your Message.  If your message is not published, you will be allowed to add it in a journey, but the journey will not be functional until the message is published.  
![Message](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/ME/0.%20Images/Message_18.png)

41.  END OF LAB.
