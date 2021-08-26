## Exercise 1 - Define an Event

In this exercise, you'll create a custom Event by making use of Journey Orchestration in combination with Adobe Experience Platform.

1. Go to [https://experience.adobe.com/#/@adobeamericaspot5/home](https://experience.adobe.com/#/@adobeamericaspot5/home)

   You'll see the `Adobe Experience Cloud`-homepage.


    ![Demo](./images/aec.png)

2. Click on `Journey Orchestration`.


    ![Demo](./images/aecjo.png)


    Next, you'll see the `Journey Orchestration`-homepage.


    ![Demo](./images/aecjoh.png)

3. In the menu, click on `Events`.


    ![Demo](./images/menuevents.png)


    You'll then see the `Events`-list.


    ![Demo](./images/eventshome.png)

4. Click `Add` to start adding your event.


    ![Demo](./images/add.png)


    You'll see an empty event popup.

    <!---
    ![Demo](./images/emptyevent.png)
    --->

    <kbd><img src="./images/emptyevent.png"  /></kdb>

5. Name the Event **webSignUp{emailAddress}** and replace **{emailAddress}** with your email address name. E.g. **webSignUpPuchadha**.

   Set Description to: **Website Sign up Event - {your email name}**

   <!---
   ![Demo](./images/evname.png)
   --->


    <kbd><img src="./images/evname.png"  /></kdb>

6. Next, you need to select a Schema. All Schemas that are shown here, are Adobe Experience Platform Schemas.

   <!---
   ![Demo](./images/evschema.png)
   --->

   <kbd><img src="./images/evschema.png"  /></kdb>


    To show up in this list, a Schema needs to have a very specific Mixin linked to it. The Mixin that is needed to show up here is called `Orchestration eventID`.


    In our use case, we want to listen for a Sign up Event. This event is part of the `Website interactions EE v.1` schema. Select this from the list.

    <!---
    ![Demo](./images/evschema1.png)
    --->

    <kbd><img src="./images/evschema1.png"  /></kdb>

7. Journey Orchestration will then automatically select some required fields, but you can edit the fields that are made available to Journey Orchestration.


    ![Demo](./images/editfields.png)

8. Click the `pencil`-icon to edit the fields.
   You'll then see a popup-window with a Schema Hierarchy that allows you to select fields.


    ![Demo](./images/popup.png)


    Fields such as the ECID and the Orchestration eventID are required, and as such, preselected.
    However, a marketeer needs to have flexible access to all data points that provide context to a Journey. So you can select additional fields.
    Once you are finished reviewing the fields, select `OK`.


    ![Demo](./images/popupok.png)


    Journey Orchestration also needs an Identifier to identify the customer. Since Journey Orchestration is linked to Adobe Experience Platform, the Primary Identifier of a schema is automatically used as the identifier for the Journey.
    The Primary Identifier will also automatically use the full Identity Graph of the Adobe Experience Platform and link all behavior across all available identities, devices and channels to the same profile. The result is that Journey Orchestration is contextual, relevant and consistent.

    <!---
    ![Demo](./images/eventidentifier.png)
    --->


    <kbd><img src="./images/eventidentifier.png"  /></kdb>

9. Click `Save` to save your custom event.


    ![Demo](./images/save.png)

10. Finally, you need to recover the `Orchestration eventID` for your custom event.

    Open your event again by clicking it in the list of events.

    On your Event, click on the `View Payload`-icon next to `Fields`.


    ![Demo](./images/fieldseye.png)

11. Clicking the `View Payload`-icon opens up a sample XDM payload for this event.


    ![Demo](./images/fieldseyepayload.png)


    Scroll down in the `Payload` until you see the line `eventID`.


    ![Demo](./images/fieldseyepayloadev.png)

12. Note down the `eventID` as you'll need it in the last exercise to test your configuration.

    In this example, the `eventID` is `e133bb4d5075fe9e0356b2136d6413c723d05d146831c6d165d70a5a0dc4a6b8`.

    You've now defined the event that will trigger the Journey we're building. Once the Journey is triggered, the geofence-fields like City, Country, Name, Latitude and Longitude will be made available to the Journey.

    As discussed in the use-case description, we then need to provide contextual promotions that depend on the weather. In order to get weather information, we'll need to define an external data sources that will provide us with the weather information for that location. We'll use the `OpenWeather`-service to provide us what that information, as part of exercise 2.

---

Next Step: [Exercise 2 - Define an External Data Source](./Exercise2-DataSources.md)
