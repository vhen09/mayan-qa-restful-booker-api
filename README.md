# Mayan QA Technical Assessment – API Testing

## Project Overview

This repository contains a Postman API testing collection created for the **Junior Tech Associate (QA) Technical Assessment**.

The collection tests the RESTful Booker API, covering authentication, booking creation, booking updates, retrieval, and deletion.

**Target API:** https://restful-booker.herokuapp.com

## Tools Used

- Postman
- REST API
- JavaScript (Postman test scripts)
- GitHub

## API Test Coverage

| Test ID | Request | Method | Test Scenario |
|---|---|---|---|
| 01 | `/auth` | POST | Create authentication token |
| 02 | `/booking` | POST | Create a booking |
| 03 | `/booking/:id` | PUT | Update an existing booking |
| 04 | `/booking/:id` | GET | Verify updated booking |
| 05 | `/booking/:id` | DELETE | Delete a booking |
| 06 | `/booking/:id` | GET | Verify deleted booking |
| 07 | `/auth` | POST | Negative test – invalid credentials |
| 08 | `/booking` | POST | Negative test – incomplete booking payload |
| 09 | `/booking/:id` | PUT | Negative test – invalid authentication token |
| 10 | `/booking/:id` | GET | Negative test – nonexistent booking |
| 11 | `/booking/:id` | DELETE | Negative test – invalid authentication token |

## Testing Features

- Dynamic extraction and reuse of authentication tokens.
- Dynamic booking ID extraction and variable chaining.
- HTTP status code assertions.
- Response body and data validation.
- Positive and negative API testing.
- Authentication and authorization checks.
- Verification of booking deletion.

## Execution Instructions

1. Download and install Postman.
2. Import `Mayan-Restful-Booker-API-Tests.postman_collection.json`.
3. Set the `baseUrl` collection variable to `https://restful-booker.herokuapp.com`.
4. Leave the `token` and `bookingId` variables blank initially.
5. Execute the requests in the appropriate sequence.
6. Review the response and test results in Postman.

## Notable Observation

The incomplete booking payload negative test returned `500 Internal Server Error` instead of a client-side validation response such as `400 Bad Request` or `422 Unprocessable Entity`.

This behavior was documented as an API validation issue.

## Repository Contents

- `Mayan-Restful-Booker-API-Tests.postman_collection.json` – Exported Postman collection containing API requests and test scripts.

## Author

Prepared as part of the Mayan Junior Tech Associate (QA) Technical Assessment.
