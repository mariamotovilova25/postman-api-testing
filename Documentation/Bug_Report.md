{\rtf1\ansi\ansicpg1251\cocoartf2639
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fmodern\fcharset0 Courier;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\partightenfactor0

\f0\fs26 \cf0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 # Bug Report: Missing clear error message or automatic token refresh on 403 Forbidden \
\
## Status: Open | Severity: Medium | Priority: High\
\
## Description\
When attempting to perform a full booking update (PUT) using an expired or missing token, the server returns a generic `403 Forbidden` response instead of a detailed error message (e.g., "Token expired"). Furthermore, the API application lacks an automated token renewal mechanism during collection runs.\
\
## Environment\
- **URL:** `https://restful-booker.herokuapp.com/booking/`\
- **Tool:** Postman Desktop\
- **Environment config:** Restful-Booker-Prod\
\
## Steps to Reproduce\
1. Generate an authorization token using `POST /auth`.\
2. Create a new booking using `POST /booking`.\
3. Wait for the session token to expire (or manually corrupt the token value in Headers).\
4. Send a `PUT` request to `/booking/\{id\}` to update the created booking.\
\
## Expected Result\
The API should return a clear, informative error message in JSON format, such as `\{"error": "Token has expired, please re-authenticate"\}` or handle session refreshing automatically.\
\
## Actual Result\
The API returns a raw `403 Forbidden` status code, causing all automated response assertions and JSON parsing scripts to fail.}