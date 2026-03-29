# DevTools Network Analysis

## Login Request Analysis

**Tool Used:**
Chrome DevTools (Network tab)

---

### Request Details

**Endpoint:**
/web/index.php/auth/validate

**Method:**
POST

**Payload:**
- _token: CSRF token used for request validation
- username: Admin
- password: admin123

---

### Response Details

**Status Code:**
302 Found

**Headers:**
- Location: /dashboard/index (redirect after successful login)
- Set-Cookie: session is created

---

### Observations

- Request includes CSRF token for security protection
- Token helps prevent unauthorized or forged requests
- Login request is sent to authentication endpoint `/auth/validate`
- Server validates credentials and returns redirect response
- Status code 302 indicates successful authentication with redirect
- Session cookie is set after login
- User is redirected to dashboard after successful login

---

### Conclusion

The login flow confirms proper client-server interaction:
- Client sends credentials via POST request
- Server validates input
- Server establishes session
- User is redirected to dashboard