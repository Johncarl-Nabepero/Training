## Section Insights and Example Code 

- Installing a laravel project 

- API is a software intermediary that allows two applications to talk to each other. 

**Sending Email Route**
```
Route::get('/',function()
{
  $data = [

    'title'=> 'Hi Student';
    'content'=> 'This laravel course created';
  ]
  Mail::send('');

  NOTES: Create a views folder email/test. 

});