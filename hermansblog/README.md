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
- {% load static %}
- free image: unsplash.com

44 Cleanup

45 DISQUS - Adding Comments
- remember to add identifier for disqus of each page

46 Add about page
- don't forget to add page to 

50 Vultr
- virtual private server

51 Security
- enter root user password
- add a regular user instead of using root user
- allow regular user to do "sudo"
- PermitRootLogin no
- sudo ufw app list
- sudo ufw allow OpenSSH
- sudo ufw enable (setup firewall)

52 Pip and Virtualenv
- sudo apt-get update
- sudo apt-get upgraded
- sudo apt-get install python3-pip
- sudo apt-get install nginx
- sudo pip3 install virtualenv

53 Uploading Code To Server
- use FileZilla
- activate venv (create virtual environments)

54 Runserver
- allow 8000
- pip install django
- python3 manage.py runserver 0.0.0.0:8000
- add following to the settings.py
    - ALLOWED_HOSTS = [your server ip]

55 Gunicorn
- in order to run django even after terminal is stopped
- pip install gunicorn (with venv permission)
- gunicorn --bind 0.0.0.0:8000 hermansblog.wsgi:application
edit /etc/systemmd/system/gunicon.service file
- sudo system start gunicorn
- sudo system enable gunicorn

56 Nginx
- config nginx/site-available
- sudo ngix -t
- sudo systemctl restart nginx
- allow 8000
- configure settings.py for static pic
    - STATIC_ROOT = os.path.join(BASE_DIR, 'static')
    - python3 manage.py collectstatic 
- Get a domain from domain.google.com
    - add your domain name to nginx/site-available
    - add following in the settings.py
        - ALLOWED_HOSTS = [your domain name]
