## Section Insight and Example code

**One to One Relationship**

- In a one-to-one relationship, one record in a table is associated with one and only one record in another table.

1. Create a new Laravel installation called onetoone

2. Create a database with the same name onetoone

3. Make sure your database setting is in your .env file so that you may connect to it of course.


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