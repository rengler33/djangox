# README.md

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

Recommended settings for vscode:

```javascript
"settings": {
    "python.formatting.provider": "black",
    "editor.formatOnSave": true,
    "python.linting.enabled": true,
    "python.linting.pylintEnabled": false,
    "python.linting.flake8Enabled": true
}
```
