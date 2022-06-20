## Section Insights and Example code 

**Example of a regular form for files**
```
<form action="/uploadfile" method="post" enctype="multipart/form-data">
    @csrf
    <div class="form-group">
        <input type="file" class="form-control-file" name="fileToUpload" id="exampleInputFile">
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

**Modifying create view for file**

```
<h1>Create Post</h1>

 {!! Form::open(['method'=>'POST', 'action'=>'PostController' 'files'=>true]) !!}

  <div> class"form-group">
    {!! Form::file('file', ['class'=>form-control])!!}

  </div>

</form>