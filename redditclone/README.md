### Reddit Clone

60 Project Setup
- create a new project
- install venv
- source venv/bin/activate
- pip3 install django
- test localhost
- python3 manage.py runserver
- settings.py
    - django.contrib.auth // handle all the auth related stuff
- python3 manage.py migrate // create all kinds of users
- create super user
    - python3 manage.py createsuperuser

61 Sign Up View 
- python3 manage.py startapp accounts
- import accounts.views and add url pattern 
- add app in the settings.py
- add request handling in the views.py (signup.html)
- add form to the signup.html

62 POST vs GET
- add form action
    - method="POST" action="{% url 'signup' %}"
    - add cert_token to the form
    - add login in the views.py
        - if request.method == 'POST'

63 Creating Users
- import django User object
- create a dummy user with username and password passed by the request
    - User.objects.create_user(request.POST['username],
                               password = request.POST['password'])
    - return error is confirmed password does not match

64 Username Uniqueness
- use try except
- user = Users.objects.get(username=request.POST['username'])
- except Users.DoNotExist
    - create user
    - import authenticate, login
    - login the user

65 Login View
- make a template for login page
    - remove confirmed password
- add url to urls.py
- add login method
    - follow the how to login section on the django offical website
    - if user is not None:
        - login
    - return error message

66 URL include 
- import url, include
- url(r'^accounts/', include('accounts.urls'))
- create urls.py
    - past urls about accounts in it
    - change the action url

67 Posts App
- create posts app
- add posts app to setting.py
- create posts url
    - urls.py in posts
    - create method in views.py
- login_required decorator for views
    - import login_required
    - add login_required decorator

68 Next Redirect

69 Creating the Post Model

70 Saving a Post Object

71 Homepage URL

72 Homepage View

73 Voting

74 Extending Templates

75 Checking if the user is logged in

76 Logout

77 Buttons and Polish

78 Homepage Cleanup