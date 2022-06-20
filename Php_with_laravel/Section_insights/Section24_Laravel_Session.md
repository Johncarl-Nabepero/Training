## Section Insight and Example Code

**Laravel Session**

- Sessions are used to store information about the user across the requests.

```
    /**
     * Show the application dashboard.
     *
     * @return \Illuminate\Contracts\Support\Renderable
     */
    public function index(Request, $request)    
    {

        $request->session(['edwin'=>master instructor]);
        return view('home');
    }
}
