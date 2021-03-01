

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
