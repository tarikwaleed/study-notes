# Topics to understand
- [ ] Signals
- [ ] Middlewares
- [ ] async django
- [ ] asgi
- [ ] polling and long polling
- [x] django logging
- [x] understand the directory structure of a new django app and the purpose of each file.
- [ ] The path() function is passed four arguments, two required: route and view, and two optional: kwargs, and name. At this point, it’s worth reviewing what these arguments are for. `understand deeply`
- [ ] `django-storage` putting static files in `s3bucket`
- [ ] what is `SECRET_KEY` in `settings.py`
- [ ] template loaders [here](https://docs.djangoproject.com/en/4.2/ref/templates/api/#django.template.loaders.cached.Loader)
- [ ] advanced ORM
- [ ] query optimization in django
- [ ] transaction management
- [ ] what happens if 2 requests came to the dataabse in the same time
- [ ] queuing in django (celery)
- [ ] redis caching
- [ ] 

### setting up static files
1. create `src/static`
2. create `root_directory_for_project/local-cdn/static` and put it in `.gitignore`
3.  create `my_app/static/my_app` for each app
4.  in `settings.py`
```py
STATIC_URL='static/'
STATICFILES_DIRS=[
    BASE_DIR / "static",
]
STATIC_ROOT= BASE_DIR.parent / "local-cdn" / "static"
```
5. add the following to  `core/urls.py`
```python
if settings.DEBUG:
    from django.conf.urls.static import static

    urlpatterns += static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
```

### setting up Templates
1. create `src/templates`
2. in `settings.py`, add this to the `TEMPLATES` list
```python
'DIRS':[ BASE_DIR / "templates"]
```
3. create `templates/base.html`




