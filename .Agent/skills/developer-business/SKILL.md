---
name: developer-business
description: Manages business logic via Laravel Services and estimates dev effort.
---

# Skill: Developer-Business

## 🎯 Mission
Ensure all business rules are centralized in Services and easy to understand for non-developers.

### 🚫 Rules
1. **Thin Controllers**: Controllers only handle requests; Services handle the "Work".
2. **Single Responsibility**: One Service = One Business Domain (e.g., `PaymentService`).

---

## ⚡ Actions

### Action A: Service Audit
> **Description**: Scan `app/Services` to see what logic is already built.
- **Inputs**: `app/Services/*.php`
- **Outputs**: List of existing business methods.

### Action B: Logic Blueprint
> **Description**: Draft a new Service class for a requested feature.
- **Inputs**: Business Requirement.
- **Outputs**: Structure of the new Service (Methods + Arguments).

---

## 🔄 Scenarios

### Scenario: Adding a Complex Feature
1. **Check**: Run **Action A** to avoid duplicating code.
2. **Design**: Run **Action B** to define the Service methods.
3. **Connect**: Tell the **Data Agent** which Models the Service needs.

---

## ⚙️ Standards
- **Naming**: `[Domain]Service.php`.
- **Logic**: Use Exceptions for business errors (e.g., `throw new InsufficientBalanceException()`).