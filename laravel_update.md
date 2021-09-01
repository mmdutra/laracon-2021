# Laravel Update 

Laravel 9 will be launched in January 2022

### API authentication

- Auth sanctum as default authentication, with token 

### Models

**Prunable trait**
  - Method "prunable" 
    - Get the prunable model query (query of the resources can be punables)
  - Method Pruning
    - Prepare the model for pruning

**Queue monitoring**

* Command ```queue:monitor```, describe the queues details (connection, queue name, size, status)
* Listener to the queue to create alerts on queue status

**Events**
```php
Event::listen(Class1Name::class);
Event::listen(Class2Name::class);
```

```php
Event::listen(function (Class1Name|Class2Name $event) {});
```

**Validation**

Add the method ```$validator->safe()```, that provides a new contract with the validated data

Add the indexes of arrays can be accepteds on a input key 

```php
[
    'users' => 'required|array:name,email'
}
```

**Where relation**
```php
return User:whereHas('posts', function ($query) {
    $query->where('posts.created_at', '<=', now()->subMonths(1))->get();
});
```

```php
return User:whereRelation(
    'posts', 'posts.created_at', '<=', now()->subMonths(1)
)->get();
```