## Lab - Understand Unified profile and ID Stitching. 

In the previous exercice we importde CRM data. This will be used by AEP to hydrate your profile information.

1. Navigate to Profile in the AJO Environment from the Left Menu
2. Select "Browse", then browse by identity as we want to retrieve a specific profile. 
Let the "Merge policy" to "Default Timebased", select "Email" in Identity namespace
In Identity Value, enter the email address you used to login in AEP. i.e ajoholuser_XXX@adobe.com and replace XXX by your number
Then click on View. 

3. The profile will be shown in the list. Click on it to review infomration we know about this profile. 
The dashboard shows the main oformation aboit this profile. We know his CRM Id, the email, and eventually some ECID (Adobe cookie) if this has browse some web pages. 

4. click on "attributes" in the top menu. You will see the last information importde from the CRM, such as loyalty points, names, etc. 

5. Now let's see how AJO manage web users.  
Go to the web site provided by the presenters. It should be something like https://builder.adobedemo.com/.....

6. Browse a page or two. 
This infomrations are stored by Adobe Journey Optimiser, as long as you don't login we will a cookie as a profile identifier. But if cooie has not been linked to an email or mobile, we can't really communicate with him.

7. OPTIONAL - Check how the data are stored.
You can retrieve the Adobe Cookie ID (ECID) used for your profile by opening the debug window of your browser (F12 on Chrome), go to "console", then type "_satellite.getVar('ECID')"
Copy the ECID. Return to AJO, browse for profile, then search profile by "ECID"
AJO will display a profile, but we don't have email address yet. You can go to "events" and see that the page view have been captured 

8. Go back to the web site, and login using the email address (something like ajoholuser_XXX@adobe.com)
No go back to AJO, refresh the profile. 
The ECID has been linked to the email address, and has the CRMID was already linked to your email, we now know everything about your profile : Loaylty, and behaviour.

9.  END OF LAB.