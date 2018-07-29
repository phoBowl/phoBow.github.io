---
layout: post
title: Django Setup
subtitle: ... Django for beginer
tags: [django-learning, django, python, basic-django]
---

_This instruction uses Linux Bash command on Windows_<br>
To install Django by Linux command:
* pip install django

After successfully install django on your machine. Let create a project<br>
**Step 1:** Run this command and change PROJECT_NAME to your project name. If you do not see any output, dont worry, It is just how it works.
* django-admin startproject PROJECT_NAME

**Step 2:** Move to your project folder
* cd PROJECT_NAME

**Step 3:** You will see a file name manage.py in the directory by using **ls** command. We will then run the server and after that try to access 127.0.0.1:8000 on you web browser. It should display a hello world page
* python manage.py runserver 0.0.0.0:8000
```
$ python manage.py runserver 0.0.0.0:8000
Performing system checks...

System check identified no issues (0 silenced).

You have unapplied migrations; your app may not work properly until they are applied.
Run 'python manage.py migrate' to apply them.

July 29, 2018 - 14:03:02
Django version 1.8.7, using settings 'learning_site.settings'
Starting development server at http://0.0.0.0:8000/
Quit the server with CONTROL-C.
```
<br>
**Step 4:** Notice the output from the previous step, we see 'You have unapplied migration;...'. Now let migrate to project with database
* python manage.py migrate
```bash
$ python manage.py migrate
Operations to perform:
  Synchronize unmigrated apps: staticfiles, messages
  Apply all migrations: admin, contenttypes, auth, sessions
Synchronizing apps without migrations:
  Creating tables...
    Running deferred SQL...
  Installing custom SQL...
Running migrations:
  Rendering model states... DONE
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying sessions.0001_initial... OK
```
Now, the project should be set up properly and we are ready with awesome Python - Django projects.
