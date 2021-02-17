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

php artisan make:seeder AuthorsTableSeeder
php artisan make:seeder BooksTableSeeder

php artisan migrate:fresh

php artisan db:seed

php artisan make:factory AuthorFactory
php artisan make:factory BookFactory

php artisan db:seed

php artisan migrate:fresh
php artisan db:seed

php artisan tinker
  Author::first()
  Author::all()
  Author::count()
  Book::first()
  Book::all()
  Book::count()
  Book::first()->author
  Author::first()->books
  Author::first()->books->count()

php artisan make:controller RegularController //remove
php artisan make:controller ResourceController -r //remove

php artisan make:controller AuthorController -r --api
php artisan make:controller BookController -r --api