## Section Insights 

**Views**

- Views contain the html code required by your application, and it is a method in Laravel that separates the controller logic and domain logic from the presentation logic.

- Views are located in laravel project `resources\views`

**Passing data to views**

Here is the example code of passing data to views

  ```public function show_post($id)
    {
        return view('post')->with('id',$id);
  }
  
  {
  return view('post',compact('id'));
  }