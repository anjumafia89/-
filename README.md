# Api test using Postman:Restful-Booker.
This repository contains a Postman collection and environment setup for testing the Restful Booker API. The API provides basic functionality for managing hotel bookings.
🔧 Here's what I worked on:
* Designed and organized test collections in Postman.
* Used Collection Runner for executing automated tests.
* Wrote JavaScript-based test scripts to validate:
  
    1.HTTP status codes
    2. JSON responses
    3.Auth token handling
    4.CRUD operations (GET, POST, PUT, DELETE)
   

<h3>Contents:</h3>
                                   
        RestfulBooker.postman_collection.json: A Postman collection with pre-configured requests for all major API endpoints.
        
        BookerENV.postman_environment.json: An environment file for use with Postman, containing variables like base URL and authentication token.

<h2>API Endpoints Covered</h2>

The collection includes requests for the following endpoints:

    1.GET /booking: Retrieve all booking IDs.
    2.GET /booking/{id}: Retrieve a specific booking.
    3.POST /booking: Create a new booking.
    4.PUT /booking/{id}: Update a booking (requires authentication).
    5.PATCH /booking/{id}: Partially update a booking.
    6.DELETE /booking/{id}: Delete a booking (requires authentication).
    7.POST /auth: Generate a token for authentication.
    8.GET /ping: Health check endpoint.

<h2>Environment Variables</h2>

<b>The BookerENV environment file includes:</b>

![image](https://github.com/user-attachments/assets/f276c4b1-6f9f-4fcc-a17b-9b46343008ff)


<h2>Restful Booker Monitoring Report</h2>

![image](https://github.com/user-attachments/assets/6e242bd0-b72c-4875-b8aa-8cf5f869db4f)



<h2>Newman Report html</h2>


<h3>Run command :  </h3>            
      
              npm install -g newman 
              npm install -g newman-reporter-html
              newman run RestfulBooker.postman_collection.json -e BookerENV.postman_environment.json -r cli,html
             
![image](https://github.com/user-attachments/assets/d83f492e-9acf-4215-bd71-ada12817fde8)


<h2>Newman Report htmlextra</h2>

once newman is install there is no need to install newman again.
              
              npm install -g newman-reporter-htmlextra
              newman run RestfulBooker.postman_collection.json -e BookerENV.postman_environment.json -r cli,htmlextra
              
![image](https://github.com/user-attachments/assets/d7da4ea6-e29c-46b4-bfe5-e2443b2bfe61)

