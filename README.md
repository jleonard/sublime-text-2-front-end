# Sublime Text 2 Front End

> ### Snippets for [.js](#javascript-snippets), [jQuery](#jquery-snippets), html and [css](#css-snippets)

## javascript snippets

####multiline comment   

``_*``


```
/*
* message
*/
```

####function  

``_fn``


```
function ${1:method}(${2:arguments}){
  ${0:/* code ... */}
}
```

####for

``_for``


```
var len = 5;
for(var ii = len - 1; ii >= 0; ii - 1){
  /* code ... */
}
```

####for in loop

``_forin``


```
for (var key in object) {
   if (object.hasOwnProperty(key)) {
      var value = object[key]; 
   }
}

```

####iife (immediately-invoked function expression)

``_iife``


```
(function(){
  /* code */
})();
```

####log 

``_log``


```
console.log()
```

####switch 

``_switch``


```
switch(var){
  case :
    /* code ... */
  break;
  case :
    /* code ... */
  break;
  default:
    /* code ... */
  break;
}
```

####ternary 

``_?``


```
condition ? true : false;
```

####timeout

``_timeout``


```
setTimeout(function,delay);
```

####try / catch / finally

``_try``


```
try {
  /* code... */
} 
catch (e) {
   /* code... */
}
finally (e) {
   /* code... */
}
```

## jquery snippets
####$.ajax()
``_$ajax``


```
$.ajax({
  url: "",
  data: {}
})
.done(function ( data ) {
  /* code ... */
})
.fail(function(jqXHR,textStatus){
  /* code ... */
})
.always(function(jqXHR,textStatus){
  /* code ... */
});
```

### $(document).ready()
``_$dr``


```
$(document).ready(function(e){
  /* code ... */
});
```

### $(function(){})
``_$fn``


```
$(function() {
  /* code ... */
});
```

### $("").on()
``_$on``


```
$('selector').on('event', function(e){
  /* code ... */
});
```

## css snippets

### @keyframes
``keyframes``

```
@-webkit-keyframes ANIMATION_NAME {
  0%   { opacity: 0; }
  100% { opacity: 1; }
}
@-moz-keyframes ANIMATION_NAME {
  0%   { opacity: 0; }
  100% { opacity: 1; }
}
@-o-keyframes ANIMATION_NAME {
  0%   { opacity: 0; }
  100% { opacity: 1; }
}
@keyframes ANIMATION_NAME {
  0%   { opacity: 0; }
  100% { opacity: 1; }
}
```
