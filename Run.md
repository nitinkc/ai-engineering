## Projects
[https://aiengineeringfromscratch.com/projects](https://aiengineeringfromscratch.com/projects)

## One time setup
```shell
uv python install 3.12

uv venv
# Replace your current environment and inject pip/setuptools
uv venv --seed

####  Inject pip into your existing venv
python -m ensurepip --upgrade

source .venv/bin/activate 
```
## Build site locally
```shell
source .venv/bin/activate 

node site/build.js          # regenerate site/data.js (optional, CI does this on main)
python3 -m http.server 8000 # from repo root

uv pip install ....
# open http://localhost:8000/site/

# http://localhost:8000/site/lesson.html?path=phases/11-llm-engineering/01-prompt-engineering&learningPath=building-and-deploying-ai-applications
```

## Keeping forks updated

```shell
git remote add upstream https://github.com/rohitg00/ai-engineering-from-scratch.git

git fetch upstream
git merge upstream/main
```
