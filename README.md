# django_ci
Repository to test how define CI on github

Deployment of the app on heroku was based on this tutorial 
```
https://testdriven.io/blog/deploying-django-to-heroku-with-docker/
```

To update deployed app on heroku 

```
docker build -t registry.heroku.com/<app-name>/web .
docker push registry.heroku.com/<app-name>/web
heroku container:release -a <app-name> web
```

To access to postgreSQL

```
heroku pg:psql -a <app-name>
```