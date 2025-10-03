# Development Guidelines

## Documentation Research
- When researching technical solutions, **MUST** use context7 to get the latest technical documentation
- Verify documentation currency before implementing third-party integrations
- Prefer official documentation over community sources

## Test-Driven Development (NON-NEGOTIABLE)

### Mandatory TDD Discipline
- Tests MUST be written BEFORE implementation (no exceptions)
- Red-Green-Refactor cycle strictly enforced:
  1. Write failing test
  2. User approves test coverage
  3. Verify test fails
  4. Implement minimal code to pass
  5. Refactor with tests passing

### Test Coverage Requirements
- Contract tests required for all APIs and module boundaries
- Integration tests required for all user-facing workflows
- Unit tests required for business logic and edge cases
- Test coverage MUST be ≥80% for all production code
- All tests MUST be deterministic (no flaky tests tolerated)

### Rationale
TDD ensures requirements are testable, prevents regression, documents intended behavior, and enables confident refactoring. The discipline forces clear thinking about interfaces before implementation.

## Code Quality Standards

### General Principles
- Write self-documenting code with clear naming
- Follow DRY (Don't Repeat Yourself) principles
- Maintain single responsibility for functions and modules
- Prioritize readability over cleverness

### Error Handling
- Fail fast with meaningful error messages
- Handle edge cases explicitly
- Never swallow exceptions silently
- Log errors with sufficient context for debugging

### Performance
- Optimize only when necessary (measure first)
- Document performance-critical sections
- Avoid premature optimization
- Consider scalability in design decisions

## Security Best Practices
- Never hardcode secrets, API keys, or credentials
- Validate all user inputs
- Follow principle of least privilege
- Keep dependencies up to date
- Perform security reviews for authentication/authorization logic

## Documentation
- Document complex business logic
- Keep README files current
- Document API contracts and interfaces
- Include setup instructions for new developers
- Update documentation when code changes
