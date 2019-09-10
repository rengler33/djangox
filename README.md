# README.md

## Adapted from wsvincent/djangox for my own projects

### Setup

Need to run:

```shell
python manage.py makemigrations users
python manage.py migrate
```

If using Docker:

```shell
docker-compose up
docker-compose exec web "python manage.py makemigrations users"
docker-compose exec web "python manage.py migrate"
```

When adding an email service, you will want to update the `DEFAULT_FROM_EMAIL` setting as well as the domain name and display name in the sites table created by all-auth.

You can generate a new secret key from inside the django shell with the following:

```python
>>> from django.core.management.utils import get_random_secret_key
>>> get_random_secret_key()
```

### Recommended settings for vscode

```javascript
"settings": {
    "python.formatting.provider": "black",
    "editor.formatOnSave": true,
    "python.linting.enabled": true,
    "python.linting.pylintEnabled": false,
    "python.linting.flake8Enabled": true
}
```
