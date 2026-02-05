# Workflow: Feature-Driven Development
**Trigger:** `/build-feature [name]`

## Execution Steps:
1. **Model & Migration:** Define the data structure.
2. **Service Layer:** Implement the logic in a new Service class.
3. **Unit Test Loop:**
   - Generate a Unit Test for the Service.
   - Run `php artisan test --unit`.
   - **Self-Correction:** If the test fails, analyze the logic, fix the Service, and re-run until it passes.
4. **Web UI:** - Create the Controller calling the Service.
   - Create the Blade templates (index, create, edit).