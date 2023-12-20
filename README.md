* Data Object
```
<div id="entryPoint">
  <h1>{{heading1}} </h1>
  <h2>{{heading2}} </h2>
  <p>{{paragraph1}} is fun</p>
</div>

new Vue({
  el:'#entryPoint',
  data:{
    heading1: 'Just an h1 heading here',
    heading2: 'heading 2 here',
    paragraph1: 'Vue JS'
  }
})
```

* Nested Data Object
```
<ul>
  <li v-for="entry in entries">
     {{ entry.content }}
  </li>
</ul>

var listExample = new Vue ({
  el: "ul",
  data: {
    entries: [
      { content: 'a'},
      { content: 'b'},
      { content: 'c'}
    ]
  }
})
```
