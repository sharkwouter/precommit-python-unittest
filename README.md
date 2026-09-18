# Pre-commit hook for Python based unit tests

A hook for running `python3 -m unittest discover` within your project upon running `git commit` using [pre-commit](https://pre-commit.com/). This is a bad idea for most projects, since unit tests can take a while and in many cases require a venv to be configured in the shell.

## Using with pre-commit

Simply add the following to your `.pre-commit-config.yaml`:

```yaml
-   repo: https://github.com/sharkwouter/precommit-python-unittest
    rev: 1.0.0
    hooks:
    -   id: python-unittest
```

