# Student Management REST API

## Project Overview

The Student Management REST API is a backend application developed using Node.js and Express.js. It provides RESTful API endpoints to manage student records through HTTP requests.

The project demonstrates backend development concepts, including API routing, CRUD operations, JSON data handling, input validation, error handling, and API testing using Postman.

## Objectives

- Understand the fundamentals of backend development.
- Create a REST API using Node.js and Express.js.
- Handle HTTP requests and responses.
- Implement CRUD operations for student records.
- Validate incoming data and handle errors.
- Test API endpoints using Postman.

## Technologies Used

- **Node.js** – JavaScript runtime for backend development.
- **Express.js** – Framework for creating API routes and handling HTTP requests.
- **Postman** – Tool for testing API endpoints.
- **JSON** – Format used for sending and receiving data.

## Project Structure

```text
student-api/
├── node_modules/
├── package.json
├── package-lock.json
├── server.js
└── README.md
```

## Prerequisites

Install the following software before running the project:

1. [Node.js](https://nodejs.org/)
2. [Visual Studio Code](https://code.visualstudio.com/)
3. [Postman](https://www.postman.com/downloads/)

## Installation and Setup

### Step 1: Create the project directory

Open the VS Code terminal and run:

```bash
mkdir student-api
cd student-api
```

If you have already created the project folder, open its terminal directly instead.

### Step 2: Initialize the project

```bash
npm init -y
```

This creates the `package.json` file.

### Step 3: Install Express.js

```bash
npm install express
```

### Step 4: Create the server

Create a file named `server.js` and add the Student Management API code.

### Step 5: Start the server

Run the following command from the project directory:

```bash
node server.js
```

The server should display:

```text
Server running at http://localhost:3000
```

The API is now ready to receive requests.

## API Endpoints

Base URL: `http://localhost:3000`

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/api/students` | Retrieve all students |
| GET | `/api/students/:id` | Retrieve a student by ID |
| POST | `/api/students` | Add a new student |
| PUT | `/api/students/:id` | Update an existing student |
| DELETE | `/api/students/:id` | Delete a student by ID |

## Testing the API Using Postman

### 1. Retrieve all students

- Method: `GET`
- URL: `http://localhost:3000/api/students`
- Click **Send** to view the student records.

### 2. Retrieve a student by ID

- Method: `GET`
- URL: `http://localhost:3000/api/students/1`
- Click **Send** to retrieve the student with ID 1.

### 3. Add a new student

- Method: `POST`
- URL: `http://localhost:3000/api/students`
- Select **Body → raw → JSON**.
- Enter the following request body:

```json
{
  "name": "Siddhi",
  "course": "Full Stack Development"
}
```

Click **Send** to create the student record.

### 4. Update a student

- Method: `PUT`
- URL: `http://localhost:3000/api/students/1`
- Select **Body → raw → JSON**.
- Enter the updated details:

```json
{
  "name": "Aarav Sharma",
  "course": "Web Development"
}
```

Click **Send** to update the record.

### 5. Delete a student

- Method: `DELETE`
- URL: `http://localhost:3000/api/students/2`
- Click **Send** to delete the student with ID 2.

## HTTP Status Codes

| Status Code | Meaning |
|---|---|
| `200 OK` | Request completed successfully |
| `201 Created` | New student record created |
| `400 Bad Request` | Invalid input data |
| `404 Not Found` | Student or requested route not found |

## Data Storage

This project uses an in-memory JavaScript array to store student records. The data is temporary and is reset whenever the server restarts.

A database such as MySQL can be integrated in a future version to provide permanent data storage.

## Learning Outcomes

By completing this project, the following skills were practised:

- Setting up a Node.js backend project.
- Developing RESTful APIs with Express.js.
- Implementing Create, Read, Update, and Delete operations.
- Handling HTTP requests and JSON responses.
- Performing basic input validation.
- Managing common API errors.
- Testing backend functionality using Postman.

## Future Enhancements

- Integrate MySQL for persistent data storage.
- Add user authentication and authorization.
- Improve validation and centralized error handling.
- Implement automated API tests.
- Connect the API to a frontend application.

## Conclusion

The Student Management REST API provides practical experience in backend development using Node.js and Express.js. It demonstrates how REST endpoints handle client requests, perform operations on application data, and return structured responses. Postman is used to verify the functionality of the API endpoints.

**Project Type:** Backend Development Practice Project  
**Category:** REST API Development  
**Status:** Completed for learning and demonstration purposes
