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
django-admin startproject django_project
```

2\. Run Server  
```bash 
python manage.py runserver
```

3\. Start App
```bash
python manage.py startapp blog
```

-----

- Always add your new __startup app__ from the `blog/apps.py` to the INSTALLED_APPS in `django_project/settings.py` 
- `{% load static %}` `<link rel="stylesheet" type="text/css" href="{% static 'blog/main.css' %}">`
- `path('', views.home, name='blog-home')` `<a class="nav-item nav-link" href="{% url 'blog-home' %}"> Home</a>`
