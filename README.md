# Konnco Studio - Laravel Code Style

## Introduction
Maybe many of the new kids who applied at Konnco Studio are a little confused about how to write laravel code at Konnco Studio, so please read this document carefully.

## Coding Style

### Variables
Always use camel case to write variables
```php
$order_detail; // BIG NO!
$OrderDetail; // BIG NO!
$orderDetail; // BIG NO!
```

### Controllers

### Models
Jika kamu sering menggunakan suatu filter sebagai contoh status publish kamu bisa menambahkan scope publish pada modelmu, sebagai contoh :
```php
Class Post extends Model {
    public function scopeWherePublished($query){
        return $query->where('status','PUBLISHED');
    }
}
```
```php
$post = Post::wherePublished()->get();
```

### Jobs
### Routings

Always use the import class, to make it easier for the IDE to identify files, and also make it easier for you to open the controller in use.
```php
Route::resource('payment', OrderApiController::class]);
Route::get('payment', [OrderApiController::class, 'index']);
```