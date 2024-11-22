# Fastapi-project
## Learning Fastapi
### TodoApp 

#### Project Overview
This FastAPI application manages lists of Todos of users. The API includes endpoints for creating, reading, updating, and deleting todos, as well as user authentication and administrative controls.

##### Endpoints
1. Health Check
GET /healthy: Simple endpoint to verify the API is running.

2. Read All Todos
GET /: Returns a list of all todos.

3. To Read,Update,Delete,Create Todo 
Read Todo: GET /todo/{todo_id} - Retrieve a todo item by ID.
Update Todo: PUT /todo/{todo_id} - Update a todo item by ID.
Delete Todo: DELETE /todo/{todo_id} - Delete a todo item by ID.
Create Todo: POST /todo - Create a new todo item.

4. Authentication (auth)
User Registration
POST /auth/: Register a new user.
Login and Token
POST /auth/token: Authenticate a user and return an access token.

5. Admin Routes (admin)
Admin Read All Todos
GET /admin/todo: Admin-only access to retrieve all todos.
Admin Delete Todo
DELETE /admin/todo/{todo_id}: Admin-only access to delete a specific todo by ID.

6. User Routes (user)
GET /user/: Retrieve information about the authenticated user.
Update User Password
Description: Get User Information

PUT /user/password: Update the password of the authenticated user.
Update User Phone Number

PUT /user/phonenumber/{phone_number}: Update the phone number for the authenticated user.

###### Installation and Setup
1. In order to run this app locally you have to install
FastAPI: pip install fastapi
uvicorn: pip install uvicorn
SqlAlchemy: pip install sqlalchemy
Alembic: pip install alembic
jose: pip install python-jose ; for encoding and decoding JWTs
passlib: pip install passlib[bcrypt] ;  for password hashing
pytest: pip install pytest

2. To run the application, start the server on your terminal with "uvicorn main:app --reload" and ensure your fastapi environment is activated
 For Windows run fastapienv/Scripts/activate.bat to activate your environment
 For mac run source fastapienv/bin/activate to activate your environment
3. To access the API Documentation, Visit the URL provided on your terminal after running the application to view and interact with the API documentation.



