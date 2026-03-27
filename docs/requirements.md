# Requirements Overview

## Project
OrangeHRM Demo — manual QA pet project

## Objective
The purpose of this project is to validate the core functionality of the OrangeHRM demo web application from the perspective of a Junior QA Engineer.

## In-Scope Modules
1. Login
2. Dashboard
3. Main navigation
4. PIM module
5. Employee search
6. Logout

## Out of Scope
1. Performance testing
2. Security testing
3. Mobile responsiveness
4. Cross-browser testing
5. Integration with external services

## Assumptions
1. The application is available and accessible through a web browser.
2. A valid test user account exists.
3. The system supports standard user interactions through UI.
4. Test environment behavior may differ from production systems.

## High-Level Functional Requirements

### 1. Login
- The user should be able to log in with valid credentials.
- The system should reject invalid credentials.
- Required fields should be validated.
- Error messages should be displayed for unsuccessful login attempts.

### 2. Dashboard
- After successful login, the user should be redirected to the dashboard.
- Dashboard elements should be displayed correctly.
- Main menu items should be accessible.

### 3. Navigation
- The user should be able to open different modules from the main menu.
- Active menu item should correspond to the selected module.

### 4. PIM Module
- The user should be able to open the PIM section.
- The user should be able to access employee list functionality.
- Employee records should be displayed in a table format.

### 5. Employee Search
- The user should be able to search employees using available filters.
- Search results should match entered criteria.
- Empty or invalid search conditions should be handled correctly.

### 6. Logout
- The user should be able to log out from the system.
- After logout, access to authenticated pages should be restricted.

## Risks
1. Demo environment may contain unstable or non-production behavior.
2. Some data may already exist and affect search or filtering results.
3. Certain functions may be limited in the demo version.