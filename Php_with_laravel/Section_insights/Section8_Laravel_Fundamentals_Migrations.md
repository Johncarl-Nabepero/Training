## Section Insights and Example Code

**Environment Configuration**

- The two environment files is .env and .env example.

**Migrations**

- Laravel Migration is an essential feature in Laravel that allows you to create a table in your database.

- Create a database and modify the .env database text same to your database name that you make.

**Creating Migration**

- By creating a migration you need to make a database field name first in the `Database\Migrations\` Folder then after that you can use `Php artisan migrate` to your terminal. 

**Here is the example of code database migration**

  ```public function up()
    {
        Schema::create('users', function (Blueprint $table) {
            $table->id();
            $table->string('name');
            $table->string('email')->unique();
            $table->timestamp('email_verified_at')->nullable();
            $table->string('password');
            $table->rememberToken();
            $table->timestamps();
        });
    }



   
