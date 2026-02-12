---
description: Orchestrates skills to generate a full Laravel CRUD (Model, Migration, Service, Controller, UI).
---

# Workflow : CRUD Execution

## 1. Context & Objective
**Goal**: Generate a functional CRUD for a specific entity by coordinating specialized agents.
**Strategy**: Sequential execution from Database -> Business Logic -> HTTP Entry -> Frontend Interface.

## 2. Execution Steps

### Step 1: Data Foundation (`developpeur-data`)
**Action**: Create the persistence layer.
1. **Generate Migration**: Define table columns based on the entity.
2. **Generate Model**: Set up `$fillable`, relationships, and casts.
3. **Generate Factory**: Create fake data for testing.

### Step 2: Business Logic (`developer-business`)
**Action**: Centralize the logic in a Service class.
1. **Create Service**: Implement `getAll()`, `store()`, `update()`, and `delete()`.
2. **Standard**: Ensure no business logic remains in the Controller.

### Step 3: HTTP Gateway (`developer-http`)
**Action**: Expose the logic via API/Web routes.
1. **Define Routes**: Add resource routes in `api.php`.
2. **Create Controller**: Inject the Service and handle JSON responses.
3. **Create Request**: Implement `FormRequest` for input validation.

### Step 4: Reactive UI (`expert-frontend`)
**Action**: Build the interactive frontend.
1. **Blade Structure**: Create the table/form container with `x-data`.
2. **Alpine Component**: Create the external `.js` component to handle `fetch()` calls.
3. **UX**: Implement `isLoading` and success/error notifications.

## 3. Validation Plan
1. **Migrate**: Run `php artisan migrate`.
2. **Test API**: Verify JSON output for `index` and `store`.
3. **Compile**: Run `npm run dev`.