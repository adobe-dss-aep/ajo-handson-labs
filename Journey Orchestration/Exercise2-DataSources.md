## Exercise 2 - Define an External Data Source

In this exercise, you'll create a custom External Data Source by making use of Journey Orchestration in combination with Adobe Experience Platform

1. Go to [https://experience.adobe.com/#/@adobeamericaspot5/home](https://experience.adobe.com/#/@adobeamericaspot5/home)

   You'll see the `Adobe Experience Cloud`-homepage.

   ![Demo](./images/aec.png)

2. Click on `Journey Orchestration`.

   ![Demo](./images/aecjo.png)

   Next, you'll see the `Journey Orchestration`-homepage.

   ![Demo](./images/aecjoh.png)

3. In the menu, click on `Data Sources`.

   ![Demo](./images/menudatasources.png)

   You'll then see the `Data Sources`-list.

     <!---
     ![Demo](./images/dshome.png)
     --->

   <kbd><img src="./images/dshome.png"  /></kdb>

4. Click `Add` to start adding your data source.

   ![Demo](./images/add.png)

   You'll see an empty data source popup.

     <!---
     ![Demo](./images/emptyds.png)
     --->

   <kbd><img src="./images/emptyds.png"  /></kdb>

5. We will use `Open Weather Map`-service. For reference you can go to [https://openweathermap.org/](https://openweathermap.org/).

   Back to `Journey Orchestration`, to your empty `External Data Source`-popup.

   Name the Data Source, use **weatherApi{emailAddress}** and replace **emailAddress** with your email address name. E.g. **weatherApiPuchadha**.

   Set Description to: **Access to the Open Weather Map**.

   The URL for the Open Weather Map API is: `http://api.openweathermap.org/data/2.5/weather`

     <!---
     ![Demo](./images/dsname.png)
     --->

   <kbd><img src="./images/dsname.png"  /></kdb>

6. Next, you need to select the Authentication to use. Select from the 'Type' dropd-down.

   Use the following values for the fields:

   |  Field   | Value                                |
   | :------: | :----------------------------------- |
   |   Type   | **API key**                          |
   |   Name   | **APPID**                            |
   |  Value   | **4ca8c0b493237afd3bed3e70f399b795** |
   | Location | **Query Parameter**                  |

     <!---
     ![Demo](./images/dsauth.png)
     --->

   <kbd><img src="./images/dsauth.png"  /></kdb>

7. Finally, you need to define a `FieldGroup`, which is the request you'll be sending to the Weather API.

   In our case, we want to use the ZipCode to request the Current Weather for that Zip.

     <!---
     ![Demo](./images/fg.png)
     --->

   <kbd><img src="./images/fg.png"  /></kdb>

   In order to match the expected API Request, configure your FieldGroup as follows:

   **IMPORTANT**

   The Field group name has to be unique, please rename fieldGroup and use this naming convention: **WeatherByZipemailAddress** so in this case, the name should be **WeatherByZipPuchadha**

     <!---
     ![Demo](./images/fg1.png)
     --->

   <kbd><img src="./images/fg1.png"  /></kdb>

8. For the Response Payload, you need to paste an example of the Response that will be sent by the Weather API.

   You can find the expected API JSON Response on the API Documentation page [here](https://openweathermap.org/current#zip).

   Or you can copy the JSON Response from here:

   ```json
   {
     "coord": { "lon": -122.08, "lat": 37.39 },
     "weather": [
       {
         "id": 800,
         "main": "Clear",
         "description": "clear sky",
         "icon": "01d"
       }
     ],
     "base": "stations",
     "main": {
       "temp": 282.55,
       "feels_like": 281.86,
       "temp_min": 280.37,
       "temp_max": 284.26,
       "pressure": 1023,
       "humidity": 100
     },
     "visibility": 16093,
     "wind": {
       "speed": 1.5,
       "deg": 350
     },
     "clouds": {
       "all": 1
     },
     "dt": 1560350645,
     "sys": {
       "type": 1,
       "id": 5122,
       "message": 0.0139,
       "country": "US",
       "sunrise": 1560343627,
       "sunset": 1560396563
     },
     "timezone": -25200,
     "id": 420006353,
     "name": "Mountain View",
     "cod": 200
   }
   ```

9. Click the `Edit Payload`-icon.

     <!---
     ![Demo](./images/owmapi2.png)
     --->

   <kbd><img src="./images/owmapi2.png"  /></kdb>

   You'll see a popup where you now have to paste the above JSON Reponse.

   ![Demo](./images/owmapi3.png)

   Paste your JSON Response.

   ![Demo](./images/owmapi4.png)

10. Click `Save`.

    ![Demo](./images/dssave.png)

    Your custom Data Source configuration is now complete. Scroll up and click `Save`.

      <!---
      ![Demo](./images/dssave2.png)
      --->

    <kbd><img src="./images/dssave2.png"  /></kdb>

    Your Data Source has now been created successfully and is part of the `Data Sources`-list.

      <!---
      ![Demo](./images/dslist.png)
      --->

    <kbd><img src="./images/dslist.png"  /></kdb>

Next Step: [Exercise 3 - Define a Custom Action](./Exercise3-Action.md)

```

```
