## Section Insights and Example code

**Relation and Mass Assignment**

- The process of sending an array of data to the specified model at once is known as mass assignment.

**Example code of Post model**

``` 
public function comment(){

 return $this->hasMany['app\Post'];

}