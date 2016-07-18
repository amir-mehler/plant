# plant

Hi!

 - Here you can find the static html example I did with the template
 - If you can run it and view [production/index.html] in your browser then you will see the mock
 - I will now describe the specifications and API calls (I'll try to keep it simple)
   - Sidebar: I need the Welcome div, Home menu and 'Production-US' underneath
   - Body:
     - 5 Numerical values
       - Titles: MAU, Registerd Devices, Companies in Production, Active Trials, Active Inserts, Applications
       - Please use the font-awesome icons I used
       - All numbers can be grey
       - Remove the '^ 4% From last week' titles
       - All values will be returned in one json with this API call
       ```sh
       $ http https://92g6bt7bib.execute-api.us-east-1.amazonaws.com/dev/scalars
       HTTP/1.1 200 OK
       Connection: keep-alive
       Content-Length: 138
       Content-Type: application/json
       Date: Mon, 18 Jul 2016 17:23:06 GMT
       Via: 1.1 55bf5f93fad6af1fd2ee6a7f298862b0.cloudfront.net (CloudFront)
       X-Amz-Cf-Id: szbV5O6OE3F08uLPujHXoCpwbV4W7b_uMRvyzUDKNxVXQ0a1nELafg==
       X-Cache: Miss from cloudfront
       x-amzn-RequestId: 4a68632e-4d0c-11e6-9861-053b5758d320

       {
           "active-inserts": 148,
           "active-trials": 47,
           "applications": 25,
           "companies-in-production": 12,
           "mau": 27048,
           "registered-devices": 25947
      }
```

[this file]: <https://github.com/amir-mehler/plant/blob/master/example-with-template/production/index.html>
