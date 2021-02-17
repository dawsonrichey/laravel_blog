composer create-project --prefer-dist laravel/laravel laravel_rest_api "6.*"

cd laravel_rest_api

php artisan serve


DB_CONNECTION=mysql
DB_HOST=ns2.giow11.siteground.us
DB_PORT=3306
DB_DATABASE=dbfd8wwh52o6zi
DB_USERNAME=dawsonsg_drichey
DB_PASSWORD=Miws1989mi!


php artisan migrate

php artisan make:model Author -m
php artisan make:model Book -m

php artisan migrate:fresh