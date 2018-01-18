#Easy install

1. git clone && checkout branch develop
2. php artisan tinker 
	-factory(App\User::class, 100)->create();
3. 


#fresh install

1. composer create-project --prefer-dist laravel/laravel datatables
2. php artisan migrate
3. php artisan tinker 
	-factory(App\User::class, 100)->create();
4. composer require yajra/laravel-datatables-oracle
5. for laravel 5.5+ no need to add class to config/app.php due to package autodiscovery 
6. php artisan vendor:publish
7. create master layout file
8. php artisan make:controller DatabaseController
9. import datatables facade in controller : use Yajra\Datatables\Datatables
10. ..
11. ..
12. ..
13. Route::get('datatables', 'DatatablesController@index');
14. Route::get('anydata', 'DatatablesControllers@anyData')->name('anydata');