# fastweb-djan-strap
Create By Taati89
initial web with django and bootstrap4

## Requirements
- [Python](https://www.python.org/downloads/release/python-367/) version 3.6.7
- [Django](https://www.djangoproject.com/) version 3.0.6
- [Bootstrap Template](https://startbootstrap.com/themes/)

## Run Server
> python website/manage.py runserver

open website with url : 
> http://localhost:8000/webapp/

## How to Using
1. New Bootstrap Template
    - Delete all file and folder in fastweb-djan-strap/website/webapp/templates and fastweb-djan-strap/website/static
    - [Download New Bootstrap Template](https://startbootstrap.com/themes/)
    - Extract file zip.
    - Move html file to fastweb-djan-strap/website/webapp/templates/webapp
    - Move other file or folder to fastweb-djan-strap/website/static
    - add "{% load static %}" in first line of all html file.
    - edit attribute "href" or "src" when not used link.
        - example
        href="css/styles.css" -> href="{% static 'css/styles.css' %}"
    - add new route with editing fastweb-djan-strap/website/webapp/urls.py 
        - add path('newPage', views.newPage, name='newPage'),
        - add new function

            def newPage(request):

                context = {}
                return render(request, 'webapp/newPage.html', context)

...