# 🛠️ Capacity: Service Management

## Description
Analyze, create, and reuse Laravel Service classes to keep controllers thin and logic organized.

## Inputs
- `app/Services/` (Existing logic)
- `app/Providers/` (Dependency injection)

## Outputs
- `app/Services/[Name]Service.php`

## ✅ Control Points
- [ ] No DB logic in Controllers (Move to Service).
- [ ] Methods are named after business actions (ex: `applyDiscount()`).
- [ ] Services are injected via the Constructor.