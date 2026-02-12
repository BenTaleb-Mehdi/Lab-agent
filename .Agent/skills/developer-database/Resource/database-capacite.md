# 🗄️ Capacity: Database Management

## Description
Direct access to manage the database structure, migrations, and indexing strategy for Laravel.

## Inputs
- `database/migrations/` (Current schema)
- `config/database.php` (Connection settings)

## Outputs
- Migration files
- SQL Optimization reports

## ❌ Specific Prohibitions
- Never run `db:wipe` or `migrate:fresh` in production context.
- Never use raw SQL if an Eloquent equivalent exists.

## ✅ Control Points
- [ ] Every table must have `timestamps()`.
- [ ] Foreign keys must use `constrained()`.
- [ ] Critical columns for searching must have an `index()`.