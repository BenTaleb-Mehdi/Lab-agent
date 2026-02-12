# ⚡ Capacity: Alpine.js & UI

## Description
Build reactive interfaces using decoupled Alpine.js components and AJAX (Fetch API) to communicate with Laravel.

## Inputs
- `resources/js/components/` (External JS files)
- `resources/views/` (Blade templates)
- `routes/api.php` (Endpoints for data)

## Outputs
- `resources/js/components/[name].js`
- Reactive Blade components (x-data)

## ✅ Control Points
- [ ] Logic is in `.js` files, not inside `@click` or `x-init`.
- [ ] `x-cloak` is used to prevent layout shift.
- [ ] `isLoading` state is handled for every network request.