### Directices
```
 v-bind, v-cloak, v-for, v-else, v-else-if, v-model, v-on, v-once, v-text, and v-html.
```

* v-model
```
v-model directive is used to make forms reactive; it helps us update data on user input events.

<!-- HTML -->
<div id="app">
  <span>Enter the weight in kilograms:</span>
  <input v-model="someNum" type="number">
  <div>The weight in pounds is: {{ someNum * 2.20 }}</div>
</div>

// js
new Vue({
  el: '#app',
  data() {
    return {
      someNum: 1
    }
  }
})
```




### Data

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

### method 
methods property is where Vue apps store their instance methods. These methods can be used in many situations, such as helper functions used in other methods or event handlers (functions that are called in response to specific user interactions).

```
const app = new Vue({
  el: "#app",
  data: {
    hoursStudied: 300
  },
  methods: {
    resetProgress: function () {
      this.hoursStudied = 0;
    }
  }
});

<button v-on:click="resetProgress">Reset Progress</button>
```

### Dynamic Class

* Object
```
   <ul>
      <li v-for="item in items" :class="{strikeout: item.purchased}">{{ item.label }}</li> 
    </ul>

---

items: [
          {
            label:'10 party hats',
            purchased: false,
            highPriority:false
          },
          {
            label:'2 board games',
            purchased:true,
            highPriority:false
          },{
            label:'20 cups',
            purchased:false,
            highPriority:false
          }
]
```


* Array

```
    <ul>
      <li v-for="item in items" :class="[item.purchased ? 'strikeout': '']">{{ item.label }}</li> 
    </ul>

---

items: [
          {
            label:'10 party hats',
            purchased: false,
            highPriority:false
          },
          {
            label:'2 board games',
            purchased:true,
            highPriority:false
          },{
            label:'20 cups',
            purchased:false,
            highPriority:false
          }
]

```

// change data use methods
// change presentation of existing data use computed property
