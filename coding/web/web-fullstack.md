# Full Stack Web development

- [Azure Static Web Apps](https://github.com/GeekTrainer/aswa-workshop)

## APIs

- [APIs for Beginners - How to use an API (Full Course / Tutorial)](https://www.youtube.com/watch?v=GZvSYJDk-us)

## Django

- [How to Start Django Project with a Database -PostgreSQL](https://stackpython.medium.com/how-to-start-django-project-with-a-database-postgresql-aaa1d74659d8)
- [Django with Nginx, Gunicorn](https://medium.com/analytics-vidhya/dajngo-with-nginx-gunicorn-aaf8431dc9e0)
- [How To Set Up Django with Postgres, Nginx, and Gunicorn on Ubuntu 22.04](https://www.digitalocean.com/community/tutorials/how-to-set-up-django-with-postgres-nginx-and-gunicorn-on-ubuntu-22-04)
- [Serving multiple Django apps with Gunicorn and Nginx (CentOS 7)](https://caterinadmitrieva.medium.com/serving-multiple-django-apps-on-second-level-domains-with-gunicorn-and-nginx-a4a14804174c)
- [The Python Requirements File and How to Create it](https://learnpython.com/blog/python-requirements-file/)
- [ImportError: cannot import name 'url' from 'django.conf.urls' after upgrading to Django 4.0](https://stackoverflow.com/questions/70319606/importerror-cannot-import-name-url-from-django-conf-urls-after-upgrading-to)

```shell
    I think a quick fix to this problem is to do followings;
    You can easily replace
    from django.conf.urls import url
    to this:
    from django.urls import re_path as url
    And keep the rest of code to be same as before.
```

- [Django TemplateSyntaxError - 'staticfiles' is not a registered tag library](https://stackoverflow.com/questions/55929472/django-templatesyntaxerror-staticfiles-is-not-a-registered-tag-library)

```shell
    If you have any of the following tags in your template:
    load staticfiles 
    load static from staticfiles 
    
    load admin_static
    Then replace it with:

    load static
```


### Azure

- [Quickstart: Deploy a Python (Django, Flask, or FastAPI) web app to Azure App Service](https://learn.microsoft.com/en-us/azure/app-service/quickstart-python?tabs=django%2Cmac-linux%2Cvscode-aztools%2Cvscode-deploy%2Cdeploy-instructions-azportal%2Cterminal-bash%2Cdeploy-instructions-zip-azcli)
- [Tutorial: Deploy a Django web app with PostgreSQL in Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/tutorial-python-postgresql-app)

### Docker

- [Deploying Django Apps with Docker: A Step-by-Step Guide](https://betterstack.com/community/guides/scaling-python/dockerize-django/) <span style="color:red">&nbsp;new</span>
- [Dockerizing Django with Postgres, Gunicorn, and Nginx](https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/) <span style="color:red">&nbsp;new</span>


- [Making queries](https://docs.djangoproject.com/en/5.1/topics/db/queries/)
- [Templates](https://docs.djangoproject.com/en/5.1/ref/templates/)

### Bootstrap

- [Build fast, responsive sites with Bootstrap](https://getbootstrap.com/)
- [CDN via jsDelivr](https://getbootstrap.com/docs/5.1/getting-started/download/#cdn-via-jsdelivr)

## Node JS

- [Learn NODE JS](https://www.tutorialspoint.com/nodejs/index.htm)
