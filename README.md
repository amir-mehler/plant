# plant

Hi!

 - Here you can find the static html example I did with the template
 - If you can run it and view production/index.html [here] in your browser then you will see the mock
 - I will now describe the specifications and API calls (I'll try to keep it simple)
   - **Sidebar**: I need the Welcome div, Home menu and 'Production-US' underneath, which is the home page.
   - **Body**:
     - 5 Numerical values (each should take a fith of the width)
       - Titles: MAU, Registerd Devices, Companies in Production, Active Trials, Active Inserts, Applications
       - Please use the font-awesome icons I used
       - All numbers can be grey
       - Remove the '^ 4% From last week' titles
       - All values will be returned in one json with this API GET call
       ```sh
       $ http https://92g6bt7bib.execute-api.us-east-1.amazonaws.com/dev/scalars
       {
           "active-inserts": 148,
           "active-trials": 47,
           "applications": 25,
           "companies-in-production": 12,
           "mau": 27048,
           "registered-devices": 25947
      }
```
   - **Three "Top 5" graphs**:
     - Each should take a third of the width
     - Device Types Doughnut graph gets unsorted data, key and value json. Keep title and subtitle: 'Device Types' and 'top 5'. No need for the 'Device/Progress' text.
     - SDK Versions bars, key and value json, data **needs** to be sorted. Title 'Top SDK Versions'. No need for subtitle.
     - Insert Types Doughnut graph - same as 'Device Types'
     - API Calls (GET):
     ```sh

     $ http https://92g6bt7bib.execute-api.us-east-1.amazonaws.com/dev/top5-device-types
     {
         "Android": 55,
         "Blackberry": 5,
         "Symbian": 10,
         "WindowsPhone": 5,
         "iOS": 25
     }

     $ http https://92g6bt7bib.execute-api.us-east-1.amazonaws.com/dev/top5-sdk-versions
     {
         "1.28.1.1": 50,
         "1.29.0.0": 100,
         "1.30.0.0": 250,
         "1.31.0.0": 25000,
         "1.31.1.0": 5000
     }

     $ http https://92g6bt7bib.execute-api.us-east-1.amazonaws.com/dev/top5-insert-types
     {
         "Combo": 25,
         "Coupon": 30,
         "Encourage Upgrade": 20,
         "Modify Text": "15",
         "One Questions Survey": 10
     }
```

   - **Two Time Series Graphs**
     - Each graph should take half of the width
     - Each graph will have just one data area
     - The data returned from the API will include a **sorted array** starting from the present day moving backwards
     - API Calls (GET):
     ```sh
     $ http https://92g6bt7bib.execute-api.us-east-1.amazonaws.com/dev/total-impressions-last-7-days
     {
       "array": [
         {
           "Wed": 710
         },
         {
           "Tue": 830
         },
         {
           "Mon": 532
         },
         {
           "Sun": 650
         },
         {
           "Sat": 329
         },
         {
           "Fri": 990
         },
         {
           "Thu": 430
         }
       ]
     }

     $ http https://92g6bt7bib.execute-api.us-east-1.amazonaws.com/dev/total-push-sent-last-7-days
     {
       "array": [
         {
           "Wed": 250
         },
         {
           "Tue": 800
         },
         {
           "Mon": 120
         },
         {
           "Sun": 1200
         },
         {
           "Sat": 300
         },
         {
           "Fri": 900
         },
         {
           "Thu": 400
         }
       ]
     }
```

 - **Thats it!**

Thank you very much - you can always reach me through amir@insert.io

[here]: <https://github.com/amir-mehler/plant/blob/master/example-with-template/production/index.html>
