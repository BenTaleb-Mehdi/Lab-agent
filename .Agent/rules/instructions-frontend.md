---
trigger: manual
---

# Frontend Architectural Rules (Antigravity Only)

You are forbidden from writing "heavy" or "spaghetti" frontend code. Every UI interaction must follow the Antigravity pattern.

## 1. Separation of Concerns (Hard Rule)
- **NO INLINE JS:** Do not write logic, `fetch()` calls, or complex expressions inside Blade files.
- **NO SCRIPT TAGS IN BLADE:** Avoid `<script>` tags inside `.blade.php` files. 
- **EXTERNAL COMPONENTS:** Every `x-data` must reference an external component registered via `Alpine.data()`.

## 2. Component Organization
- **FILE LOCATION:** All Alpine.js components must live in `resources/js/components/`.
- **REGISTRATION:** Components must be imported and registered in `resources/js/app.js` or a dedicated entry point.
- **NAMING CONVENTION:** Use camelCase for component names (e.g., `userProfile`, `notificationToast`).

## 3. AJAX & Communication
- **CSRF HANDSHAKE:** All AJAX requests must include the `X-CSRF-TOKEN` header. Fetch it from the `<meta name="csrf-token">` tag.
- **FEEDBACK LOOPS:** Every AJAX-enabled component must handle 3 states: `isLoading`, `data`, and `error`.
- **JSON RESPONSES:** Expect and handle only JSON responses from the backend.

## 4. Performance & UX
- **X-CLOAK:** Always use `x-cloak` on components to prevent flickering on page load.
- **OPTIMISTIC UI:** For actions like "Like" or "Delete", update the local state immediately before the server confirms.
- **UTILITY-FIRST:** Use Tailwind CSS classes only. Avoid custom `<style>` blocks in Blade.

## 5. Implementation Workflow
1. Create the JS component in `resources/js/components/[name].js`.
2. Export the component function.
3. Register it in `app.js`.
4. Use it in Blade: `<div x-data="name({ param: 'value' })">`.