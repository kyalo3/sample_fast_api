# FastAPI Recipients API
- This is a FastAPI application that provides an API for managing recipients. The API allows you to create, read, update, and delete recipients.

*Endpoints*

- 1. GET /
Description: Returns a welcome message.
Response: {"name": "First Data"}
GET /get-recipient/{recipient_id}
Description: Retrieves a recipient by ID.
Path Parameters:
recipient_id (int): The ID of the recipient to retrieve.
Response: The recipient object or {"Data": "Not Found"} if the recipient is not found.
- 2. GET /get-by-name
Description: Retrieves a recipient by name.
Query Parameters:
recipient_id (int): The ID of the recipient.
name (str, optional): The name of the recipient to search for.
test (int): A test parameter.
Response: The recipient object or {"Data": "Not Found"} if the recipient is not found.
- 3. POST /create-recipient/{recipient_id}
Description: Creates a new recipient.
Path Parameters:
recipient_id (int): The ID of the recipient to create.
Request Body: A Recipient object.
Response: The created recipient object or {"Error": "Recipient ID already exists"} if the recipient ID already exists.

- 4. PUT /update-recipient/{recipient_id}
Description: Updates an existing recipient.
Path Parameters:
recipient_id (int): The ID of the recipient to update.
Request Body: A Recipient object with the updated fields.
Response: The updated recipient object or {"Error": "Recipient ID does not exist"} if the recipient ID does not exist.

- 5. DELETE /delete-recipient/{recipient_id}
Description: Deletes a recipient.
Path Parameters:
recipient_id (int): The ID of the recipient to delete.
Response: {"Message": "Recipient deleted successfully"} or {"Error": "Recipient ID does not exist"} if the recipient ID does not exist.

*Models*
*Recipient*

name (str): The name of the recipient.
age (int): The age of the recipient.
id (int): The ID of the recipient.

*UpdateRecipient*
name (str, optional): The updated name of the recipient.
age (int, optional): The updated age of the recipient.
id (int, optional): The updated ID of the recipient.

*Running the Application*
Install the required dependencies:
bash
pip install fastapi uvicorn

uvicorn --
Run the application:
bash

*uvicorn myapi:app --reload*

Access the API at http://localhost:8000
*Documentation*
The API documentation is automatically generated using Swagger UI and can be accessed at http://localhost:8000/docs.
