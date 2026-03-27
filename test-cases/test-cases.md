# Test Cases

## Login

### TC-01: Login with valid credentials

**Preconditions:**
User is on login page

**Steps:**
1. Enter valid username
2. Enter valid password
3. Click Login button

**Expected Result:**
User is successfully logged in and redirected to dashboard

---

### TC-02: Login with invalid password

**Preconditions:**
User is on login page

**Steps:**
1. Enter valid username
2. Enter invalid password
3. Click Login button

**Expected Result:**
Error message is displayed and user is not logged in

---

### TC-03: Login with empty fields

**Preconditions:**
User is on login page

**Steps:**
1. Leave username empty
2. Leave password empty
3. Click Login button

**Expected Result:**
Validation messages are displayed for required fields

---

## Dashboard

### TC-04: Dashboard is displayed after login

**Preconditions:**
User is logged in

**Steps:**
1. Observe dashboard page

**Expected Result:**
Dashboard elements are visible and loaded correctly

---

## Navigation

### TC-05: Navigate to PIM module

**Preconditions:**
User is logged in

**Steps:**
1. Click on PIM in main menu

**Expected Result:**
PIM module is opened successfully

---

## Employee Search

### TC-06: Search employee by name

**Preconditions:**
User is in PIM module

**Steps:**
1. Enter employee name in search field
2. Click Search

**Expected Result:**
Matching employee is displayed in results

---

### TC-07: Search with no results

**Preconditions:**
User is in PIM module

**Steps:**
1. Enter non-existing name
2. Click Search

**Expected Result:**
System shows empty result or appropriate message

---

## Logout

### TC-08: Logout from system

**Preconditions:**
User is logged in

**Steps:**
1. Open user menu
2. Click Logout

**Expected Result:**
User is logged out and redirected to login page

---

## Negative & Edge Cases

### TC-09: Login with leading/trailing spaces in username

**Preconditions:**
User is on login page

**Steps:**
1. Enter valid username with spaces before and after (e.g., "  admin  ")
2. Enter valid password
3. Click Login button

**Expected Result:**
System trims spaces and processes input correctly. User is logged in if credentials are valid.

---

### TC-10: Login with very long username

**Preconditions:**
User is on login page

**Steps:**
1. Enter username exceeding allowed length (e.g., 256+ characters)
2. Enter valid password
3. Click Login button

**Expected Result:**
System rejects input and displays validation message indicating invalid username length.

---

### TC-11: Login with SQL injection attempt

**Preconditions:**
User is on login page

**Steps:**
1. Enter ' OR '1'='1 in username field
2. Enter any password
3. Click Login button

**Expected Result:**
System treats input as plain text. Login fails and error message is displayed.

---

### TC-12: Username case sensitivity check

**Preconditions:**
Registered user exists

**Steps:**
1. Enter username in different case
2. Enter valid password
3. Click Login button

**Expected Result:**
System consistently applies case sensitivity rules and handles authentication accordingly.

---

### TC-13: Login with only spaces in username field

**Preconditions:**
User is on login page

**Steps:**
1. Enter only spaces in username field
2. Enter valid password
3. Click Login button

**Expected Result:**
System treats input as invalid and displays validation message.