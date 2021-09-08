## Lab - Understand Unified profile and ID Stitching. 

In the previous exercice we imported CRM data. This will be used by AEP to hydrate your profile information.

1. Navigate to Profile in the AJO Environment from the Left Menu
2. Select "Browse", then browse by identity as we want to retrieve a specific profile. 
Let the "Merge policy" to "Default Timebased", select "Email" in Identity namespace
In Identity Value, enter an email address of a profile. We have created some for you. Use holY.uXX@gmail.svpoc.io where you need to replace Y by the sandbox number (1, 2, or 3) and XX by your attendee number. Ex : hol2.u01@gmail.svpoc.io
Then click on View. 
![Identity](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Identity_profileSearchEmail.JPG)

3. The profile will be shown in the list. Click on it to review information we know about this profile. 
The dashboard shows the main informations about this profile. We know his CRM Id, email, and eventually some ECID (Adobe cookie) if he has browsed some web pages. 

4. click on "attributes" in the top menu. You will see the last information imported from the CRM, such as loyalty points, names, etc. 

5. Now let's see how AJO manage web users.  
Go to the web site provided by the presenters. It should be something like https://builder.adobedemo.com/.....

6. Browse a page or two. 
This informations are stored by Adobe Journey Optimiser, as long as you don't login we will use a cookie as a profile identifier. But if cooie has not been linked to an email or mobile, we can't really communicate with him.

7. OPTIONAL - Check how the data are stored for anonymous.
You can retrieve the Adobe Cookie ID (ECID) used for your profile by opening the debug window of your browser (F12 on Chrome), go to "console", then type "_satellite.getVar('ECID')"
![Identity](https://github.com/adobe-dss-aep/ajo-handson-labs/blob/main/0.%20Images/Identity_web_ECID.JPG)
Copy the ECID. Return to AJO, browse for profile, then search profile by "ECID"
AJO will display a profile, but we don't have email address yet. You can go to "events" and see that the page view have been captured 

8. Go back to the web site, and login using the email address. Use holY.uXX@gmail.svpoc.io where you need to replace Y by the sandbox number (1, 2, or 3) and XX by your attendee number. Ex : hol2.u01@gmail.svpoc.io
No go back to AJO, refresh the profile. 

The ECID has been linked to the email address, and has the CRMID was already linked to your email, we now know everything about your profile : Loyalty, and behaviour.

9.  END OF LAB.