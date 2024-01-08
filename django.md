# Topics to understand
- [ ] Signals
- [ ] Middlewares
- [ ] async django
- [ ] asgi
- [ ] polling and long polling
- [ ] django logging
- [ ] understand the directory structure of a new django app and the purpose of each file.
- [ ] The path() function is passed four arguments, two required: route and view, and two optional: kwargs, and name. At this point, it’s worth reviewing what these arguments are for. `understand deeply`
- [ ] `django-storage` putting static files in `s3bucket`

### setting up static files
1. create `src/static`
2. create `root_directory_for_project/local-cdn/static`
3.  create `my_app/static/my_app` for each app
4.  in `settings.py`
```py
STATIC_URL='static/'
STATICFILES_DIRS=[
    BASE_DIR / "static",
]
STATIC_ROOT= BASE_DIR.parent / "local-cdn" / "static"
```
5. in `core/urls.py`
```python
from django.conf import settings
from django.contrib import admin
from django.urls import path
urlpatterns = [
path( 'admin/', admin.site.urls),
if settings.DEBUG:
    # do not do this in production
    from django.conf.urls.static import static
    from django.conf import settings

    urlpatterns +=
    static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)


```



