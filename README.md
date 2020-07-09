# routes-schedules-process-ws

## Introduction
This is an implementation for *Routes and Schedules Process API* which provides the capability to query location routes and the departure schedule from multiple transport providers. It calls different System APIs for different providers and combines their result to present a unified view of the Routes or Schedules available.

## API Details
More about *Routes and Schedules Process API* can be found at https://anypoint.mulesoft.com/exchange/portals/scrollwell/4c4287b2-7066-4b83-864f-60985a79247e/routes-and-schedules-process-api/

## Some Implementation Details
1. Currently there are no secutiry requirements for this API hence its not secured
2. Current transport providers are First Coach and Transnational.
3. FirstCoach Routes API requires Basic Authentication, password for which has been configured and secured using Mulesoft's standard procedure for securing properties
4. For securing properties:
    a. Algorithm = Blowfish 
    b. Mode = CBC 
   
   **NOTE:** Above details are according to FirstBooking's Organizational Security Policy and has been advised by the IT Security Team

## Running and Testing the project
To run the application from Anypoint Studio perform the following steps:

1. Fetch the project from Github
2. Edit Run Configurations to provide an environment variables: 
    a. env = dev
    b. securityKey = fbdevseckey
   
   **NOTE:** For securityKey for other controlled environments please contact the IT Operations Team
   
3. Run the configuration
4. Extract the Postman collection and environment files from *src/test/resources/postman*
5. Import the Postman collection and environment files in Postman
6. Select *firstbooking-dev* and invoke the requests
