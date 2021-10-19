# Django Boilerplate

## Current Features

- Django user model extended with AbstractUser
- Dockerized
- Postgres DB
- Crispy forms and Tailwind CSS

## How to use this boilerplate

1. Git clone https://github.com/vacchiano/django-boilerplate
2. Build the css run `npm run build`
3. `docker compose up -d --build`
4. `docker compose exec web python manage.py migrate`
5. Code away

Don't forget to remove the "home" function in config/urls.py and use your own. To start a new project - a personal blog for example, run 
```
docker compose exec web python manage.py startapp core
```
Replace core with whatever the name of the project you are starting. Also, to run any of the Django commands or pipenv install new packages you have to start with "docker compose exec web" - where exec stands for execute and web is the name of the service you defined in the docker-compose.yml file.

- *adopted from this blog post here https://htmx-django.com/blog/a-minimalistic-modern-django-boilerplate*
- *tailwind css incorporated based on this blog post here https://medium.com/@lendinez/how-to-use-tailwind-in-django-and-not-die-in-the-attempt-2853eb164aa7*