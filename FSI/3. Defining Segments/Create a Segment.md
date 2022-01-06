## Lab - Create a Segment in AJO

In this exercise, you will create a Segment in Adobe Journey Optimizer that will be used to send specific communications, or select offer to promote


### Create your first segment
The first segment we want to create is to identify customers who Can be interested in Term deposit account. We will select this profile based on their risk preference, accounts owned, and net worth.    

1.  Navigate to Segments in the AJO Environment by clicking on “Segments” from the Left Menu

2.  Click on Create Segment

![Segment](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/8f00bf935516f16f128faa2c9eed3ad218ae994b/0.%20Images/Segmentation_1.png)


3.  Insert Name for Segment – “FSI - TD prospect -XX”. Replace XXX with your attendee number. 

In the segment User Interface, you can create segment based on profile attributes, events, reuse previously created segments, or a combinaison of those options. For this segment we will use profile information. Let's start with the profile attributes 


4.  Select "Attributes:, search for “Account Type”, or browse property Individual profile > AdobedemoAmerica 275 > Holdings


5.  Drag the attribute onto Canvas. As holdings is a list of account, AJO will create the structure for you to select people who have one specific Account.  Select "equal" then type "TD"


![Segment](../0.%20Images/segment1_1.JPG)


6. Replace the condition "include account" to"exclude account as we don't want to target customers who already have a term deposit account   

![Segment](../0.%20Images/Segment1-step2.JPG)


7. Now let's add the risk preference to select people who prefer 'low' to 'medium' risk type investment. Search for "risk", and drag and drop the "risk profile" attribute BELOW the block account. 

![Segment](../0.%20Images/Segment1-step3.JPG)


8. verify that condition "equal" is selected, then select value "low" in the drop down list. Repeat to add value " medium. Finally check that we select people who have no TD account AND risk profile = low or medium..

![Segment](../0.%20Images/Segment1-step4.JPG)


9. Now let's check they have enough money to invest. Search for "networth", add the attribute in your condition below previous condition, then select "greater than 30000. 

![Segment](../0.%20Images/Segment1-step5.JPG)


10. Your segment is now ready, click on Save

11.  END OF LAB.
