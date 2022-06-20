``` 
  //Inserting data using polymorphic many to many

Route::get('/create', function(){

  $post = Post::create(['name'=>'Johncarl Post']);
  
  $tag  = tag::find(1);

  $post->tags()->($tag);
  

});

 //Reading data using polymorphic many to many

 Route::get('/read',function()
 {
 $post = Post::findorfail(1){

    foreach($post->tags as tag){
        echo $tag;

    }
      }
 });
 

 //Updating data using polymorphic many to many

 Route::get('/update', function()
 {
     
     $post = Post::findOrfail(1);

     foreach($post=>tags as $tag){
      $tag = whereName('PHP')->update(['name'='Updated Php]); 
     }


 });

  //Deleting data using polymorphic many to many

Route::get('/delete', function()
{

  $post = Post::find(1);
  
  foreach($post->tags as $tag){

    $tag->whereId(2)->delete();
  }
})

 





