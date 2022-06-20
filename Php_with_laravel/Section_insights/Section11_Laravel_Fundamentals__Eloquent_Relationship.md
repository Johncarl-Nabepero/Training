## Section Insights and Example Code 

**One to One Relationships**

-  Is a fundamental relation. For example, the User model has only one Bank Account, so he has one account number. So we can connect both models, User, and Bank, as a one-to-one relationship with each other.

- Here's the code of adding an user_id for one to one

   ```public function up()
    {
        Schema::create('failed_jobs', function (Blueprint $table) {
            $table->id();
            $table->user_id();
            $table->text('connection');
            $table->text('queue');
            $table->longText('payload');
            $table->longText('exception');
            $table->timestamp('failed_at')->useCurrent();
        });
    }


**One to Many Relationships**

- A one-to-many relationship in Laravel defines as a Single model owning multiple models.

   ```public function up()
    {
        Schema::create('user_roles', function (Blueprint $table) {
            $table->id();
            $table->user_id();
            $table->role_id();
            $table->timestamps();
        });
    }
     Notes: After you add a user_id and role_id you need to migrate it to your terminal so that they will added to your database. 


**Has Many Through Relation**

- A hasManyThrough relationship indicates a many-to-many relationship with another model.

**Polymorphic Relation**

- A Polymorphic connection occurs when a model belongs to multiple types of models but only to one association.

```posts
    id - integer
    name - string

users
    id - integer
    name - string


