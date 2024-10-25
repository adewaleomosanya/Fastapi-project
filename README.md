# Fastapi-project
## Learning Fastapi
This project has two different projects in it 
1. books.py 
2. TodoApp
### books.py
### Project Overview
This API allows users to create, read, update, and delete books. Each book includes information such as title, author, description, rating, and published date.
#### Endpoints
Get All Books
URL: /books
Method: GET
Description: Retrieves a list of all books.

Get Book by ID
URL: /books/{book_id}
Method: GET
Description: Retrieves a specific book by its ID.
Path Parameter: book_id (integer, required, greater than 0)

Get Books by Rating
URL: /books/
Method: GET
Query Parameter: book_rating (integer between 1 and 5)
Description: Returns books with the specified rating.

Get Books by Published Date
URL: /books/publish/
Method: GET
Query Parameter: published_date (integer between 2000 and 2030)
Description: Retrieves books published in a specific year.

Create a New Book
URL: /create-book
Method: POST
Body: JSON object containing title, author, description, rating (1-5), and published date (2000-2030).
Description: Adds a new book to the collection.

Update a Book
URL: /books/update_book
Method: PUT
Body: JSON object with updated fields.
Description: Updates an existing book's information.

Delete a Book
URL: /books/{book_id}
Method: DELETE
Path Parameter: book_id (integer, required, greater than 0)
Description: Deletes a book from the collection.

##### Installaion and Setup
1. Ensure you have FASTAPI and Uvicorn installed and create a fastapi environment
pip install fastapi 
pip install uvicorn
create the fastapi environment with : python3 -m venv fastapienv
2. To run the application, start the server on your terminal with "uvicorn books2:app --reload" and ensure your fastapi environment is activated
 For Windows run fastapienv/Scripts/activate.bat to activate your environment
 For mac run source fastapienv/bin/activate to activate your environment
3. To access the API Documentation, Visit the URL provided on your terminal after running the application to view and interact with the API documentation.

###### TodoApp 

###### Project Overview
This FastAPI application manages lists of Todos of users. The API includes endpoints for creating, reading, updating, and deleting todos, as well as user authentication and administrative controls.

###### Endpoints
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

###### Installaion and Setup
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



