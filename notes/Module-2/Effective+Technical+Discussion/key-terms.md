# Terminologies
## Markdown
* Unordered lists can be denoted as `*` and `-`

---

## Reproducible Code
* Code that can be reliably executed to produce same results
* Supports documentation and sharing of technical discussions

### Example Use Case
```
def add(a, b):
	return a + b
```

`add()` here is reproducible because always produces `5` when `print(add(2,3))` is called

---

## GitHub
* Python package: `github`

### Example Use Case
```
import github

# Authenticate yourself and access GitHub API
g = github.Github("your_access_token")
repo = g.get_repo("gitusername/reponame")
print(repo.description)
```

---

## Gist
* Simple way to share Code Snippets and Fragments via GitHub

### Example Use Case
```
import requests

url = 'https://api.github.com/gists/gist_id'
print(response.json()['description'])
```

---

## Jupyter Notebook
* Usually for `ipynb` files, basically for Python notebooks