### Setup Guide project

## Step 1: Clone project

```
1. git clone https://github.com/JxNov/laravel-l5-repository-template.git

2. after clone, you can change the name of project
   - mv laravel-l5-repository-template your_project_name
   
3. cd your_project_name

4. rm -rf .git
```

## Step 2: Setup docker

- [Install docker](https://docs.docker.com/compose/install/)

```
1. cp .env.example .env

2. docker-compose build

3. docker-compose up -d
```

## Step 3: Setup laravel

```
1. docker exec -it container_name bash

2. mkdir storage

3. cd storage/

4. mkdir -p framework/{sessions,views,cache} - if not has this folder

5. composer install

6. php artisan key:generate

7. php artisan migrate

8. php artisan db:seed

9. chmod -R o+w storage/
```

## Step 5: When change config queue

```
1. docker-compose dowm
2. docker-compose build
3. docker-compose up -d

OR

1. supervisorctl restart all
```

## NOTE

```
1. When change config crontab
    - cron reload
```
