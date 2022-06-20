```
//Inserting using polymorphic

Route::get('/create/{photo}', function ($photo) {
  $staff = Staff::find(1);
  $staff->photos()->create(['path'=>$photo]);
  return ('Created successfully');
});


//Reading using polymorphic

Route::get('/read', function () 
{
  $staff = Staff::find(1);

  foreach($staff->photos as $photo){
    echo $photo->path;
  }
});

//Updating using polymorphic

Route::get('/update/{id}/{update}', function ($id,$update)
 {
  $staff = Staff::findOrFail(1);

  $photo = $staff->photos()->whereId($id)->first();
  $photo->path = $update;
  $photo->save();
  return ('Updated Success');
});

//Deleting using polymorphic

Route::get('/delete/{id}', function ($id)
 {
  $staff = Staff::findOrFail(1);
  $staff->photos()->whereId($id)->delete();
  return ('Delete Success);
});

//Assign using polymorphic

Route::get('/assign', function () 
{
  $staff = Staff::findOrFail(2);
  $photo = Photo::findOrFail(4);

  $staff->photos()->save($photo);
}






