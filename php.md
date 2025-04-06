## General Guidelines for PHP and Laravel Development
* PHP Version: Assume the use of PHP 8.2 to leverage its latest features and improvements.
* Laravel Version: For Laravel-specific code, assume Laravel 10 is in use.
* Prevent N+1 Query Issues: Always optimize database queries to avoid N+1 problems and highlight potential occurrences in code reviews or explanations.
* Constructor Property Promotion: Use PHP 8’s constructor property promotion to reduce boilerplate code in classes.
* Yoda-Style Comparisons: Write comparisons in Yoda style (e.g., `null === $variable` instead of `$variable === null`) to prevent accidental assignments (e.g., `$variable = null`).
* Strict Null Checks: Avoid `is_null()`; prefer strict comparisons to `null` (e.g., `=== null`).
* Empty Array Checks: Replace comparisons to an empty array (e.g., `$array === []`) with `empty($array)` for simplicity.
* PHPDoc Comments: Omit unnecessary PHPDoc comments above functions when return types and parameters are explicitly defined in the code.
* Avoid Redundant Checks: Do not combine `isset()` and `!empty()` unless absolutely necessary; prefer a single, clear condition.
* Modern PHP Features: Leverage the latest PHP features available in PHP 8.2, such as readonly properties or enhanced type systems.
* Minimize Conditional Chains: Limit lengthy `if/elseif/else` chains; use `match` expressions or early returns to improve readability and maintainability.
* Prefer Match Expressions: Favor `match` expressions over `if` or `switch` statements for concise and type-safe condition handling.
* Early Returns: Use early returns to simplify control flow and enhance code readability.
* Avoid Function Chaining: Refrain from direct function chaining (e.g., `doSomething(doAnother())`); instead, use intermediate variables with descriptive names (e.g., `$result = doAnother(); doSomething($result);`) for better readability and debugging.
* Data Handling: Avoid passing data as plain arrays; use Data Transfer Objects (DTOs) or Enums, especially for API request data, to improve type safety and structure.
* Avoid Flag Parameters: Replace boolean flag parameters with Enums to represent state clearly and explicitly.
* Adhere to Principles: Follow KISS (Keep It Simple, Stupid), SOLID, and DRY (Don’t Repeat Yourself) principles in all code design.
* Refactoring: Do not refactor existing code unless explicitly requested by the user.
* Design Patterns: Promote the use of design patterns, avoiding traditional Singleton implementations (self-enforced single instances). Instead, use Laravel’s container-managed singletons (e.g., `$app->singleton()`), which provide reusable instances through the service container while retaining flexibility.
* Error Handling: Implement consistent error handling with try-catch blocks for exceptions, returning meaningful error messages or responses, particularly in API contexts.

## Prefered packages
* Do NOT use FOSRestBundle
* Use symfony/http-client instead of guzzle when not using laravel
* Setup grumphp with code quality tools php cs fixer and phpstan
* Create unit tests for all code
* Create feature tests for all commands and endpoints
