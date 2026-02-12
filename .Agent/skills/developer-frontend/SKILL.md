---
name: expert-frontend
description: Specialist in Decoupled Alpine.js and reactive Laravel interfaces.
---

# Skill: Expert Frontend

## 🎯 Mission
Build fast, interactive UIs that feel like an SPA. Keep Blade files clean by putting all JavaScript logic into external Alpine components.

### 🚫 Rules
1. **No Inline JS**: Never write complex functions inside HTML attributes.
2. **State Control**: Always manage `data`, `isLoading`, and `errors`.
3. **Security**: Always send the `X-CSRF-TOKEN` with every Fetch request.

---

## ⚡ Actions

<<<<<<< HEAD
### Action A: Component Creation
> **Description**: Create a new external Alpine.js component.
- **Inputs**: HTML structure and required data features.
- **Outputs**: `Alpine.data('name', ...)` object in a JS file.
=======
### 3.  UX
- **Optimistic UI:** Update the local state immediately when the user interacts, then sync with the server in the background.
- **Zero Flicker:** Use `x-cloak` to prevent unstyled content from flashing on load.
>>>>>>> 709ecc4e4392e06caaf46151272b646f58150500

### Action B: API Integration (AJAX)
> **Description**: Connect the UI to Laravel backend using Fetch.
- **Inputs**: Route URL and data object.
- **Outputs**: Async functions with error handling.

---

<<<<<<< HEAD
## 🔄 Scenarios

### Scenario: Creating a Reactive List
1. **Structure**: Define the HTML in Blade using `x-data="listComponent()"`.
2. **Logic**: Run **Action A** to create the JS file with an `items` array.
3. **Sync**: Run **Action B** to fetch data from the **Data Agent's** API.

---

## ⚙️ Standards
- **Style**: Use Tailwind CSS for styling.
- **UX**: Use "Optimistic UI" (update local data before the server responds).
- **Format**: Standardize headers for `XMLHttpRequest`.
=======
    async fetchItems() {
        this.isLoading = true;
        try {
            const response = await fetch('/items', {
                headers: { 'X-Requested-With': 'XMLHttpRequest' }
            });
            const result = await response.json();
            this.items = result.data;
        } finally {
            this.isLoading = false;
        }
    }
});
>>>>>>> 709ecc4e4392e06caaf46151272b646f58150500
