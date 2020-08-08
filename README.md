# UIkit paginator for Laravel
Laravel Paginator template for the UIKit JS/CSS Library from YOOtheme.

## How To Use This File?
1. Export the existing paginator's files with the default ```artisan``` *vendor* command:
```bash
php artisan vendor:publish --tag=laravel-pagination
```

2. Copy the *uikit.blade.php* file into the vendor directory with the other paginator's files.
```bash
cp ./resources/views/vendor/pagination/uikit.blade.php /path/to/laravel/installation/resources/views/vendor/pagination/.
```

3. Update the default paginator updating the boot method in the AppServiceProvider.php file on 'app/Providers' with the following script:
```php
...
use Illuminate\Pagination\Paginator;
...
class AppServiceProvider extends ServiceProvider
{
...
		public function boot()
	    {
        ...
        Paginator::defaultView('pagination::uikit');
        Paginator::defaultSimpleView('pagination::uikit');
        ...
	    }
	}
```

Done! Now you have it!

Happy Coding!