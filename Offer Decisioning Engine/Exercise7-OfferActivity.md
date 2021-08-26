## Exercise 7 - Create an Offer Activity

Offer activities are containers for your offers that will leverage the Offer Decision Engine in order to pick the best offer to deliver, depending on the target of the delivery.
The list of offer activities is accessible in the Activities menu. Filters are available to help you retrieve activities according to their status or start and end dates.

In this exercise, you'll create an activity, which is simply a container for your offers that contains the logic that informs the selection of an offer.

To create an activity, follow these steps:

1.	Select the Activities menu, then click `Create activity`

    ![Demo](images/createActivity.png)
    
  - Specify the activity’s name. For the purposes of the lab, please use this naming convention. (“UpsellActivity + your sandbox number. Ex: AutoLoanUpsellActivity24”)

2.	 Define a start and end date, and time. Start date = today. End date = 1 year from today, then click `Next`

![Demo](images/createActivity2.png)
    
3.	Drag and drop or click on the “+” to add the placements for the banner, email text and mobile text from the list to add it to the activity. 

    ![Demo](images/createActivity3.png) 
    
4.	Click `Add collection` for the EmailBannerPlacement. You should see your associated offers listed in the collection we created earlier.
5.	Click `Add` to add all of the available offers in the collection to the placement.

    ![Demo](images/createActivity5.png) 

6.	Repeat this process for both the EmailTextPlacement and the MobileTextPlacement by clicking on `Add collection` and clicking `Add` to add all the available offers in the collection to that placement.
7.	Click `Next` to confirm.
8.	Select the Fallback offer that will be presented as a last resort to the customers that do not match the offers eligibility rules and constraints
9.	Click `Next` to review a summary of you offer activity. You should see 3 decisions, each containing 2 offer types (Auto loan and Wealth management,) and a fallback offer.
 
    ![Demo](images/createActivitySummary.png) 
    
10.	If everything is configured properly and your activity is ready to be used to present offers to customers, click `Finish` then select `Save and activate`


 ---

Next Step: [Exercise 8 - Validate Your Offer ](Exercise8-ValidateOffer.md)
