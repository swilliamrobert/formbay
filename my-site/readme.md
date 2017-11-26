## FormBay - API

Please follow the guide.

1. `git clone`
2. `cd my-site`
3. `composer install`
4. `sudo chmod -R 777 ./storage ./bootstrap ./database`
5. `sudo docker-compose up -d`
6. `sudo docker-compose exec app php artisan key:generate`
7. `sudo docker-compose exec app php artisan migrate`
8. `sudo docker-compose exec app php artisan db:seed`
9. `sudo docker-compose exec app php artisan serve`

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