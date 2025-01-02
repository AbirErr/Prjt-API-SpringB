Unique Task Manager API
Requirements

- Java JDK 17+
- Maven
- MySQL (8.x or higher)
- IDE (like IntelliJ IDEA or Eclipse)
- Postman (optional, for testing API endpoints)

Setup

1. Clone or Download the project.
2. Database Setup:
   - Open MySQL and run:
     CREATE DATABASE uniquetasksdb;
   - Update your MySQL username and password in src/main/resources/application.properties:
     spring.datasource.username=YOUR_USERNAME
     spring.datasource.password=YOUR_PASSWORD
3. Build the Project:
   - Open a terminal in the project folder and run:
     mvn clean install

Run the Application

1. Start the application:
   mvn spring-boot:run
2. The API will be available at:
   http://localhost:8080/tasks/api

Endpoints

Base URL: /tasks/api


1. Get All Tasks
   - GET /
   - Returns a list of tasks.

2. Get Task by ID
   - GET /{taskId}
   - Returns a specific task.

3. Create a New Task
   - POST /
   - Example Body:
     {
       "taskTitle": "New Task",
       "taskDescription": "Task description",
       "taskCompleted": false
     }

4. Update a Task
   - PUT /{taskId}
   - Example Body:
     {
       "taskTitle": "Updated Task",
       "taskDescription": "Updated description",
       "taskCompleted": true
     }

5. Delete a Task
   - DELETE /{taskId}

Test the API

- Use Postman or a browser to test the endpoints.
- For example:
  - Get All Tasks:
    Open: http://localhost:8080/tasks/api in a browser.

Technologies Used

- Spring Boot
- MySQL
- Maven
- Java
