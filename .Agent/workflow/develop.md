#  Antigravity Developer Workflow

When a new feature is requested:

1. **DB Step:** `expert-database` designs the migration.

2. **Logic Step:** `expert-service` writes the Action/Service class.
3. **HTTP Step:** `expert-http` creates the route and the controller method.
4. **UI Step:** `expert-frontend` builds the Alpine.js component and connects it via AJAX.

**Core Rule:** Every expert must review the code to ensure it's "Light" and follows the Antigravity principles.