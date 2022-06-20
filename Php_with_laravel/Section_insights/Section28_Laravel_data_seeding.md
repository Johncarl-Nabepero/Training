## Section Insights

**Data Seeding**

- Laravel includes the ability to seed your database with data using seed classes. All seed classes are stored in the database/seeders directory. By default, a DatabaseSeeder class is defined for you.

- Seeders run in your terminal `php artisan db:seed`

**You can add database seeder in your laravel project by putting this in your terminal.**

```
PS C:\xampp\htdocs\seeder> php artisan make:seeder UsersTableSeeder
Seeder created successfully.


 public function run()
    {
        DB::table('users')->insert([
            'name' => Str::random(10),
            'email' => Str::random(10).'@gmail.com',
            'password' => Hash::make('password'),
        ]);
 
 