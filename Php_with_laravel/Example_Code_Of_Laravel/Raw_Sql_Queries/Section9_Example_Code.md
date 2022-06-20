```
//Inserting Data Example Code

 Route::get('/insert', function()
 {
  DB::insert('insert into post (title, body) values (?, ?)', [ 'Hi', ' This is the body that i mmake']);
     
      });

//Reading Data Example Code

Route::get('/read', function()
{
        $results = DB::select('select * from post');
        foreach ($results as $post){
            return $post->title;
        }
      });

//Updating Data Example Code

Route::get('/update',function()
{
    $update = DB::update('update post set title = "Title has been updated" where id=?', [5]);
    if ($update = 1) {
        return ('Hello done updated');
    }
});

//Deleting Data Example Code

Route::get('/delete', function()
{
  DB::deleted('delete from post  where id=?', [4]);
  return ('destroy');
});


