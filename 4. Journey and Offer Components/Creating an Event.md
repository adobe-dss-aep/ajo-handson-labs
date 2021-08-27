## Lab - Create an Event in AJO

In this exercise, you will create an Event in Adobe Journey Optimizer.

1.  Navigate to Journeys
2.  Click on Manage in Events
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_1.png)

3.  Click on Create Event
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_2.png)

4.  Click on Name – Change the Name to “LumaPurchase##”  - where ## is the Attendee Number.
5.  Click on Type – Select Unitary
6.  Click on Event ID Type – Select Rules Based
7.  Click on Schema – Select CRM Profile Transaction Event Schema
8.  Click on Fields
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_3.png)

9.  Click on Fields
10.  Click on Order to select the Fields that are being used to track the event.
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_4.png)

11.  Select OrderTotal
12.  Click OK.
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_5.png)

13.  Click on Event ID Condition – Click on the Pencil to open the “Add an Event ID Condition”
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_6.png)

14.  Click on OrderTotal
15.  Drag onto the Canvas 
16.  Select “Greater Than” – and set value to “0”.
17.  Click Ok
18.  Click Ok
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_7.png)

19.  Notice that Event ID Condition has been populated;
20.  Leave NameSpace as “CRMID”;  Leave Profile Identifier as “The CRMID of Identification”
21.  Click Save.
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_8.png)

22.  Notice that the Event is now listed in your Events List.
![Event](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/c3a5eba7996441f20b79aea2e9302a5781060d8a/0.%20Images/Creating_Event_9.png)

23.  END OF LAB.
