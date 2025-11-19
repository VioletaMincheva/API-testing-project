Mini E-Commerce API Testing Project

This project demonstrates a complete API testing workflow using Postman, Mock Server, Newman, and GitHub.
It simulates a simplified e-commerce system and showcases functional API testing, chained requests, dynamic variables, negative scenarios, and remote execution.

🚀 Project Overview

The goal of this project is to validate the main flows of a mini e-commerce system, including:
User management – Create user, login, logout
Authentication – Token handling and reuse
Product catalog – List items, retrieve a single item
Shopping cart – Add products, update, delete, view
Order operations – Complete a mock purchase
Negative testing – Invalid login, missing tokens, wrong request bodies
Tests are fully automated using Newman and can be executed from any machine, without local Postman collections — all files are hosted on GitHub.

🧰 Tools & Technologies

Postman – Test design and collection execution
Mock Server – Simulated backend API
JavaScript Assertions – Response and schema validation
Postman Environments – Variables and token extraction
Newman – Command-line execution
htmlextra Reporter – Rich HTML reporting
GitHub – Source control + remote execution

📁 Repository Contents
File	Description
Mini E-Commerce 77.postman_collection.json	Full API test collection
Mock server 77.postman_environment.json	Environment with dynamic variables
newman_report.html	Sample HTML report generated via Newman
▶️ Run Tests from Anywhere (Newman Command)

Use this command in GitBash, CMD, or any environment with Newman installed:

newman run "https://raw.githubusercontent.com/VioletaMincheva/API-testing-project/main/Mini%20E-Commerce%2077.postman_collection.json" ^
  -e "https://raw.githubusercontent.com/VioletaMincheva/API-testing-project/main/Mock%20server%2077.postman_environment.json" ^
  -r htmlextra --reporter-htmlextra-export "newman_report.html"
start newman_report.html

This command downloads the collection & environment directly from GitHub and generates a detailed HTML report.

📊 Example Validations Included

Status codes
JSON schema validation
Required fields
Token extraction and reuse
Text and numerical validations
Error-handling verification

🎯 Key Learning Outcomes

This project demonstrates:
Structuring scalable API tests
Using variables and dynamic chaining
Separating collection + environment for portability
Running API tests via CI-style tools (Newman)
Comparing mock APIs with expected business flows
Managing test data and negative scenarios
