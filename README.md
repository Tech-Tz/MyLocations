The code for the solution has been pushed for the web app named MyLocations.

It is a basic app for viewing location images. We can also search for new locations online using Foursquare api and Flickr api.

![alt text](https://github.com/Tech-Tz/MyLocations/blob/main/Docs%20images/1.png)

You can search and filter for existing location images using a keyword in the database as shown below.

![alt text](https://github.com/Tech-Tz/MyLocations/blob/main/Docs%20images/2.png)

If a location does not exists in the db, you can search for that location online as shown below.

![alt text](https://github.com/Tech-Tz/MyLocations/blob/main/Docs%20images/3.png)

Once you are redirected to the search page, you can enter a keyword for that location, the region and the category.

![alt text](https://github.com/Tech-Tz/MyLocations/blob/main/Docs%20images/4.png)

A location will contain up to N images. The images will be added only if they do not already exist in the db. An image may also be associated with M locations. Therefore, there is many-to-many relationship with Locations and Images.

Tech-stack:

Asp.Net Core Mvc
.NET 8
JQuery 3.6.0
Bootstrap 5.2.0
SQL Server 2016
Kindly follow steps below to run the app:

Modify db connection string in src/MyLocations.Web/appSettings.json
Insert your foursquare api key and flickr api key and api secret in the in src/DBCreationScript.sql

![alt text](https://github.com/Tech-Tz/MyLocations/blob/main/Docs%20images/5.png)

We preferred implementing code for calling the foursquare and flickr apis directly in the solution instead of using nuget packages as these packages are outdated. There is also a security risk of passing api keys to the methods provided by the nuget packages.

Future improvements:

- Asp.net core mvc framework was intially chosen. We can implement the back end using asp.net core web api and the front end with a JS framework for example Angular.
- Add unit tests
- Fine tune the searching of locations/images with foursquare and flickr api by further experimentation on the number and type of parameters passed to the api endpoints.
- Use information obtained from Places Api endpoints in foursquare to input in Personalisation Api endpoints in foursquare for customizing user experience.
- Instead of displaying the individual images in the page, we can display the locations. When we click on a location, we can navigate through the list of images of that location.
- Passing a list of categories instead of only one category when searching for a location.
- Real time search in javascript for searching locations in DB
- Implement authentication and user defined list of locations
