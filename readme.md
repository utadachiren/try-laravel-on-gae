# getting started

```
docker run --rm -it -v ${PWD}:/app -w /app composer install
cp .env.example .env
docker run --rm -it -v ${PWD}:/app -w /app php:7.2 artisan key:generate
docker run --rm -it -v ${PWD}:/app -w /app php:7.2 artisan serve
```

# how install

```
# 5.5
docker run --rm -it -v ${PWD}:/app -w /app composer create-project --prefer-dist laravel/laravel ./ "5.5.*"

# 5.5 -> 5.6
# https://qiita.com/tmf16/items/b7a90c265d5f696a2325
# change composer.json and do next
# GitHub token is required during installation
docker run -it --rm -v ${PWD}:/app -w /app composer update

# 5.6 -> 5.7
# change composer.json and do next
docker run -it --rm -v ${PWD}:/app -w /app composer update

# 5.7 -> 5.8
# In another directory do next and copy they
docker run --rm -it -v ${PWD}:/app -w /app composer create-project --prefer-dist laravel/laravel ./ "5.5.*"