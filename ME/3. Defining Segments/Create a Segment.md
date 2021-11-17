## Lab - Create a Segment in AJO

In this exercise, you will create a Segment in Adobe Journey Optimizer that will be used to send specific communications, or select offer to promote


### Create your first segment
The first segment we want to create is to Identify customers who just have a free subscription plan and who are interested in a specific type of show, and watch only episode 1 of a season. We will use it to propose a paid plan to watch the rest of the season   

1.  Navigate to Segments in the AJO Environment by clicking on “Segments” from the Left Menu
2.  Click on Create Segment
![Segment](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/8f00bf935516f16f128faa2c9eed3ad218ae994b/0.%20Images/Segmentation_1.png)


3.  Insert Name for Segment – “Free subscriber who watched episode1 -XX”. Replace XXX by your attendee number. 

In the segment User Interface, you can create segment based on profile attributes, events, reuse previously created segments, or a combinaison of those options. For this segment we will use profile infomration adn experience events. Let's start with the profile attributes 

4.  Select "Attributes:, search for “Account Type”, or browse property Individual profile > AdobedemoAmerica 275 > Holdings

5.  Drag the attribute onto Canvas. As holdings is a list of account, AJO will create the structure for you to select people who have one specific Account.  Select "equal" then type "free"

![Segment](../0.%20Images/segment1_1.JPG)

6.  Now let's apply additional filter to select people who watch only the episode 1 of a season, and not episode 2. Go to Experience Event, search for "product". or browse event->product list items. this is where we store infomratio nabout product/show viewed. Drag and drop "Name" in the canvas in the middle section. That will create a condition for people who have an event with a specific Product name. Then, specify the product name by selecting "contains", then type "episode 1"  

![Segment](../0.%20Images/Segment1-step2.JPG)

7. Change the time to 6 days.

![Segment](../0.%20Images/Segment1-step3.JPG)

8. We now have people who view any show named "something episode 1" in the last 6 days. Le's filter that further to only select people who watched drama show. 
In the list of attributes on the left panel, click on "adobeamericas275, then drag and drop "Main category" in your event Rules pannel, just below the condition "name contains episode 1". 
Select "equal" then type "drama"

![Segment](../0.%20Images/Segment1-step4.JPG)


9.  Your segment is now ready. You can click on "refresh Extimate" to get a pre count of your segment. Then click on Save


10.  END OF LAB.
