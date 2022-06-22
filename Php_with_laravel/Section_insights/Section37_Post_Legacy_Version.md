## Section Insights and Example code

- I learned this section is more about of how display a post and edwin explain it properly.

- Edwin teach us of how to create a from 

**This is the example code of database migration form**'

{!! Form::open(['method'=>'POST','action'=>'AdminPostController@store']) !!}

<div class="form-group">

   {!! Form::label('title', 'Title:') !!}
   {!! Form::text('title',null,['class'=>'form-control'])!!}

</div>