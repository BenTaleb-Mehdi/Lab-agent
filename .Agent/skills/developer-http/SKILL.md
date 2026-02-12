---
name: developer-http
description: Manages Routing, Controllers, and Middleware for secure data flow.
---

# Skill: HTTP Specialist

## 🎯 Mission
Ensure the application is accessible and secure. You bridge the **Frontend Agent's** requests to the **Business Agent's** services.

### 🚫 Rules
1. **Validation First**: Always use `FormRequest` to validate data before it hits the Controller.
2. **No Business Logic**: Never write complex logic in Controllers; call a Service instead.
3. **Restful**: Follow REST patterns for URL naming (e.g., `GET /items`, `POST /items`).

---

## ⚡ Actions

### Action A: Route Definition
> **Description**: Create clean and secure URL endpoints.
- **Inputs**: Feature name and required access level (Guest/Auth).
- **Outputs**: Route definitions with appropriate Middlewares.

### Action B: Controller Implementation
> **Description**: Create methods to receive requests and return responses.
- **Inputs**: HTTP Verb (GET/POST) and the Service to call.
- **Outputs**: Controller methods returning JSON or Views.

---

## 🔄 Scenarios

### Scenario: Creating a New API Endpoint
1. **Route**: Execute **Action A** to define the URL in `api.php`.
2. **Validate**: Create a `FormRequest` to check the incoming data.
3. **Connect**: Execute **Action B** to call the **Business Agent's** Service and return the result to the **Frontend Agent**.

---

## ⚙️ Standards
- **Middleware**: Use `auth:sanctum` for API security.
- **Responses**: Always use a consistent JSON structure for APIs.
- **Versioning**: Use versioning for APIs (e.g., `/api/v1/...`).