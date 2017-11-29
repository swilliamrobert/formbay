## FormBay - API

Please follow the guide.

Development Setup.

1. `git clone`
2. `sudo groupadd docker`
3. `sudo gpasswd -a $USER docker`
4. `sudo chmod -R 777 ./storage ./bootstrap ./database`
5. `docker-compose build`
6. `docker-compose up -d`

Application Setup

1. `composer install`
2. `docker-compose exec app php artisan key:generate`
3. `docker-compose exec app php artisan migrate`
4. `docker-compose exec app php artisan db:seed`
5. `docker-compose exec app php artisan serve`

Use postman or browser to call the below API
```
URL : http://0.0.0.0:8080/api/users
```

1. Get All Users
```
URL : http://0.0.0.0:8080/api/users
```
2. Get users by ID
```
URL : http://0.0.0.0:8080/api/users/5a0e4b82078f471ae05dd33f
```
3. Full text search by name
```
Example Params: key=name / value=Susana
URL : http://0.0.0.0:8080/api/users?name=Susana