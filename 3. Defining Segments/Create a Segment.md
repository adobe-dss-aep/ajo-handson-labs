## Lab - Create a Segment in AJO

In this exercise, you will create two Segments in Adobe Journey Optimizer that will be used to send specific communications.


# First Segment
The first segment we want to create is to send coupon to sliver member who have low propensity score to buy in the next 3 months. 
We will send coupon to those customers to boost our sales. 

1.  Navigate to Segments in the AJO Environment by clicking on “Segments” from the Left Menu
2.  Click on Create Segment
![Segment](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/8f00bf935516f16f128faa2c9eed3ad218ae994b/0.%20Images/Segmentation_1.png)


3.  Insert Name for Segment – “Silver Coupon - XXX”. Replace XX by your attendee number. 

In the segment User Interface, you can create segment basde on profile attribute, events, reuse created segment, or a combinaison of those options. Fr this segment we just use profile infomration. 

4.  Select "Attributes:, search for “Level”, or browse property Individual profile > AdobedemoAmerica 275 > Loyalty

5.  Drag Event Level onto Canvas. Select "silver"

![Segment](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/8f00bf935516f16f128faa2c9eed3ad218ae994b/0.%20Images/Segment1-step1.JPG)

6.  Search for "propensity", Select "propensity to buy in the next 3 months", and drag and drop below the "level = silver" block. 
Select "is less than 75" as we don't want to give coupon to people who are likely to buy anyway. 
Check the condition is "AND"

![Segment](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/8f00bf935516f16f128faa2c9eed3ad218ae994b/0.%20Images/Segment1-step2.JPG)

You can click on "refresh Extimate" to get a pre count of your segment.  

7.  Click on Save

8.  Notice that the Segment has been created.
![Segment](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/8f00bf935516f16f128faa2c9eed3ad218ae994b/0.%20Images/Segment1-step3.JPG)
 

# Second Segment
Later on the journey, we will want to retarget people who have receive a coupon but didn't use it for purchase. Let's create this 
segment.

9.  Go back to segment list, creae a new one. Name it "Coupon unused- XXX" Replace XXX by your attendee number

10. Select "events" in the left pannel. 
For this segment we want to target people who have received a coupon, then not made a purchase. We need to define a sequence of events. 


9.  END OF LAB.
