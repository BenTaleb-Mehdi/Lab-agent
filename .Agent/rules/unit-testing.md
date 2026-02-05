# Rule: Unit Testing Standards
Every Service class must have a corresponding Unit Test.

## Requirements:
- **Framework:** Use **PHPUnit**.
- **Location:** Tests must be placed in `tests/Unit`.
- **Mocking:** Use mocks for external dependencies to keep tests fast and isolated.
- **Coverage:** Tests must cover the "Happy Path" and at least two "Edge Cases" (e.g., empty inputs, invalid numbers).