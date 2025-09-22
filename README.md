# LittleTiers

A Node.js learning project for building a simple blog/post management system using Express.js and LowDB.

## Overview

LittleTiers is a hands-on educational project designed to teach the fundamentals of:
- Node.js backend development
- Express.js web framework
- Database operations with LowDB (file-based JSON database)
- RESTful API design
- Frontend-backend integration

This project contains skeleton code with placeholders marked as `// YOUR CODE` that students need to implement.

## Features

The completed application will provide:
- ✅ Basic post management (create, read, update, delete)
- ✅ Post publishing/unpublishing functionality
- ✅ Simple web interface to interact with posts
- ✅ RESTful API endpoints for all operations

## Prerequisites

- Node.js (version 12 or higher)
- npm (Node Package Manager)
- Basic knowledge of JavaScript
- Understanding of HTTP methods and REST APIs

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Arazguly/littletiers.git
cd littletiers
```

2. Install dependencies:
```bash
npm install
```

## Project Structure

```
littletiers/
├── README.md           # This file
├── package.json        # Project dependencies and scripts
├── http_server.js      # Main Express.js server (skeleton)
├── simple.js           # Basic LowDB operations (skeleton)
├── public/
│   └── index.html      # Frontend interface
└── db.json             # Database file (created automatically)
```

## Learning Exercises

### 1. Simple Database Operations (`simple.js`)

Complete the following functions to learn basic database operations:
- Initialize the data store
- Add posts to the database
- Count total posts
- Find posts by ID
- Filter posts by published status

### 2. HTTP Server Setup (`http_server.js`)

Implement the Express.js server with the following components:
- Set up Express application
- Configure static file serving
- Implement API endpoints

### 3. API Endpoints

Complete these REST API endpoints:

#### GET `/data`
Return all posts from the database

#### GET `/posts/:title/:id/:published`
Add a new post with the given title, id, and published status
- Example: `curl http://localhost:3000/posts/ping/1/false`

#### GET `/published/:boolean`
Filter posts by published status (true/false)
- Example: `curl http://localhost:3000/published/true`

#### GET `/published/:id/:boolean`
Update the published status of a specific post
- Example: `curl http://localhost:3000/published/1/true`

#### GET `/delete/:id`
Delete a post by its ID
- Example: `curl http://localhost:3000/delete/5`

### 4. Frontend Integration (`public/index.html`)

Complete the JavaScript code to:
- Handle API responses
- Display data in the browser
- Provide user feedback

## Usage

### Running the Server

1. Complete the skeleton code in `http_server.js`
2. Start the server:
```bash
node http_server.js
```
3. Open your browser and navigate to `http://localhost:3000`

### Testing the API

Use curl commands to test your implementation:

```bash
# Add a post
curl http://localhost:3000/posts/hello-world/1/true

# Get all posts
curl http://localhost:3000/data

# Filter published posts
curl http://localhost:3000/published/true

# Update post status
curl http://localhost:3000/published/1/false

# Delete a post
curl http://localhost:3000/delete/1
```

### Testing Database Operations

Run the simple database operations:
```bash
node simple.js
```

## Data Structure

Posts are stored with the following structure:
```json
{
  "posts": [
    {
      "id": "1",
      "title": "Sample Post",
      "published": true
    }
  ]
}
```

## Troubleshooting

### Common Issues

1. **Port already in use**: Change the port number in your server code
2. **Dependencies not installed**: Run `npm install`
3. **Database file missing**: The `db.json` file is created automatically
4. **API not responding**: Ensure the Express server is properly configured

### Tips

- Use `console.log()` to debug your code
- Check the browser's developer console for errors
- Verify your API endpoints with tools like Postman or curl
- Make sure your Express routes are properly defined

## Dependencies

- **express**: Web framework for Node.js
- **lowdb**: Simple file-based JSON database

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Contributing

This is an educational project. Feel free to:
- Report issues
- Suggest improvements
- Share your completed solutions
- Create additional exercises

## Learning Resources

- [Express.js Documentation](https://expressjs.com/)
- [LowDB Documentation](https://github.com/typicode/lowdb)
- [Node.js Documentation](https://nodejs.org/docs/)
- [RESTful API Design](https://restfulapi.net/)
