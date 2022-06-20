```
   // Creating data

Route::get('/create/{address}', function ($address) 
{
    $user = User::findOrFail(1);
    $address = new Address(['address'=>$address]);
    $user->address()->save($address);
    return ('Address added in database '). $address->address;

});

//Reading data 

Route::get('/read', function()
{

    $user = User::findOrFail(1);
    echo $user->address->address;

});

//Updating data

Route::get('/update' ,function()
{
$address = Address::whereUserId(1)->first();
$address->address = "Mandaue city";
$address->save();
return  ('Address Updated '). $address->address;
});

//Deleting data

Route::get('/destroy', function()
{

    $user = User::findOrFail(1);
    $user->address()->destory();

    return ('Destroy');
});