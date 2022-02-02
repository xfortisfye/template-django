# template-django

## Installation

```bash
pip install requirements.txt
```
<details>
    <summary>Additional Information</summary>
    pip install django
</details>
<br>

### Start Project

1\. Create Project  
```bash
django-admin startproject template_django
```

2\. Run Server  
```bash 
python manage.py runserver
```

-----
In urls.py
```python
urlpatterns = [
    path('admin/', admin.site.urls),
    path('blog/', include('blogs.urls'))
    path('', include('blog.urls')),
]
```

In blogs/urls.py
```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.home, name='blog-home'),
]
```

In blogs/views.py
```python
from django.shortcuts import render
from django.http import HttpResponse

def home(request):
    return HttpResponse('<h1>Blog Home</h1>')
```