

### Step 1:

Created the github repo :

echo "# DVC-ML-usecase" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Sumit-Kumar-Dash/DVC-ML-usecase.git
git push -u origin main


### Step 2
Created the env :

conda create -n dvc_ml python=3.7 -y
conda activate dvc_ml

## Referenced repo:
https://github.com/c17hawke/dvc-ML-demo-AIOps

## Now run these commands from local terminal 
git init
git remote add origin https://github.com/Sumit-Kumar-Dash/DVC-ML-Use-case.git
git branch -M main

## Step 3
touch .gitignore
touch README.md
touch requirements.txt  

mkdir -p src/utils
touch src __init__.py
touch src/utils __init__.py

dvc init

touch params.yaml dvc.yaml

## Step 4
touch setup.py
create setup.py :--------------------

from setuptools import setup

with open("README.md", "r", encoding="utf-8") as f:
    long_description = f.read()

setup(
    name="src",
    version="0.0.1",
    author="c17hawke",
    description="A small package for dvc ml pipeline demo",
    long_description=long_description,
    long_description_content_type="text/markdown",
    url="https://github.com/c17hawke/dvc-ML-demo-AIOps",
    author_email="sunny.c17hawke@gmail.com",
    packages=["src"],
    python_requires=">=3.7",
    install_requires=[
        'dvc',
        'pandas',
        'scikit-learn'
    ]
)

------end of setup.py

## Step 5
mkdir config 
touch config.yaml 
    edit the config.yaml file

## step 6
touch src/utils/all_utils.py   src/stage_01_load_save.py 

edit all_utils.py , requirements.txt 

## Step 7
pip install -r requirements.txt
pip list 

## Step 8  - IMP
edit stage_01_load_save.py and dvc.yaml

## Step 9
python src/stage_01_load_save.py 
dvc repro
dvc dag

git add .
git commit -m "commit message"
git push origin main# DVC-ML-Use-case
