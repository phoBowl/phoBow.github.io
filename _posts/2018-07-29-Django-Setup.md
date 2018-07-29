---
layout: post
title: Django Setup
subtitle: ... Django for beginer
tags: [django-learning, django, python, basic-django]
---

_This instruction uses Linux Bash command on Windows_<br>
To install Django by Linux command:
* pip install django

After successfully install django on your machine. Let create a project
Step 1: Run this command and change PROJECT_NAME to your project name. If you do not see any output, dont worry, It is just how it works.
* django-admin startproject PROJECT_NAME

Step 2: Move to your project folder
* cd PROJECT_NAME

Step 3: You will see a file name manage.py in the directory by using **ls** command. We will then run the server and after that try to access 127.0.0.1:8000 on you web browser. It should display a hello world page
* python manage.py runserver 0.0.0.0:8000

Step 4: Migrate to project with database
* python manage.py migrate
