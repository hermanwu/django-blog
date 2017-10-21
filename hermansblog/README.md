install virtualenv for a container environment
- conda install virtualenv

create environment admin
- virtualenv venv

activate admin
- source venv/bin/activate

install django to the environment
- pip3 install django

start project
- django-admin startproject hermanblog

start app
- python3 manage.py startapp posts

start server:
- python3 manage.py runserver


Add post app
Add home page
Use views.py to handle home page request
Setup urls.py file for home page url

Model is used to represent things

Create post model

Data migration to create model in db:
- make migration script
- run migration script to generate database model

Create super admin user
- python3 manage.py createsuperuser

Register post to model
- admin.site.register(Post)

Create posts

Return posts from through views.py
and disply them on html page


Display Image
- config MEDIA_URL and 
MEDIA_ROOT in urls.py and settings.py

Configure urlpatterns for detailed post page

Make everything pretty using bootstrap

43 Static Images

44 Cleanup

45 DISQUS - Adding Comments

