# Pipenv Test Case 1: .python-version File Detection

## What This Tests
Tests that `.python-version` (pyenv) file is the highest priority source for Python version detection in Pipenv projects.

## Expected
3.9.0 found through PyenvVersionFile

## Files
- `.python-version` - Contains `3.9.0`
- `Pipfile` - Contains conflicting version `3.8` in requires section

## Expected Behavior
Your version detection tool should detect **Python 3.9.0** from `.python-version`.

## Priority
This is the **highest priority** detection method for Pipenv projects.

## Note
Even though Pipfile specifies Python 3.8, the .python-version file takes precedence according to the pipenv priority chain.
