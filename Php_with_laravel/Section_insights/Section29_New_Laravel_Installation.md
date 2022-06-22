## Section Insights and Example Code 

**Creating components**

- In the App\Resources\Views i learn how to make a folder name Components then make `master.blade.php`.

- Sections, layouts, and inclusions all give similar benefits; nevertheless, some people may find the mental model of components and slots easier to grasp. Components can be written in two ways: class-based components and anonymous components.

```
<?php

use Illuminate\Database\Seeder;

class DatabaseSeeder extends Seeder
{
    /**
     * Seed the application's database.
     *
     * @return void
     */
    public function run()
    {
        factory( class: 'App\User', amount:10)->create();
    }
}
```

`Run : php artisan db:seed`