# Rule: Monolith Service Architecture

The Agent must follow the Service Pattern for all business logic to ensure Unit Testability.

## Implementation Standards:

- **Controllers:** Must be "Thin." Their only job is to handle requests and return `view()` or `redirect()`.
- **Services:** All database operations and calculations must live in `App\Services`.
- **Type Safety:** All Service methods must use strict PHP type hinting (e.g., `public function calculate(int $amount): float`).

## Reason for this Rule:

To allow for pure **Unit Testing** without needing to boot the entire Laravel database or routing engine.
