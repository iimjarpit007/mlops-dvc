create env

'''bash

conda create -n wineq python=3.11

'''

activate env

'''bash

conda activate wineq

'''

create requitements.txt

installed the requirements

''' bash

pip install - r requirements.txt

'''

create template.py

'''bash

echo.> template.py

download data from the link

https://drive.google.com/drive/folders/18zqQiCJVgF7uzXgfbIJ-04zgz1ItNfF5

process of sync github account with vscode

Click source control-->select github-->enter your credentials

bash '''

git init

bash '''

bash '''

dvc init

bash '''

bash '''

dvc add data_given/winequality.csv

bash '''

bash '''

git add .

bash '''

git commit -m "first commit"

bash '''

bash '''

git add . && git commit -m "update README.md"

bash'''

Create github repository-->mlops-dvc

bash'''
git remote add origin https://github.com/iimjarpit007/mlops-dvc.git
git branch -M main
git push origin main

'''

update params.yaml

after every update run below two commands

bash '''
git add . && git commit -m "update params.yamland README.md" 
git push origin main
bash'''

update get_data.py in src folder and create get and rea data method
push the changes yafter adding and commiting

create load_data.py to load data to raw folder
update dvc.yaml file till load_stage
run dvc repro to run stages
update readme
push the changes yafter adding and commiting

create split_data.py to split data to into train and test and save in processed folder
update dvc.yaml file till load_split_stage
run dvc repro to run stages
update readme
push the changes yafter adding and commiting

create train_and_evaluate.py to train and evaluate test data, generate scores and parametrics
update dvc.yaml file for train and eval stage
run dvc repro to run stages
update readme
push the changes yafter adding and commiting

bash'''

dvc metrics show
dvc metrics diff

bash'''

you can change value of param l1 and alpha in param.yaml and see diff
dvc repro
dvc metrics show
dvc metrics diff

no test the model
install tox and pytest
update tox
make dir test-bash '''mkdir tests''' and create .py files in it
tox command''' tox'''
tox command for rebuiding'''tox -r'''

create package by creating setup.py
run bash '''pip install -e .''' to create src package

bash'''
cd ..
import src
cd MLOPS_P1/
ls
'''
src egg info file will be created with all details


build your own package commands

bash'''
python setup.py sdist bdist_wheel
'''
above will create shareable dist of whl and tar.gz which they can install in their own pc

setup command'''
pip install -e .
'''