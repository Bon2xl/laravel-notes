# My Laravel Notes

## Routes

### Routers 1.0
Get  and print URL parameters in routes and display template 
[/routes/web.php](/routes/web.php)
[resources/views/routes.blade.php](resources/views/routes.blade.php)


```php
use Illuminate\Http\Request;

Route::get('/routes', function (Request $request) {
  $name = $request->input('name');
  return view('routes', [
    'name' => $name,
  ]);
});
```
```
https://laravel-notes.test/routes/?name=arvind
```
```blade
what is my name? {{ $name ?? '' }}
```
```
OUTPUT: arvind
```


