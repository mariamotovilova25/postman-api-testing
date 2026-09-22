# Restful-Booker API Testing Portfolio Project 
![Postman API Tests](https://github.com/mariamotovilova25/postman-api-testing/actions/workflows/main.yml/badge.svg)
This repository contains a professional and fully comprehensive API testing suite built using **Postman** and **JavaScript (Chai Assertion Library)**. The project covers the complete CRUD lifecycle of the booking service on the Restful-Booker platform, accompanied by full test documentation.

## 🛠️ Tech Stack & Concepts Used
- **Tooling:** Postman Desktop Client, Postman Collection Runner
- **Scripting:** JavaScript, Chai Assertion Library
- **Authentication:** Token-based authorization via Cookies
- **Testing Techniques:**
  - Dynamic Variable passing between requests (Environments)
  - JSON Schema Validation (using `tv4` structures)
  - Full CRUD lifecycle verification (Create, Read, Update, Delete)
  - Negative and boundary test scenarios
  - Data-Driven Testing (DDT) preparation

## 📂 Project Structure
```text
postman-api-testing/
├── Documentation/
│   ├── Test_Plan.md                   # Strategic testing approach & scope
│   └── Bug_Report.md                   # Documented defect found during testing
├── Postman/
│   ├── Restful-Booker-API-Testing.postman_collection.json  # Exported Postman Collection
│   └── Restful-Booker-Prod.postman_environment.json       # Environment variables
├── Screenshots/
│   └── 03-requests-and-tests/          # Execution visual proof
│       ├── 01_create_token_success.png
│       ├── 02_create_booking_success.png
│       ├── 03_get_booking_success.png
│       ├── 04_update_booking_success.png
│       ├── 05_partial_update_success.png
│       ├── 06_delete_booking_success.png
│       └── 07_collection_runner_passed.png
├── Test_Data/
│   └── Booking_Payloads.json           # Valid and invalid JSON test datasets
├── Test_Reports/
│   └── Test_Run_Report.md              # Detailed summary report of the test execution
└── README.md                           # Project overview and instructions

## Test Scenarios Covered
1. **POST Auth - Create Token:** Generates an access token and automatically stores it in the environment variables.
2. **POST Booking - Create Booking:** Generates a new booking, validates response structure, and extracts the `bookingId` for downstream requests.
3. **GET Booking - Get Booking:** Performs **JSON Schema validation** to ensure exact data-type structures and checks response consistency.
4. **PUT Booking - Update Booking:** Updates all booking fields, utilizing the dynamically generated authorization token.
5. **PATCH Booking - Partial Update:** Modifies specific fields (`firstname`, `totalprice`) and asserts that other data remains unchanged.
6. **DEL Booking - Delete Booking:** Deletes the created record and asserts the successful deletion status code.

## How to Run the Tests Locally

### Prerequisites
* Installed [Postman Desktop App](https://www.postman.com/downloads/).

### Import and Execution Steps
1. **Clone or Download** this repository.
2. Open Postman and click **Import** in the top-left corner.
3. Import both files from the `/Postman` directory:
   - `Restful-Booker-API-Testing.postman_collection.json`
   - `Restful-Booker-Prod.postman_environment.json`
4. Select the **Restful-Booker-Prod** environment from the environment dropdown list in the top right.
5. Click on the collection options `...` -> **Run Collection**.
6. Ensure all 6 requests are checked and click **Run Restful-Booker API Testing**.
