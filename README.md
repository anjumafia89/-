# Api testing using Postman:Restful-Booker.
This repository contains a Postman collection and environment setup for testing the Restful Booker API. The API provides basic functionality for managing hotel bookings.

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

  ![image](https://github.com/user-attachments/assets/b3810678-4a17-4356-903b-a9c645a95a10)

<h2>Restful Booker Monitoring Report</h2>

![image](https://github.com/user-attachments/assets/a961a06c-1035-46ff-b039-156e596d3a7e)

<h2>Newman Report html</h2>


<h3>Run command :  </h3>            
      
              npm install -g newman 
              npm install -g newman-reporter-html
              newman run RestfulBooker.postman_collection.json -e BookerENV.postman_environment.json -r cli,html
             
![image](https://github.com/user-attachments/assets/f1f7f903-1f94-41b9-a6f1-fda645061f66)

<h2>Newman Report htmlextra</h2>

once newman is install there is no need to install newman again.
              
              npm install -g newman-reporter-htmlextra
              newman run RestfulBooker.postman_collection.json -e BookerENV.postman_environment.json -r cli,htmlextra
              
![image](https://github.com/user-attachments/assets/1abc963b-ee5b-45fc-b1eb-fa4fe37b9987)
