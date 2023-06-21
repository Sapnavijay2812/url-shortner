# url-shortner

# Project Description
This project implements a basic search functionality for URLs and notes, allowing users to search for specific content within their stored URLs and notes. Additionally, it includes user authentication using JSON web tokens (JWT) to secure the system and ensure that sensitive user data is protected. The project aims to provide a convenient and secure way for users to search their saved URLs and notes.

# How to Run the Project
To run the project, follow the steps below:

1. Clone the project repository from GitHub.

2. Install the required dependencies:
Node.js (version X.X.X or higher)
MongoDB (version X.X.X or higher)
Express.js (version X.X.X or higher)
Mongoose (version X.X.X or higher)
JSON Web Token (JWT) (version X.X.X or higher)
Other dependencies (check the project's package.json file)
   
3. Set up the database:
Create a MongoDB database and obtain the connection URL.
Update the database connection URL in the project's configuration files.

4. Run the following commands in the project's root directory:
```
npm install
npm start
```
5. The project should now be running on your local machine. Access it via 'http://localhost:3000' or the specified port.

# Internal Working of the Project
The project's internal working can be divided into two main tasks:

# Task 1: Implementing Search Functionality
To implement the search functionality, different approaches can be considered:

Option 1: Retrieve all data and filter on the frontend (not recommended): This approach involves fetching all the data from the database and performing the filtering process on the client-side. However, this approach may result in performance issues, especially when dealing with large datasets.

Option 2: Classic query iteration: This approach involves querying the database and iterating through all the data to find the desired results. While it is a viable solution, it may not be efficient for large datasets.

Option 3: Mongo Atlas Search (recommended): This approach involves utilizing Mongo Atlas Search, which allows for efficient text-based search capabilities. By setting up search indexes, the search functionality can be optimized, providing faster and more accurate results.

For further enhancement, an auto-complete functionality can be implemented, which suggests search terms as the user types, providing a more intuitive user experience.

Internal Working of the Project
The project's internal working can be divided into two main tasks:

Task 1: Implementing Search Functionality
To implement the search functionality, different approaches can be considered:

Option 1: Retrieve all data and filter on the frontend (not recommended): This approach involves fetching all the data from the database and performing the filtering process on the client-side. However, this approach may result in performance issues, especially when dealing with large datasets.

Option 2: Classic query iteration: This approach involves querying the database and iterating through all the data to find the desired results. While it is a viable solution, it may not be efficient for large datasets.

Option 3: Mongo Atlas Search (recommended): This approach involves utilizing Mongo Atlas Search, which allows for efficient text-based search capabilities. By setting up search indexes, the search functionality can be optimized, providing faster and more accurate results.

For further enhancement, an auto-complete functionality can be implemented, which suggests search terms as the user types, providing a more intuitive user experience.

# Task 2: Implementing Authentication with JWT
To implement authentication using JSON web tokens, the following steps are typically involved:

User Registration:

Collect user registration details (e.g., username, email, password).
Hash the password using a secure hashing algorithm (e.g., bcrypt) and store the hashed password in the database.
Create a unique user identifier and generate a JWT containing the user identifier as a payload.
Send the JWT back to the client for future authenticated requests.
User Login:

Collect user login credentials (e.g., username, password).
Retrieve the user's hashed password from the database based on the provided username.
Compare the provided password with the hashed password using the same hashing algorithm.
If the passwords match, generate a new JWT containing the user identifier and send it back to the client.
Protecting Routes:

Implement middleware that verifies the JWT for protected routes.
When the client sends a request to a protected route, the middleware checks the validity of the JWT and allows or denies access accordingly.
By implementing these steps, the project ensures that only authenticated users can access certain routes and perform authorized actions.

# Learning Takeaways
While working on this project, you can expect to gain the following learning takeaways:

Understanding and implementing search functionality using different approaches.
Utilizing a NoSQL database (MongoDB) and leveraging its search capabilities.
Implementing user authentication using JSON web tokens (JWT) for securing the application.
Learning how to hash passwords securely to protect user data.
Building RESTful APIs and handling protected routes using middleware.


# Resources/References
During the development of this project, the following resources/references can be helpful:

MongoDB Documentation: https://docs.mongodb.com/
Express.js Documentation: https://expressjs.com/
Mongoose Documentation: https://mongoosejs.com/
JSON Web Token (JWT) Documentation: https://jwt.io/
bcrypt NPM Package: https://www.npmjs.com/package/bcrypt
Note: The specific versions of the dependencies and additional resources may vary based on your project's requirements and preferences.











