## Section Insights and Example code

**Eloquent Polymorphic Many to Many Relationship**

- A polymorphic relationship is used when you want something like Many to Many relationship, but without having to create extra tables every time you want to add a new Model to the mix

**Summary**

- Creating a Laravel Project with the database, 4 models and 4 migrations.

1. Create a new Laravel installation called polymorphicmanytomany

2. Create a database with the same name polymorphicmanytomany

3. Create 4 models, Post, Video, Tag and Taggable; here is a reminder of how we do that below

`php artisan make:model Post -m` 

`php artisan make:model Video -m`

`php artisan make:model Tag -m`

**CSRF** 

- Cross-site request forgeries are a sort of malicious exploit in which an authenticated user is used to execute unauthorized commands

**HERE IS THE EXAMPLE CODE**

``` 
  //Inserting data using polymorphic many to many

Route::get('/create', function(){

  $post = Post::create(['name'=>'Johncarl Post']);
  
  $tag  = tag::find(1);

  $post->tags()->($tag);
  

});

 //Reading data using polymorphic many to many

 Route::get('/read',function(){
 $post = Post::findorfail(1){

    foreach($post->tags as tag){
        echo $tag;
        
    }
 }

 })





