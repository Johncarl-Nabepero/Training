## Section Insights and Example Code 

**Creating components**

- In the App\Resources\Views make a folder name Components then make `master.blade.php`

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