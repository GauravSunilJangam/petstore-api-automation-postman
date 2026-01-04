🚀 PetStore API Automation – Postman & Newman
📌 Project Overview

This project demonstrates end-to-end REST API automation testing using Postman and Newman on the Swagger PetStore public REST API.

The framework covers positive, negative, and regression scenarios with environment-based execution and detailed HTML reporting.

🧪 Application Under Test

Swagger PetStore – Public REST API
Base URL: https://petstore.swagger.io/v2

🧩 Modules Covered
🐶 Pet Module

Create Pet

Get Pet by ID

Update Pet

Delete Pet

Pet Not Found (Negative)

🏬 Store Module

Create Order

Get Order by ID

Delete Order

Order Not Found (Negative)

👤 User Module

Create User

Get User

Update User

Delete User

Login & Logout

🛠 Tools & Technologies

Postman – API testing & scripting

Newman – CLI execution

newman-reporter-htmlextra – HTML reporting

JavaScript – Assertions & test logic

Git & GitHub – Version control

📂 Project Structure
petstore-api-automation-postman
├── postman
│   ├── collections
│   │   └── petstore_api_collection.postman_collection.json
│   └── environments
│       └── petstore_qa_environment.postman_environment.json
├── reports
│   └── PetStore_Report.html
└── README.md

⚙️ Environment Configuration

The project uses Postman Environment Variables:

baseUrl

petId

orderId

username

password

Environment file:

postman/environments/petstore_qa_environment.postman_environment.json

▶️ How to Execute Using Newman
🔹 Prerequisites

Node.js installed

Newman installed globally

npm install -g newman
npm install -g newman-reporter-htmlextra

🔹 Run Collection with HTML Report
newman run postman/collections/petstore_api_collection.postman_collection.json \
-e postman/environments/petstore_qa_environment.postman_environment.json \
-r cli,htmlextra \
--reporter-htmlextra-export reports/PetStore_Report.html

📊 Test Report

After execution, an HTML execution report is generated at:

reports/PetStore_Report.html


Open this file in any browser to view:

Request-wise execution status

Assertions summary

Response times

Failure details (if any)

✅ Key Highlights

Environment-based execution

Collection-level common assertions

Dynamic ID handling using environment variables

Swagger PetStore instability handled gracefully (5xx safe assertions)

Newman CLI execution with HTML report

CI/CD ready structure

👤 Author

Gaurav Sunil Jangam
API Automation Tester | Postman | Newman | REST API Testing

⭐ If you find this project useful, feel free to star the repository.