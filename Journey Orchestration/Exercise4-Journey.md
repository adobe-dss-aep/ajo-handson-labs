## Exercise 4 - Design a trigger-based Customer Journey

In this exercise, you'll create an Orchestrated Journey by making use of Journey Orchestration in combination with Adobe Experience Platform

1. Go to [https://experience.adobe.com/#/@adobeamericaspot5/home](https://experience.adobe.com/#/@adobeamericaspot5/home)

   You'll see the `Adobe Experience Cloud`-homepage.

   ![Demo](./images/aec.png)

2. Click on `Journey Orchestration`.

   ![Demo](./images/aecjo.png)

   Next, you'll see the `Journey Orchestration`-homepage, which shows all existing Journeys.

   ![Demo](./images/aecjoh.png)

3. Click `Create` to start creating your Journey.

   ![Demo](./images/jocreate.png)

   You'll then see a new, blank Journey.

   <kbd><img src="./images/jonew.png"  /></kdb>

4. Name the Journey **Website Registration Journey emailAddress** and replace **emailAddress** with LDAP. In this example, the Journey Name is **Website Registration Journey puchadha**. No other values must be set at this moment.

   <kbd><img src="./images/joname.png"  /></kdb>

   Click `OK`.

   ![Demo](./images/jonameok.png)

5. On the left side of your screen, have a look at `Events`. You should see your previously create Event on that list. Select it, then drag and drop it on the Journey Canvas.

   ![Demo](./images/joevents.png)

   Your Journey then looks like this:

   ![Demo](./images/jo1.png)

6. Next, click on `Orchestration`.

   ![Demo](./images/jo2.png)

   You now see `Orchestration`-capabilities.

   ![Demo](./images/jo3.png)

7. Select `Condition`, then drag and drop it on the Journey Canvas.

   <kbd><img src="./images/jo4.png"  /></kdb>

8. You now have to define 2 conditions:

   - It's Raining
   - It's Clear

   Let's define the first condition.

9. Click on the `Condition`.

   #### Condition 1: It's Raining

   <kbd><img src="./images/jo5.png"  /></kdb>

10. Click on the `Edit`-icon for the expression of Path1.

    <kbd><img src="./images/jo6.png"  /></kdb>

    You'll then see an empty `Simple Editor`-screen.

    ![Demo](./images/jo7.png)

    Our query will be a bit more advanced, so we'll need the `Advanced Mode`.

11. Click `Advanced Mode`.

    ![Demo](./images/jo8.png)

    You'll then see the `Advanced Editor` which allows code entry. Paste it in `##{weatherApiemailAddress.WeatherByZipemailAddress.weather.main} == 'Rain'` (replace emailAddress)

    You'll then see this.

    ![Demo](./images/jo10.png)

12. In order to retrieve the temperature as part of this Condition, you need to provide the zipCode in which the customer currently is.
    The `zipCode` needs to be linked to the dynamic parameter `zip`.

    Click the field `dynamic val: zip` as indicated in the screenshot.

    <kbd><img src="./images/jo11.png"  /></kdb>

    You then need to find the field that contains the current zip code of the customer in the AEP Data Sources. Here we are leveraging the unified profile data in AEP to get the profiles zip code.

    You can navigate the field structure from the panel or simply paste the expression below into the expression text box.
    `#{ExperiencePlatform.ProfileFieldGroup.profile.homeAddress.postalCode}`

    ![Demo](./images/jo12.png)

13. Click `OK`.

    ![Demo](./images/jook.png)

14. Rename the path from path1 to 'Raining'

    <kbd><img src="./images/jopath1name.png"  /></kdb>

15. Next, we'll add the 2nd condition.

    #### Condition 2: Its Clear

    After having added the first condition, you'll see this screen.

    <kbd><img src="./images/joc2.png"  /></kdb>

16. Click `Add Path`.

    ![Demo](./images/joadd.png)

17. Click on the `Edit`-icon for the expression of Path1.

    <kbd><img src="./images/jo6.png"  /></kdb>

    You'll then see an empty `Simple Editor`-screen.

    ![Demo](./images/jo7.png)

    Our query will be a bit more advanced, so we'll need the `Advanced Mode`.

18. Click `Advanced Mode`.

    ![Demo](./images/jo8.png)

    You'll then see the `Advanced Editor` which allows code entry. Paste it in `#{weatherApiemailAddress.WeatherByZipemailAddress.weather.main} == 'Clear'` (replace emailAddress)

    You'll then see this.

    ![Demo](./images/jo14.png)

19. To retrieve the temperature as part of this Condition, you need to provide the zipCode in which the customer currently is.
    The `zipCode` needs to be linked to the dynamic parameter `zip`.

    Click the field `dynamic val: zip` as indicated in the screenshot.

    <kbd><img src="./images/jo11.png"  /></kdb>

    You then need to find the field that contains the current zip code of the customer in the AEP Data Sources. Here we are leveraging the unified profile data in AEP to get the profiles zip code.

    You can navigate the field structure from the panel or simply paste the expression below into the expression text box.
    `#{ExperiencePlatform.ProfileFieldGroup.profile.homeAddress.postalCode}`

    ![Demo](./images/jo12.png)

20. Click `OK`.

    ![Demo](./images/jook.png)

21. Rename the path from path1 to 'Clear'

    <kbd><img src="./images/jopath2name.png"  /></kdb>

    Hit Ok on the top right

    ![Demo](./images/joocok.png)

22. Next, we will be adding in Actions.

    #### Add Actions for Raining Path

    We'll attempt to send an SMS message to our customer.

    Your Journey will then look like this.

    ![Demo](./images/joa8.png)

23. Click on `Actions` as indicated in the screenshot.

    Select the smsNexmoemailAddress - action (your emailAddress), then drag and drop it after the condition you just added.

    ![Demo](./images/joa9.png)

    You'll see a popup.

    <kbd><img src="./images/joa10.png"  /></kdb>

24. Navigate to the `Action Parameters`.

    <kbd><img src="./images/joa11.png"  /></kdb>

25. Click on the `Edit`-icon for the Action Parameter `Mobile PhoneNumber`.

    ![Demo](./images/joa12.png)

    In the popup, you'll see, click on `Advanced Mode`.

    ![Demo](./images/jo8.png)

    Select the below code, copy it, and paste it in the `Advanced Mode Editor`.

    `#{ExperiencePlatform.ProfileFieldGroup.profile.mobilePhone.number}`

    ![Demo](./images/joa14.png)

26. Click `OK`.

27. Click on the `Edit`-icon for the Action Parameter `Message`.

    <kbd><img src="./images/joa15.png"  /></kdb>

    You'll see a popup with the `Simple Mode Editor`.

    ![Demo](./images/joasm.png)

    In the popup, you'll see, click on `Advanced Mode`.

    ![Demo](./images/jo8.png)

28. Paste this code in the `Advanced Mode Editor`. Click `OK`.

    `"Hi "+ #{ExperiencePlatform.ProfileFieldGroup.profile.person.name.firstName} +" don't let it rain on your investments, chat with our Advisors now."`

    ![Demo](./images/joa16.png)

29. Click `OK`.

    ![Demo](./images/joocok.png)

30. Click `OK`.

    <kbd><img src="./images/joa17.png"  /></kdb>

31. In the left menu, go back to `Actions`, select the Action `slackNotification`, then drag and drop it after the `smsNexmoemailAddress`-Action (Replace emailAddress).

    <kbd><img src="./images/joa18.png"  /></kdb>

32. Go to `Action Parameters` and click the `Edit`-icon for the parameter `Message`.

    <kbd><img src="./images/joa19.png"  /></kdb>

    In the popup window, click `Advanced Mode`.

    ![Demo](./images/joa20.png)

33. Select the below code, copy it, and paste it in the `Advanced Mode Editor`.

    `"Hi "+ #{ExperiencePlatform.ProfileFieldGroup.profile.person.name.firstName} +" don't let it rain on your investments, chat with our Advisors now."`

    ![Demo](./images/joa21.png)

34. Click `OK`.

    ![Demo](./images/joocok.png)

35. Click `OK`.

    <kbd><img src="./images/joa22.png"  /></kdb>

36. In the left menu, go to `Orchestration`, select `End`, then drag and drop `End` after the `textSlackLdap`-Action.

    <kbd><img src="./images/joa23.png"  /></kdb>

#### Add Actions for Clear Weather Path

37. We'll attempt to send an SMS message to our customer.

    Your Journey will then look like this. Click on `Actions` as indicated in the screenshot.

    ![Demo](./images/joapath21.png)

38. Select the smsNexmoemailAddress - action (your emailAddress), then drag and drop it after the condition you just added.

    <kbd><img src="./images/joapath22.png"  /></kdb>

    You'll see a popup.

    <kbd><img src="./images/joa10.png"  /></kdb>

39. Navigate to the `Action Parameters`.


    <kbd><img src="./images/joa11.png"  /></kdb>

40. Click on the `Edit`-icon for the Action Parameter `Mobile PhoneNumber`.

    ![Demo](./images/joa12.png)

    In the popup, you'll see, click on `Advanced Mode`.

    ![Demo](./images/jo8.png)

41. Select the below code, copy it, and paste it in the `Advanced Mode Editor`.

    `#{ExperiencePlatform.ProfileFieldGroup.profile.mobilePhone.number}`

    ![Demo](./images/joa14.png)

42. Click `OK`.

    ![Demo](./images/joaok.png)

43. Click on the `Edit`-icon for the Action Parameter `Message`.

    <kbd><img src="./images/joa15.png"  /></kdb>

    You'll see a popup with the `Simple Mode Editor`.

    ![Demo](./images/joasm.png)

    In the popup, you'll see, click on `Advanced Mode`.

    ![Demo](./images/jo8.png)

44. Paste this code in the `Advanced Mode Editor`. Click `OK`.

    `"Hi "+ #{ExperiencePlatform.ProfileFieldGroup.profile.person.name.firstName} +" have a clear path to Retirement, chat with our Advisors now."`

    ![Demo](./images/joapath216.png)

45. Click `OK`.

    ![Demo](./images/joocok.png)

46. Click `OK`.

    <kbd><img src="./images/joapath217.png"  /></kdb>

47. In the left menu, go back to `Actions`, select the Action `slackNotification`, then drag and drop it after the `smsNexmoemailAddress`-Action (Replace emailAddress).

    <kbd><img src="./images/joapath218.png"  /></kdb>

48. Go to `Action Parameters` and click the `Edit`-icon for the parameter `Message`.

    <kbd><img src="./images/joa19.png"  /></kdb>

49. In the popup window, click `Advanced Mode`.

    ![Demo](./images/joa20.png)

    Select the below code, copy it, and paste it in the `Advanced Mode Editor`.

    `"Hi "+ #{ExperiencePlatform.ProfileFieldGroup.profile.person.name.firstName} +" have a clear path to Retirement, chat with our Advisors now."`

    ![Demo](./images/joapath221.png)

50. Click `OK`.

    ![Demo](./images/joaok.png)

51. Click `OK`.

    <kbd><img src="./images/joapath222.png"  /></kdb>

52. In the left menu, go to `Orchestration`, select `End`, then drag and drop `End` after the `textSlackLdap`-Action.

    <kbd><img src="./images/joapath223.png"  /></kdb>

    Your Journey is now fully configured.

    ![Demo](./images/jodone.png)

53. Click `Publish`.

    ![Demo](./images/jopublish.png)

54. Click `Publish`.

    ![Demo](./images/jopublish1.png)

    Your Journey is now published.

    ![Demo](./images/jopublish2.png)

---
