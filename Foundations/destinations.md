Lab  - Activation Workflow  
==========
<table style="border-collapse: collapse; border: none;" class="tab" cellspacing="0" cellpadding="0">

<tr style="border: none;">

<div align="left">
<td width="600" style="border: none;">
<table>
<tbody valign="top">
      <tr width="500">
            <td valign="top"><h3>Objective:</h3></td>
            <td valign="top"><br>In this exercise, we’ll share segments created in a previous lab with an S3 destination.</br>
            </td>
     </tr>
     <tr width="500">
           <td valign="top"><h3>Prerequisites:</h3></td>
           <td valign="top"><br>S3 Destination</td>
     </tr>
</tbody>
</table>
</td>
</div>

<div align="right">
<td style="border: none;" valign="top">

<table>
<tbody valign="top">
      <tr>
            <td valign="middle" height="70"><b>section</b></td>
            <td valign="middle" height="70"><img src="https://github.com/adobe/AEP-Hands-on-Labs/blob/master/assets/images/left_hand_nav_menu_segments.png?raw=true" alt="Segments"></td>
      </tr>
      <tr>
            <td valign="middle" height="70"><b>version</b></td>
            <td valign="middle" height="70">3</td>
      </tr>
      <tr>
            <td valign="middle" height="70"><b>date</b></td>
            <td valign="middle" height="70">2021-04-26</td>
      </tr>
</tbody>
</table>
</td>
</div>

</tr>
</table>

Instructions:
-----------------
1.	In the left navigation of AEP, select Destinations.
2.	Select the 'My destinations’ radio button in the Catalog view. Verify you see an Amazon S3 Connection 

![Demo](./images/mydestinations.png)

3.	Select 'Activate'. You have two choices for Account type: 'Existing account' and 'New account'. Keep the default selection for 'Existing account'. Select the radio button to the left of the Amazon S3 destination and click 'Next' in the upper right corner.

![Demo](./images/account_existing.png)
 
4.	In the 'Authentication' screen, enter the following values: 
      Name: AEP Activation 
      Description: Activation to S3
      Bucket-name: rtcdp-lab
      Folder-path: /rtcdp-lab/pot5
      Marketing actions: Export to third party

![Demo](./images/destination_authenticate.png)
 
5.	Select 'Create destination'. Then select 'Next' in the upper right corner.

6.	On the 'Select segments' screen, select the segments you created in the previous lab (Segments).

![Demo](./images/select_segments.png)

8.	Click on ‘Next’ in the upper right corner of the workflow. This will take you to the 'Scheduling' step. Open the 'Schedule' settings and select 'Export incremental files'. Select the current date in the calendar.

![Demo](./images/scheduling.png)

9.	Click on 'Next' in the upper right corner of the workflow. Clear all fields. Add two new fields:
      person.gender
      personalEmail.address

![Demo](./images/attributes.png)

10.   Click on 'Next' in the upper right corner of the workflow. This will take you to the the 'Review' step. Select 'Finish' to complete the Profile Activation.

![Demo](./images/dest_review.png)

<br>
<br>
<br>

Return to [Lab Agenda Directory](https://github.com/adobe/AEP-Hands-on-Labs/blob/master/labs/retail/README.md#lab-agenda)
