{
  "info": {
    "_postman_id": "frontend-intern-assignment-001",
    "name": "Frontend Intern Assignment APIs",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
  },
  "item": [
    {
      "name": "Signup User",
      "request": {
        "method": "POST",
        "header": [{ "key": "Content-Type", "value": "application/json" }],
        "body": {
          "mode": "raw",
          "raw": "{\n  \"name\": \"John Doe\",\n  \"email\": \"john@example.com\",\n  \"password\": \"123456\"\n}"
        },
        "url": { "raw": "http://127.0.0.1:8000/api/signup", "protocol": "http", "host": ["127.0.0.1"], "port": "8000", "path": ["api", "signup"] }
      }
    },
    {
      "name": "Login User",
      "request": {
        "method": "POST",
        "header": [{ "key": "Content-Type", "value": "application/json" }],
        "body": {
          "mode": "raw",
          "raw": "{\n  \"email\": \"john@example.com\",\n  \"password\": \"123456\"\n}"
        },
        "url": { "raw": "http://127.0.0.1:8000/api/login", "protocol": "http", "host": ["127.0.0.1"], "port": "8000", "path": ["api", "login"] }
      }
    },
    {
      "name": "Get Profile",
      "request": {
        "method": "GET",
        "header": [{ "key": "Authorization", "value": "Bearer {{JWT_TOKEN}}" }],
        "url": { "raw": "http://127.0.0.1:8000/api/profile", "protocol": "http", "host": ["127.0.0.1"], "port": "8000", "path": ["api", "profile"] }
      }
    },
    {
      "name": "Update Profile",
      "request": {
        "method": "PUT",
        "header": [
          { "key": "Authorization", "value": "Bearer {{JWT_TOKEN}}" },
          { "key": "Content-Type", "value": "application/json" }
        ],
        "body": {
          "mode": "raw",
          "raw": "{\n  \"name\": \"John Updated\",\n  \"email\": \"john.updated@example.com\"\n}"
        },
        "url": { "raw": "http://127.0.0.1:8000/api/profile", "protocol": "http", "host": ["127.0.0.1"], "port": "8000", "path": ["api", "profile"] }
      }
    },
    {
      "name": "Tasks CRUD",
      "item": [
        {
          "name": "Get All Tasks",
          "request": {
            "method": "GET",
            "header": [{ "key": "Authorization", "value": "Bearer {{JWT_TOKEN}}" }],
            "url": { "raw": "http://127.0.0.1:8000/api/tasks", "protocol": "http", "host": ["127.0.0.1"], "port": "8000", "path": ["api", "tasks"] }
          }
        },
        {
          "name": "Create Task",
          "request": {
            "method": "POST",
            "header": [
              { "key": "Authorization", "value": "Bearer {{JWT_TOKEN}}" },
              { "key": "Content-Type", "value": "application/json" }
            ],
            "body": {
              "mode": "raw",
              "raw": "{\n  \"title\": \"Sample Task\",\n  \"description\": \"This is a test task.\"\n}"
            },
            "url": { "raw": "http://127.0.0.1:8000/api/tasks", "protocol": "http", "host": ["127.0.0.1"], "port": "8000", "path": ["api", "tasks"] }
          }
        },
        {
          "name": "Update Task",
          "request": {
            "method": "PUT",
            "header": [
              { "key": "Authorization", "value": "Bearer {{JWT_TOKEN}}" },
              { "key": "Content-Type", "value": "application/json" }
            ],
            "body": {
              "mode": "raw",
              "raw": "{\n  \"title\": \"Updated Task\",\n  \"description\": \"Updated description.\"\n}"
            },
            "url": { "raw": "http://127.0.0.1:8000/api/tasks/{{TASK_ID}}", "protocol": "http", "host": ["127.0.0.1"], "port": "8000", "path": ["api", "tasks", "{{TASK_ID}}"] }
          }
        },
        {
          "name": "Delete Task",
          "request": {
            "method": "DELETE",
            "header": [{ "key": "Authorization", "value": "Bearer {{JWT_TOKEN}}" }],
            "url": { "raw": "http://127.0.0.1:8000/api/tasks/{{TASK_ID}}", "protocol": "http", "host": ["127.0.0.1"], "port": "8000", "path": ["api", "tasks", "{{TASK_ID}}"] }
          }
        }
      ]
    }
  ]
}
