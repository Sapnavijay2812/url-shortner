# URL Shortener

## Description
This project is a fully functional URL shortener built from scratch using **Node.js**, **Express**, and **MongoDB**. The application allows users to shorten long URLs and retrieve them later using a unique shortened identifier. This project aims to provide a lightweight solution for managing shortened URLs with a simple interface.

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Database Schema](#database-schema)
- [License](#license)
- [Contributing](#contributing)
- [Acknowledgments](#acknowledgments)

## Features
- Shorten long URLs
- Redirect to the original URL when the shortened URL is accessed
- View all shortened URLs in a list
- Basic error handling for invalid URLs and duplicate entries
- User-friendly interface for inputting URLs

## Tech Stack
- **Node.js**: JavaScript runtime for building server-side applications
- **Express**: Web framework for Node.js for handling HTTP requests
- **MongoDB**: NoSQL database for storing shortened URLs and their original counterparts
- **Mongoose**: ODM (Object Data Modeling) library for MongoDB and Node.js
- **dotenv**: Module for loading environment variables from a `.env` file

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/url-shortener.git
   cd url-shortener
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up MongoDB:**
   - Ensure you have [MongoDB](https://www.mongodb.com/try/download/community) installed and running on your machine.
   - Create a database named `url_shortener`.

4. **Configure environment variables:**
   - Create a `.env` file in the root directory and add your MongoDB connection string:
     ```plaintext
     MONGODB_URI=mongodb://localhost:27017/url_shortener
     ```

5. **Start the server:**
   ```bash
   npm start
   ```

## Usage
- Open a web browser and navigate to `http://localhost:3000` to access the application.
- Enter a long URL into the input field and click the "Shorten" button.
- The application will return a shortened URL that you can click to be redirected to the original URL.
- To view all shortened URLs, navigate to `/urls`.

## API Endpoints
| Method | Endpoint           | Description                          |
|--------|--------------------|--------------------------------------|
| POST   | `/shorten`         | Shortens a long URL                 |
| GET    | `/:shortenedId`    | Redirects to the original URL       |
| GET    | `/urls`            | Retrieves all shortened URLs         |

### Request Example for Shortening a URL
To shorten a URL, send a POST request to `/shorten` with a JSON body:
```json
{
  "url": "https://www.example.com"
}
```

### Response Example
```json
{
  "shortenedUrl": "http://localhost:3000/abc123"
}
```

## Database Schema
The application uses a MongoDB collection called `urls` to store the following information:
- **originalUrl**: The original long URL (String)
- **shortenedId**: The unique identifier for the shortened URL (String)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or suggestions. 

## Acknowledgments
- Inspired by various URL shortening services.
- Special thanks to the Node.js, Express, and MongoDB documentation for guidance.
