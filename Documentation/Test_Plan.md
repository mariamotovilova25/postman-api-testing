{\rtf1\ansi\ansicpg1251\cocoartf2639
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx566\tx1133\tx1700\tx2267\tx2834\tx3401\tx3968\tx4535\tx5102\tx5669\tx6236\tx6803\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Test Plan: Restful-Booker API Testing\
\
## 1. Introduction\
This document outlines the testing strategy, scope, and test scenarios for the Restful-Booker REST API. The goal is to ensure the stability of the booking management lifecycle (CRUD operations) and proper authentication control.\
\
## 2. Scope of Testing\
* **In-Scope:**\
  * Authentication (Token generation).\
  * Booking creation, retrieval, full and partial updates, and deletion.\
  * API response status codes, headers, and body content.\
  * JSON Schema validation for the GET endpoint.\
* **Out-of-Scope:**\
  * Performance and load testing.\
  * UI testing.\
\
## 3. Environment & Tools\
* **Target Environment:** `https://restful-booker.herokuapp.com`\
* **Testing Tool:** Postman Desktop (v10.x)\
* **Language:** JavaScript (Chai Assertion Library)\
\
## 4. Test Scenarios & Acceptance Criteria\
* **TS_01: Authentication** \'97 Verify that valid credentials return a 200 OK status and a token.\
* **TS_02: Create Booking** \'97 Verify that a new booking is created successfully and returns a unique ID.\
* **TS_03: Read Booking** \'97 Verify retrieval of booking details and validate the response structure against the JSON schema.\
* **TS_04: Update Booking (PUT)** \'97 Verify full data updates using a valid token.\
* **TS_05: Partial Update (PATCH)** \'97 Verify partial updates without affecting unmodified fields.\
* **TS_06: Delete Booking (DELETE)** \'97 Verify deletion of the record and confirm subsequent requests return 404 Not Found.}