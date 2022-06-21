```
Route::get('/dates', function()
{    

$date = new DataTime('+1 week');

echo $data->format('m-d-Y');

});


Route::get('/getname',function()
{

$user = User::find(1);

echo $user->name;

});