# ASYNCHRONOUS LARAVEL

### Definition of ASYNC

- Different tasks can be executed at the same time
- A taks doesnt have to wait another task finish to execute

### Two tipes of processing tasks 

* **CPU-bound** 
  - math calc
  - graphic processing
  - processing audio

* **I/O-bound**
  - http requests
  - database connections
  - send emails

### Laravel Octane

- A lib that uses php-swoole to give a async application for laravel 

```php
[$response, $results, $cache] = Octane::concurrently([
    fn::http(),
    fn::query(),
    fn::cache()
]);
```

### References
- Mastering swoole PHP
- Laravel queues in action
