Flights API
An API to find flights based on departure date, departure airport code and arrival airport code. This API returns a list of flights with details about the flights, seats and price information.
API calls are secured with a JWT token. User logs into Cognito Hosted UI to get the JWT Token and passes the token in the Authorization HTTP header.
API verifies the JWT token and then allows the requested action to be performed.
API interacts with flight and airport tables in RDS MySQL database to get the results. RDS credentials are stored securely in AWS Secret Manager.

API returns the following fields:
Flight Id, Departure, Departure, Departure AirportCode, Departure Airport Name, departure Airport City, Departure Airport Locale Arrival Airport Code,
Arrival Airport Name, Arrival Airport City, Arrival Airport Locale, Arrival Date, Arrival Time, Ticket Price Ticket Currency, Flight Number, Flight Duration; Seat Available
Database for this module has 2 tables:
Airport table - stores the details of the Airport with Airport Code as primary key and associated airport details. Flight table - stores the inventory of flights with their schedule, capacity and seat availability.
Technical Frameworks: Java 15, Spring Boot, Lombok, Spring Data JPA, AWS SDK V2 for Cognito and Secrets Manager integration
