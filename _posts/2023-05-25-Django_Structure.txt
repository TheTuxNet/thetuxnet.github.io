---
title: "Basic Django project structure"
date: 2023-05-25
excerpt: Project structure for a simple django project
categories: django 
tags: django
---
# Basic Django project structure

```
django_project
├── app/
│   ├── migrations/
│   ├── static/
│   ├── templates/
│   ├── tests/
│   ├── __init__.py
│   ├── admin.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
├── config/
│   ├── settings/
│   │ ├── __init__.py
│   │ ├── base.py
│   │ ├── development.py
│   │ ├── staging.py
│   │ ├── production.py
│   │ └── testing.py
│   ├── __init__.py
│   ├── asgi.py
│   └── wsgi.py
├── docs/
├── scripts/
├── static/
├── media/
├── tests/
├── requirements/
│   ├── base.txt
│   ├── development.txt
│   ├── staging.txt
│   └── production.txt
├── .env
├── .gitignore
└── manage.py
```
Requirements and settings should contain separate files for each environment

## Settings
- base.py (common settings)
- local.py (local dev settings - extends base.py)
- staging.py (staging version - extends base.py)
- test.py (test settings - extends base.py)
- production.py (live server settings - extends base.py)