# API Testing (Postman)

## API Used
JSONPlaceholder (https://jsonplaceholder.typicode.com)

---

## Test Case 1: GET list of users

**Request:**
GET /users

**Steps:**
1. Send GET request to /users

**Expected Result:**
- Status code: 200
- Response contains list of users

---

## Test Case 2: GET single user

**Request:**
GET /users/1

**Steps:**
1. Send GET request to /users/1

**Expected Result:**
- Status code: 200
- Response contains user with ID = 1

---

## Test Case 3: GET non-existing user

**Request:**
GET /users/9999

**Steps:**
1. Send request to non-existing user

**Expected Result:**
- Status code: 404
- Empty or error response

---

## Test Case 4: POST create user

**Request:**
POST /users

**Body:**
{
  "name": "Test User",
  "email": "test@test.com"
}

**Steps:**
1. Send POST request with valid body

**Expected Result:**
- Status code: 201
- Response contains created object

---

## Test Case 5: POST with invalid data

**Request:**
POST /users

**Body:**
{
  "name": ""
}

**Steps:**
1. Send POST request with invalid body

**Expected Result:**
- System should validate input
- Error response or validation failure

---

## Test Case 6: POST with invalid JSON format

**Request:**
POST /users

**Body:**
{
  "name": "Test User"
  "email": "test@test.com"
}

**Expected Result:**
- Server returns error due to invalid JSON format

**Actual Result:**
- Status code: 500 Internal Server Error
- Error message: JSON parsing error

**Conclusion:**
Error is caused by malformed JSON request, not by API logic

---

## Observations

- API follows REST principles
- GET requests retrieve data
- POST requests create data
- Status codes indicate request result (200, 201, 404)
- API does not validate input data
- POST request returns 201 even for invalid payload
- This behavior is expected for mock API (JSONPlaceholder)