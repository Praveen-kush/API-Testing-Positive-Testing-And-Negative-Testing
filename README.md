✅ Positive Test Cases

#	Method	Endpoint	Description
1	GET	/api/users?page=2	Fetches a list of users
2	GET	/api/users/2	Retrieves a single user by ID
3	POST	/api/users	Creates a user with valid payload
4	PUT	/api/users/2	Updates an existing user
5	PATCH	/api/users/2	Partially updates a user
6	DELETE	/api/users/2	Deletes a user
7	POST	/api/register	Registers a user with valid credentials
8	POST	/api/login	Logs in a user with valid credentials
❌ Negative Test Cases

#	Method	Endpoint	Description
1	GET	/api/users/999	Fetch non-existent user – expect 404
2	POST	/api/users	Missing fields in body – expect 400
3	POST	/api/register	Missing password – expect validation error
4	POST	/api/login	Missing credentials – expect error message
5	GET	/api/unknown/23	Invalid resource – expect 404 Not Found
🚀 Getting Started
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/reqres-api-testing.git
cd reqres-api-testing
2. Import into Postman
Open Postman

Click Import

Upload Reqres API.postman_collection.json

(Optional) Import Reqres.postman_environment.json

🧪 Running Tests
Run via Postman GUI
Open the imported collection

Click Run Collection

Choose environment and click Run Tests

Run via Newman (CLI)
Install Newman globally:

bash
Copy
Edit
npm install -g newman
Run the collection:

bash
Copy
Edit
newman run "Reqres API.postman_collection.json"
With environment:

bash
Copy
Edit
newman run "Reqres API.postman_collection.json" -e "Reqres.postman_environment.json"
📸 Screenshots
Add screenshots of successful and failed test runs here, such as:

Postman test results

Newman CLI output

📄 License
This project is licensed under the MIT License – feel free to use, modify, and distribute.

Let me know if you’d like:

A downloadable version of the Postman .json collection

Sample test scripts (JavaScript code inside Postman tests)

CI/CD integration using Newman (e.g., GitHub Actions)
