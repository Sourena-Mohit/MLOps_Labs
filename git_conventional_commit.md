## Conventional Commits

The Conventional Commits specification provides a standard way of writing commit messages to make them more readable and informative. Each commit message starts with a type (e.g., `feat:`, `fix:`) that indicates the purpose of the change.

### Common Types Used in Conventional Commits

1. **chore:**
   - **Purpose:** Used for changes that do not modify source code or tests.
   - **Examples:** Updating build tools, dependency management, or configuration files.
   - **Example Commit Message:**
     
     chore: update npm dependencies
     

2. **docs:**
   - **Purpose:** For changes related to documentation.
   - **Examples:** Updating README files, comments, or inline documentation.
   - **Example Commit Message:**
     
     docs: update contributing guidelines
     

3. **style:**
   - **Purpose:** For code style changes that do not affect the functionality of the code.
   - **Examples:** Adjusting formatting, fixing whitespace, or correcting typos in the code.
   - **Example Commit Message:**
     
     style: fix indentation in main.py
     

4. **refactor:**
   - **Purpose:** For code changes that neither add new features nor fix bugs, but improve the code's structure or readability.
   - **Examples:** Renaming variables, simplifying functions, or modularizing code.
   - **Example Commit Message:**
     
     refactor: simplify authentication logic
     

5. **perf:**
   - **Purpose:** For changes that improve performance.
   - **Examples:** Optimizing algorithms, reducing memory usage, or enhancing loading speed.
   - **Example Commit Message:**
     
     perf: improve database query performance
     

6. **test:**
   - **Purpose:** For adding or updating tests.
   - **Examples:** Adding unit tests, integration tests, or correcting existing test cases.
   - **Example Commit Message:**
     
     test: add unit tests for user registration
     

7. **feat:**
   - **Purpose:** For introducing new features.
   - **Examples:** Adding new API endpoints, implementing a new UI component, or integrating a new library.
   - **Example Commit Message:**
     
     feat: add support for user notifications
     

8. **fix:**
   - **Purpose:** For bug fixes.
   - **Examples:** Resolving errors, fixing broken functionality, or patching vulnerabilities.
   - **Example Commit Message:**
    
     fix: resolve login issue on mobile devices
     

### Conventional Commit Format

A typical Conventional Commit message looks like this:


<type>[optional scope]: <description>

[optional body]

[optional footer(s)]