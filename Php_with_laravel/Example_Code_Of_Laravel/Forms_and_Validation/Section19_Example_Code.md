```
@extends('layouts.app')


@section('content')

<h1>Create Post</h1>

 {!! Form::open(['method'=>'POST', 'action'=>'PostController@store']) !!}

  <input type="text" name="title" placeholder="Enter Title">

  <input type="submit" name="submit">

</form>

```