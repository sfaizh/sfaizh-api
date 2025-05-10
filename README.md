# Backend API for blogs

A lightweight Node.js RESTful API designed for blog management, with user authentication, and post handling. Dockerized for easy deployment.

## Features

- JWT-based authentication
- Blog CRUD operations
- User management
- Swagger documentation (`api/swagger.json`)
- JSON-based data storage for posts
- Docker and Docker Compose support

## Getting Started

### Prerequisites

- Node.js (v14 or newer)
- Docker & Docker Compose (for containerized setup)
- MongoDB (if running outside Docker)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/sfaizh-api.git
   cd sfaizh-api-main
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Create an `.env` file in the root directory with the following:**
   ```env
   PORT=3000
   JWT_SECRET=your_jwt_secret
   DB_URL=Your_mongodb_endpoint
   ```

4. **Start the server:**
   ```bash
   npm start
   ```

### Running with Docker

To build and run the project using Docker:

```bash
docker compose up --build
```

This will start the API along with any services defined in `compose.yaml`.

## Project Structure

```
sfaizh-api-main/
├── api/
│   └── swagger.json          # Swagger API documentation
├── config/
│   └── dbConn.js             # MongoDB connection setup
├── controllers/
│   ├── authController.js     # Auth logic
│   ├── blogsController.js    # Blog CRUD logic
│   └── usersController.js    # User management
├── data/
│   └── json/                 # Static blog post data
├── logs/
│   └── events.log            # Event logs
├── index.js                  # Main application entry point
├── Dockerfile                # Docker setup
├── compose.yaml              # Docker Compose config
├── package.json              # Project dependencies
└── README.md                 # Project info
```
