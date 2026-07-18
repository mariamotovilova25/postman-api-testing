{\rtf1\ansi\ansicpg1251\cocoartf2639
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Test Run Execution Report \
\
## 1. Execution Summary\
* **Date of Execution:** July 16, 2026\
* **Environment:** Restful-Booker-Prod (`https://restful-booker.herokuapp.com`)\
* **Execution Source:** Postman Collection Runner\
* **Total Iterations:** 1\
* **Total Tests:** 13\
* **Passed Tests:** 13\
* **Failed Tests:** 0\
* **Skipped Tests:** 0\
* **Total Duration:** 2s 321ms\
* **Average Response Time:** 290ms\
\
## 2. Detailed Test Results by Request\
\
### 1. POST 01. Auth - Create Token\
* **Status:** 200 OK (890 ms)\
* **Tests Passed (2/2):**\
  * `[PASS]` Status code is 200\
  * `[PASS]` Response contains token\
\
### 2. POST 02. Booking - Create Booking\
* **Status:** 200 OK (271 ms)\
* **Tests Passed (2/2):**\
  * `[PASS]` Status code is 200\
  * `[PASS]` Response contains booking ID and details\
\
### 3. GET 03. Booking - Get Booking\
* **Status:** 200 OK (144 ms)\
* **Tests Passed (3/3):**\
  * `[PASS]` Status code is 200\
  * `[PASS]` Schema is valid (JSON Schema Validation)\
  * `[PASS]` Response data matches created booking\
\
### 4. PUT 04. Booking - Update Booking\
* **Status:** 200 OK (139 ms)\
* **Tests Passed (2/2):**\
  * `[PASS]` Status code is 200\
  * `[PASS]` Response contains updated data\
\
### 5. PATCH 05. Booking - Partial Update Booking\
* **Status:** 200 OK (150 ms)\
* **Tests Passed (2/2):**\
  * `[PASS]` Status code is 200\
  * `[PASS]` Response contains partially updated data\
\
### 6. DEL 06. Booking - Delete Booking\
* **Status:** 201 Created (838 ms)\
* **Tests Passed (2/2):**\
  * `[PASS]` Status code is 201 Created\
  * `[PASS]` Response body is 'Created'\
\
## 3. Conclusion\
All automated test cases executed successfully without any regressions. The API correctly maintains the full CRUD lifecycle under the current environmental conditions.}