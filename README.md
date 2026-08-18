# Pytest Basic Function Tests

A collection of basic pytest test functions demonstrating fundamental testing concepts including assertions, functions, and class-based tests.

## Overview

This project contains introductory pytest test cases that showcase:
- Simple function assertions
- Mathematical operations testing
- Class-based test organization
- Credential validation testing

## Files

### test_example.py
Contains basic test functions demonstrating simple assertions and calculations:

- **`test_example()`**: A simple assertion test that verifies 1 equals 1
  - Purpose: Demonstrates the most basic pytest assertion
  - Expected Result: PASS

- **`test_addition()`**: Tests basic arithmetic operation
  - Purpose: Verifies that 2 + 2 equals 4
  - Expected Result: PASS

### test_login.py
Contains class-based tests for login functionality:

- **`TestLogin` class**: Organized test class for login-related tests
  - **`test_login()`**: Tests username and password validation
    - Verifies username equals "admin"
    - Verifies password equals "admin123"
    - Expected Result: PASS

## Installation & Setup

### Prerequisites
- Python 3.6+
- pytest

### Install pytest
```bash
pip install pytest
```

## Running Tests

### Run all tests in the directory
```bash
pytest
```

### Run a specific test file
```bash
pytest test_example.py
pytest test_login.py
```

### Run a specific test function
```bash
pytest test_example.py::test_example
pytest test_example.py::test_addition
pytest test_login.py::TestLogin::test_login
```

### Run tests with verbose output
```bash
pytest -v
```

### Run tests with detailed output and print statements
```bash
pytest -s
```

### Run tests and show coverage
```bash
pytest --cov
```

## Expected Output

When running all tests:
```
test_example.py::test_example PASSED
test_example.py::test_addition PASSED
test_login.py::TestLogin::test_login PASSED

=== 3 passed in 0.XX seconds ===
```

## Key Pytest Concepts

### Assertions
The `assert` statement is used to verify that a condition is true:
```python
assert 1 == 1  # Passes if condition is true
assert result == 4  # Fails if condition is false
```

### Test Functions
- Must start with `test_` prefix
- Use assertions to verify expected behavior
- Each function tests one specific behavior

### Test Classes
- Class names should start with `Test`
- Contain multiple test methods
- Useful for organizing related tests
- Each method must start with `test_`

## Learning Resources

- [Pytest Official Documentation](https://docs.pytest.org/)
- [Pytest Assertions](https://docs.pytest.org/en/stable/example/index.html)
- [Pytest Fixtures](https://docs.pytest.org/en/stable/fixture.html)

## Next Steps

To expand these basic tests:
1. Add more complex assertions
2. Implement test fixtures for setup/teardown
3. Add parametrized tests for testing multiple inputs
4. Integrate with CI/CD pipelines
5. Add test coverage reports
6. Implement mock objects for external dependencies

---

**Status**: Basic test suite for learning pytest fundamentals
