## Questions
* django only for webapp ? cli also
* what does wsgi.py actually do?
* `python manage.py runserver` runs app, but how do we actually serve our application in prod ?
* we use pyenv in prod ... how it works?
* What’s the difference between a project and an app?
* what is `r'^` in urls. - jus regex
* urlname need not necessarily be the appname or best practice ?
* what if many urls shares same functionalities ....how to write functionality shared by many urls ?
* `url()` vs `path()` - just rename
* what is .idea/

* what if we forget to makemigrations and instead run migrate directly


## Notes

##### Create project
    Note: need isolated environment to create Django project

   * create a virtual environment  - `pyenv virtualenv 3.6.5 name_of_project`
   * Associate the python environment created to the path - `pyenv local name_of_project`
   * Install Django - `pip install Django`
   * Scaffold new project - `django-admin startproject name_of_project`
   * start app `python ./manage.py runserver`

##### Create apps

   * create new app - `django-admin startapp app_name` will create view,model,url,admin,apps and tests files
   1. url - has the urlpatterns for the app
        * urlpattern is the **path** for the **view** given a **name** .
   2. model - defines database layout of the app
        * has the models i.e sub-classes of `django.models.Model` defining the Fields with type or sometimes behaviour
   3. view - holds the business logic for the corresponding url
   4.

##### steps for app
    1. create view
    2. create path for the view in URLconf of the app.
    3. include the URLconf of the app in the project.
    4. create Model
    5. include the app in the INSTALLED_APPS in project settings
    6. run makemigrations for the app to generate migrations code
    7. run migrate to apply changes to database
    8. start app