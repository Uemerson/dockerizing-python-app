# About this repository
Example of dockerizing Python App using Flask with Postgres, Gunicorn, and Nginx.

# How to run ?

### Development

```
$ docker-compose up -d --build
$ docker-compose exec web python manage.py create_db
```

### Production

```
$ docker-compose -f docker-compose.prod.yml up -d --build
$ docker-compose -f docker-compose.prod.yml exec web python manage.py create_db
```

### Test it out one final time

- Upload an image at http://localhost:1337/upload.
- Then, view the image at http://localhost:1337/media/IMAGE_FILE_NAME.

To stop and remove containers, networks, images, and volumes:
```
$ docker-compose down -v
```