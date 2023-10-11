# Predicting_Kedney_Disease

# Chronic_Kidney_Disease
This dataset can be used to predict the chronic kidney disease and it can be collected from the hospital nearly 2 months of period.
- Dataset : https://archive.ics.uci.edu/dataset/336/chronic+kidney+disease
- Setup Gibhub
- Created Conda environment (conda create -p venv python==3.7 -y)
- Created Decision Tree Machine learning with accuracy: 0.9917
- Created a pikle file in order to create a web app and to deploy to Herukou cloud
- Create file requirements.txt

- On terminal: pip install -r requirements.txt

- Setup Gitcls: configuration needs to do its for the first time

    git config --global user.name
    git config --global user.email
    Commit steps for all the code into github repo:

        - git add file name; if add is only one file such (requirements.txt)
        - git add . ; if add all the file
        - git commit -m "massage any"
        - git push origin main; to main branch

- create app.py file
- into app.py file:
    - import pickle
    - from Flask import Flask,request,app,jasonify,url_for,reder_template

- check the app it into postman and the push to github

- create a web app where create a form at app.py

- For HerokuAccount - create a file as procfile which allows to specify command into heroku acc

- Docker and github Action

- create a Docker file:

    - FROM: THIS COMMAND IS TO SELECT A BASE IMAGE which set on linus os
    - COPY: whatever file we have here we neeed to copy to the BASE image
    - WORKDIR: workdirectory is the same where we copy from all the file here
    - RUN: we have in those file some dependencies which needs to run as we have a file requirements.txt
    - EXPOSE: inside the docker image run as a container we have to expose a port
    - CMD: run gunicorn which helps to run entire python app in herukou

- Setup Github Action: 2 folder needs to created

    - folder: .github
    - into .github another folder: workfolws
    - into both folder: create file main.yaml as soon as we push into github , it sees the folders here , all the docker will   be into main.yaml file

- main.yaml:
    to find: 
        - 1 secret: go to github setting : secret : new repo secret: herokou api key : herolu deshbord, go account, from seting, see api key
        - 2 secret key: click new secret: herouki email
        - 3 secret : herouko app name