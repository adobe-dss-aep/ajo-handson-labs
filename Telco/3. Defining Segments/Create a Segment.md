## Lab - Create a Segment in AJO

In this exercise, you will create two Segments in Adobe Journey Optimizer that will be used to send specific communications, or select offer to promote


### First Segment
The first segment we want to create is to Identify customers who may have a mobile plan, but no broadband plan. This can used for cross sale.  

1.  Navigate to Segments in the AJO Environment by clicking on “Segments” from the Left Menu
2.  Click on Create Segment
![Segment](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/8f00bf935516f16f128faa2c9eed3ad218ae994b/0.%20Images/Segmentation_1.png)


3.  Insert Name for Segment – “No Broadband - XXX”. Replace XXX by your attendee number. 

In the segment User Interface, you can create segment based on profile attributes, events, reuse previously created segments, or a combinaison of those options. For this segment we just use profile infomration. 

4.  Select "Attributes:, search for “Account Type”, or browse property Individual profile > AdobedemoAmerica 275 > Holdings

5.  Drag the attribute onto Canvas. As holdings is a list of account, AJO will create the structure for you to select people who have one specific Account.  Select "equal" then type "broadband"

![Segment](../0.%20Images/segment1_1.JPG)

6.  We also want to target customer, not anonymous user on who came to the web site and didn't loged in. So let's filter our segment by selecting only customer. For this, let's check if we have a CRMID. Search for CRMID, drag and drop it below your first condition, then select "exist"

![Segment](../0.%20Images/segment1_final.JPG)

You can click on "refresh Extimate" to get a pre count of your segment.  

7.  Click on Save


### Second Segment
Let's imagine we also want to propose mobile phone. We will need to understand which type of phone our prospect are interested in, for example iphone or galaxy. For that we will need to use their behavioural data. In this ex

9.  Go back to segment list, create a new one. Name it "Galaxy Phone prospect - XX" Replace XX by your attendee number

10. For this segment we want to target people who have viewed at least 2 pages of Galaxu phone, then didn't purchase 
All interactions on the web site are captured and stored as experience events.  
Select "events" in the left pannel.

10. Search for "SKU", or browse XDM ExperienceEvent > Product List Item > SKU. Drag and Drop the SKU attributes in the middle part. Select "contains 'galaxy'". You can also define how mny time this event should happens. Select "Include at least 2".
![Segment](/0.%20Images/Segment2_step1.JPG)
 
 
12. Second step is to check if they went to the web site and posted a review. WE use the information captured by the web site for this. Browse for web > web interaction, then drag and drop this attribute on the right side of the first event. Select name "equal review"     
![Segment](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Segment2_step3.JPG)
 
13. Last step is to define when do we want this events to occurs to be part of the segment. Let select in last 7 days ( the time condition just above the 2 events.)

14. Save your segment. 

15.  END OF LAB.
