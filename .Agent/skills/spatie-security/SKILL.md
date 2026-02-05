# Skill: Spatie Security Expert
Specialized knowledge for managing Roles and Permissions in Laravel.

## Capabilities:
- **Policy Generation:** Can automatically create Laravel Policies for any Model.
- **Middleware Injection:** Knows how to add `->middleware('can:...)` to Web routes.
- **Role Syncing:** Includes a script to verify if Permissions in code match the Database.

## Usage Rule:
Whenever a new feature is built via `/build-feature`, this skill is activated to ensure the "Create" and "Delete" actions are protected by specific roles.