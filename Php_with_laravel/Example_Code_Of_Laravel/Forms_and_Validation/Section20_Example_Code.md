```
Route::get('/dates', function()
{    

$date = new DataTime('+1 week');

echo $data->format('m-d-Y');

});
```

**Accessors**

- Laravel Accessors and Mutators are custom, user defined methods. Accessors are used to format the attributes when you retrieve them from database.

```
Route::get('/getname',function()
{

$user = User::find(1);

echo $user->name;

});