## Setion Insight and Example Code

**Eloquent One to Many Relationship**

- In a one-to-many relationship, one record in a table can be associated with one or more records in another table.


**HERE IS THE EXAMPLE CODE**

```
//Creating data

Route::get('/create/{title}/{body}', function ($title,$body)
 {
    $user = User::findOrFail(1);
    $post = new Post(['title'=>$title,'New title '=> $body]);

    $user->posts()->save($post);
    foreach($user->posts as $posts)
    {
        return ("Done Creating post :"). $posts->title. (""). $posts->body;
    }
 
});

//Reading data

Route::get('/read', function () {
    $user = User::findOrFail(1);
    foreach($user->posts as $post)
    {
        echo $post->title.
         "<br>";
    }
    
});


//Updating data 

Route::get('/update/{id}/{title}/{body}', function ($id,$title,$body) 
{
    $user = User::findOrFail(1);
    $user->posts()->whereId($id)->update(['title'=>$title,'New title'=>$body]);   
    foreach($user->posts as $post)
    {
        echo ('Updating post '). $id . "<hr>";
        return $post->title. "<br>" . $post->body;
    }
});

//Deleting data 


Route::get('/destroy/{id}', function ($id)
 {
    $user = User::findOrFail(1);
    $user->posts()->whereId($id)->destroy();   
    echo ('Done Destroying');
});
