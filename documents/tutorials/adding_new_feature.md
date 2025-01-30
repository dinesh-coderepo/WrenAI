# Adding a New Feature to WrenAI

This tutorial will guide you through the process of adding a new feature to the WrenAI repository. Follow the steps below to create a new branch, make changes, write tests, and submit a pull request.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **Git**: Version 2.30 or higher
- **Python**: Version 3.12 or higher
- **Node.js**: Version 18 or higher
- **Poetry**: Version 1.8.3
- **Just**: Version 1.36 or higher
- **Docker**: Latest version

## Step 1: Create a New Branch

First, create a new branch for your work. This helps keep your changes organized and makes it easier to collaborate with others.

```sh
git checkout -b <branch-name>
```

Replace `<branch-name>` with a descriptive name for your branch.

## Step 2: Make Changes

Make the necessary changes to add your new feature. This may involve modifying existing files or creating new ones. Ensure your code follows the project's coding standards and best practices.

## Step 3: Write Tests

Write tests for your new feature to ensure it works as expected. Place your tests in the appropriate test directory and follow the existing test structure.

### Example Test (Python)

```python
import pytest

def test_new_feature():
    assert new_feature() == "expected result"
```

### Example Test (JavaScript)

```javascript
test('new feature', () => {
  expect(newFeature()).toBe('expected result');
});
```

## Step 4: Commit Changes

Commit your changes with a clear and descriptive commit message.

```sh
git commit -m "Description of the changes"
```

## Step 5: Push Changes

Push your changes to your forked repository.

```sh
git push origin <branch-name>
```

## Step 6: Create a Pull Request

Create a pull request (PR) to the main repository. Provide a clear description of the changes and link to any relevant issues.

1. **Go to the main repository on GitHub**.
2. **Click on the "Pull requests" tab**.
3. **Click on the "New pull request" button**.
4. **Select your branch from the "compare" dropdown**.
5. **Provide a clear and descriptive title and description for your PR**.
6. **Link to any relevant issues**.
7. **Click on the "Create pull request" button**.

## Additional Resources

For more information on contributing to WrenAI, refer to the following resources:

- [Contributing Guide](../contributing.md)
- [Getting Started](getting_started.md)
- [Deployment](deployment.md)

We appreciate your contributions and look forward to working with you!
