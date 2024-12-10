# Key Terms

## CI (Continuous Integration)
Practice of frequently merging developer code changes into a shared repo and automatically testing the changes to catch issues early

```
import unittest

def sum(a, b):
	return a + b

# Test for validation
class TestSum(unittest.TestCase):
	def test_sum(self):
		self.assertEqual(sum(2, 3), 5)

if __name__ == '__main__':
	unittest.main()

# If test passes, CI/CD pipeline continues
# If test fails, pipeline is blocked
```

---

## Build Server

* Server that automatically runs Builds and Tests whenever code changes are pushed to the repo
* **GitHub Action** is an example of a popular cloud-based build server

---

## Makefile
A file containing recipes for common project automation tasks like
* Installing dependencies
* Running tests
* Linting code

Makefiles are commonly used with CI/CD pipelines

```
# Makefile

# Example Makefile recipe

lint:
	pylint **/*.py

test:
	pytest -vv

format:
	black *.py

clean:
	rm -rf build

# Call with `make lint`, `make test` etc
```

---

# YAML
(Yet Another Markup Language)

* Commonly used for config
* GH Actions workflows are all defined in YAML

```
# YAML

# GH Actions Workflow YAML

name: CI
on: [push]

jobs:
	
	lint:
		runs-on: ubuntu-latest
		steps:

		- uses: actions/checkout@v3

		- name: Set up Python
		  uses: actions/setup-python@v3
		  with:
		    python-version: "3.9"

		- name: Install
		  run: |
		    pip install black

		- name: Lint
		  run: |
		    black . --check
```

---

## Artifact

* Output of a build process
* Usually some file(s) that get deployed or released if tests pass
* Represent the state of code at a point in time

```
# Artifact

import pickle

data = {"page_views": [154, 183, 287]}

# Save final analysis as an artifact
with open("report.pkl", "wb") as f:
	pickle.dump(data, f)

# Archive / Upload report.pkl
# If tests pass --> Deploy live!
```