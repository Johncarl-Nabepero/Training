## Section Insights and Example Code 

**Many to Many Relationship**

- A many-to-many relationship occurs when multiple records in a table are associated with multiple records in another table.

1. Create a new Laravel installation called manytomany

2 Create a database with the same name manytomany

3. Make sure your database setting is in your .env file so that you may connect to it of course.

```
//Creating data

Route::get('/create', function () 
{
 $user = User::find(1);
 $user->roles()->save(new Role(['name'=>'Admin']));

 return ('Success created');
});

//Reading data

Route::get('/read', function () 
{
    $user = User::findOrFail(1);
    foreach ($user->roles as $role
    {
        echo $role->name;
    }
});

//Updating data

Route::get('/update', function ()
 {
    $user = User::findOrFail(1);

    if($user->has('roles')){

        foreach($user->roles as $role){

            if($role->name == 'Admin')
            {
                $role->name = "Edwin";
                $role->save();
                return ('Done Updating!!');
            }

        }
    }

});

//Deleting data

Route::get('/delete/{id}', function($id)
{
$user = User::findOrFail(1);
foreach ($user->roles as $role)
 {
    $role->whereId($id)->delete();
}
// $user->roles()->delete();
});


//Detach an user

Route::get('/detach', function()
{

    $user = User::findOrFail(1);
    $user->roles()->detach(3);
    
});

//Sync a user

Route::get('/sync', function()


    $user = User::findOrFail(1);
    $user->roles()->sync([2,]);
});