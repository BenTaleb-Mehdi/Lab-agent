# 🌐 Capacity: HTTP Communication

## Description
Manage the entry points of the application, including Routing, Controllers, and Middleware logic.

## Inputs
- `routes/` (web.php and api.php)
- `app/Http/Controllers/`
- `app/Http/Middleware/`

## Outputs
- `app/Http/Controllers/[Name]Controller.php`
- API Response formats (JSON)

## ✅ Control Points
- [ ] Routes use named routes (e.g., `->name('users.index')`).
- [ ] Controllers are "Thin" (Logic is delegated to Services).
- [ ] API responses use standard HTTP status codes (200, 201, 422, etc.).