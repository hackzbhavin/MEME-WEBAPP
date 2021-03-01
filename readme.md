

Download all the files

- Requirements: Commandprompt/ Console/ Terminal , browser 


> Go inside the directory
1. To migrate all settigs `python manage.py migrate` 

2. `python manage.py makemigrations memewebapp`
3. To run server `python manage.py runserver`
4. To create superuser `python manage.py createsuperuser`


---
What i have done in this project?
--
1. Login Page accepts username and password credentials with proper validation

2. Login user validates through database

3. Redirects to webpage where the cookies get stored for current session(You may need to reload the tab it does work on normal server hosted on pc after clicking accept). Each session has its own cookies

4. Informed the users that website collects the cookies and store their consent in database and ask for their choice to accept or decline. Cookies shown in the container at the bottom which fades away after 5 seconds.

5. If user accepts the cookies 5 memes are shown from the api at https://imgflip.com/api

6. else user will be displayed sorry message and the session will be logged out





DEPLOYEMENT STEPS
----
------------------ DEPLOYEMENT STEPS ON PYTHONANYWHERE ---------------

1. Go to https://www.pythonanywhere.com/login/

2. Signup for new account if don’t have any

3. Open console

TYPE:

1. pwd

2. git clone ‘https://github.com/hackzbhavin/MEME-WEBAPP’

3. mkvirtualenv –python=/usr/bin/python3.5 myenv

4. pip install django

5. pip install requests

4. Now open dashboard in another tab till the task is running on console

5. Go to web tab

6. create web app click next

1. select manual configuration [ Select a Python Web Framework]

2. choose python 3.5

3. You will have your web app ready just need to add more settings

-------------------------- Customize your web tab--------------------------

1. edit virtual env add myenv

........(environment name created in console)

2. edit code edit WSGI configuration file

remove everything just keep the django part and remove the comment like below attached screeenshot modify path modify os.environ['DJANGO_SETTINGS_MODULE'] save the file

3. update allowed host in project FILES in settings.py add the url without http example: ALLOWED_HOSTS = ['hackzbhavin.pythonanywhere.com']

4. Now reload the url you may find the css is not loaded on the html page

5. At the end of the file add STATIC_ROOT='/home/hackzbhavin/MEME-WEBAPP/static'

6. In console run python manage.py collectstatic

7. In WEB tab STATIC FILES url : /static/ directory : /home/hackzbhavin/MEME-WEBAPP/static

8. Dont forget to RELOAD
