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

66 URL include 

67 Posts App

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