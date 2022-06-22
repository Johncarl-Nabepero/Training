## Section Insights and Example Code 

 **Setting up views and routes** 
 
 -  Routes are defined in your route files, which are located in the routes directory.

 `Route::resource('/posts','PostsController');`

 ** Persisting data to database **

 ``` public function store(Request $request)
    {
       // post::create($request->all());

       $input = $request->all();

        $input['title'] = $request->title;

        Post::create($request->all());
    }
```

  **Commands**

 Make sure you have App\Post in the top of your controller.

 **Reading data**
 
```  
  /**
     * Display a listing of the resource.
     *
     * @return \Illuminate\Http\Response
     */
    public function index()
    {
        $posts  = Post:all();
        return view('posts.index', compact('posts'));
    }


   /**
     * Show the form for creating a new resource.
     *
     * @return \Illuminate\Http\Response
     */
    public function create()
    {
       return view('posts.create');
    }
```






