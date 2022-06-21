## Section Insights

**Eloquent**

- Eloquent is an object relational mapper (ORM) that is included by default within the Laravel framework.

```
//Reading data using eloquent

Route::get('/read',function()
{

    foreach($posts as $post){
        return $post->title;
    }

});

//nserting data using eloquent

Route::get('/insert',function()
{
   
     $post = Post::find(2);

     $post->title = "New title";
     $post->content = "New content";
     
     $post->save();
    }

});

//Updating with eloquent

Route::get('/update',function()
{
   
     $post::where('id',2)->where('is_admin', 0)->update(['title'=>'content'='Hello done updating']);

     $post->title = "New";
     
     $post->save();
    }

});

//Softdeleting / Trashing

Route::get('/softdelete',function()
{
   
     Post::find(1)->delete();


});


