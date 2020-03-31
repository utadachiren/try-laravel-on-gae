# getting started

```
docker run --rm -it -v ${PWD}:/app -w /app composer install
cp .env.example .env
docker run --rm -it -v ${PWD}:/app -w /app php:7.2 artisan key:generate
docker run --rm -it -v ${PWD}:/app -w /app php:7.2 artisan serve
```