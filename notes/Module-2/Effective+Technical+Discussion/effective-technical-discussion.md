# Effective Technical Discussion
Must be able to share reproducible code 
(code MUST run smoothly if not what's the point to share)

## 2 Ways to Share Reproducible Code:

### 1. Hosted Git
* GitHub (most common)
* bitbucket
* GitLab

Two main ways to share code:
1. Create public repo and/or MD files -- MD can also serve out via webpages (ie GitHub Pages or blog engine like [Hugo](https://gohugo.io/))
2. [Gist](https://gist.github.com/) (GitHub feature) -- Code Snippet can be automatically rendered out in many chat programs

### 2. Hosted Jupyter Notebooks
* Fundamental limitation: the Python packaging environment
* Solution: use Jupyter Notebooks that have portable runtime (ie [Docker](https://www.docker.com/) and [Colab](https://colab.research.google.com/))

**Recreate Code and Run Locally using Docker**
```
#!/usr/bin/env bash

# Build image
docker build --tag=flasksklearn .

# List docker images
docker image ls

# Run flask app
docker run -p 8000:80 flasksklearn
```

**Colab**
`.ipynb` files

---

## Other forms of Technical Discussion
* Add audio, video, images
* Sharing images (GitHub Issues)
* Screencast (Zoom, QuickTime Player, Camtasia)

---

**In essence:**
* Produce once, reuse many