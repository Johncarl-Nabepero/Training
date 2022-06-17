## Section Insights and Example code**

**Laravel Tinker**

- Tinker allows you to interact with a database without creating the routes.

**Creating data with tinker**

```cms:php artisan tinker
Psy Shell v0.11.1 (PHP 8.1.1 — cli) by Justin Hileman
>>> $post = App
PHP Parse error: Unexpected character "" (ASCII 31) on line 1
>>> $post = App\Models\Post::create(['title'=>'PHP post from tinker' , 'body'=>'This is body']) ;
=> App\Models\Post {#3521
     title: "PHP post from tinker",
     body: "This is body",
     updated_at: "2022-02-18 03:50:49",
     created_at: "2022-02-18 03:50:49",
     id: 3,
   }

Finding record using constraints in tinker

>>> $post = App\Models\find(6);
PHP Error:  Call to undefined function App\Models\find() in Psy Shell code on line 1
>>> $post = App\Models\Post::find(6);
=> null
>>> $post = App\Models\Post::find(3);
=> App\Models\Post {#3536
     id: 3,
     title: "PHP post from tinker",
     body: "This is body",
     created_at: "2022-02-18 03:50:49",
     updated_at: "2022-02-18 03:50:49",
     is_admin: 0,
     deleted_at: null,
   }

Update with tinker

>>> $post->content = "updated record 3";
>>> $post->save();
=> true

Deleting with tinker

>>> $post = App\Models\Post::onlyTrashed()
=> Illuminate\Database\Eloquent\Builder {#3506}
>>> $post->forcedelete()
=> 0



