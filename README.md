# Front End Snippets For Sublime Text

## basic js

#### Multiline comment

##### Tab Trigger:  _*

```js
/*
* message
*/
```  

#### console.log()

##### Tab Trigger:  _log

 
```js
console.log();
``` 

#### for loop

##### Tab Trigger:  _for

 
```js
var len = array.length;
for(var ii = 0; ii < len; ii++){
  var cur = array[ii];
  /* code ... */
}
```  

#### for-in loop

##### Tab Trigger:  _forin

 
```js
for (var key in object){
 if (object.hasOwnProperty(key)){
   var value = object[key];
 }
}
```  

#### Google Analytics

##### Tab Trigger:  _ga

 
```js
var _gaq = _gaq || [];
  _gaq.push(['_setAccount', '${1:UA-XXXXX-X}']);
  _gaq.push(['_trackPageview']);

  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();
```
 

#### switch statement

##### Tab Trigger:  _switch

 
```js
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

#### ternary statement

##### Tab Trigger:  _?

 
```js
condition ? true : false;
```  

#### try / catch / finally

##### Tab Trigger:  _try

 
```js
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


#### Array.filter()

##### Tab Trigger:  _filter

 
```js
var filtered = array.filter(
    function(element){ 
      return true|false; 
    }
  );  
```    

#### Array.sort()

##### Tab Trigger:  _sort

 
```js
items.sort(function (a, b) {
  if (${1:a > b}){
    return 1;
  }
  if (${2:a < b}){
    return -1;
  }
  // a must be equal to b
  return 0;
});  
```  

#### setTimeout

##### Tab Trigger:  _timeout

 
```js
setTimeout(function(){},delay);
```  

#### named function

##### Tab Trigger:  _function

 
```js
function method(arguments){
  /* code ... */
}
```  

## advanced js

#### iife

##### Tab Trigger:  _iife

 
```js
(function(){
  /* code */
})();
``` 

#### Class boilerplate

##### Tab Trigger:  _class

```js
    function ClassName (param) {

      this.publicVar = 'foo';
      var privateVar = 'bar';

      var that = this;

      function privateMethod(){
        /* 
        * this method can be accessed by
        * privileged methods but not by
        * public methods.
        */
      }

      this.privilegedMethod = function(){
        /* 
        * this method has access to both
        * the public and private properties
        * of the object
        */
      }
    }

    ClassName.prototype.publicMethod = function() {};
``` 

#### Singleton

##### Tab Trigger:  _singleton

```js
     var ClassName;
    (function() {
        var instance;

        ClassName = function ClassName() {
            if (instance) {
                return instance;
            }

            instance = this;

            /* code */
        };
    }());
``` 

#### Promise

##### Tab Trigger:  _promise

  ```js
     var promise = new Promise(function(resolve, reject) {

      var success;

      /* code */

      if (success) {
        resolve();
      }
      else {
        reject(Error());
      }
    });

    promise.then(
      function(result) {
        console.log(result);
      },
      function(err) {
        console.log(err);
      }
    );
``` 


#### Promise (then)

##### Tab Trigger:  _then

```js
   promise.then(
    function(result) {
      console.log(result);
    },
    function(err) {
      console.log(err);
    }
  );
``` 

## jQuery snippets

#### $.ajax()

##### Tab Trigger:  _$ajax

   ```js
    $.ajax({
      url: '',
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


#### $(document).ready()

##### Tab Trigger:  _$dr

     ```js
    $(document).ready(function(e){
      /* code ... */
    });
    ``` 


#### $(function)

##### Tab Trigger:  _$fn

     ```js
    $(function() {
      /* code ... */
    });
    ``` 

#### $('.selector').on()
##### Tab Trigger:  _$on

     ```js
    $('selector').on('event', function(e){
      /* code ... */
    });
    ```

    #### plugin boilerplate

    ##### Tab Trigger:  _plugin

     ```js
    (function($){

      var ClassName = function (element, options){

        this.$element  = $(element);

        // plugin options
        this.options   = $.extend({}, ClassName.DEFAULTS, options);

        var that = this;

      };

      ClassName.DEFAULTS = {};

      var old = $.fn.pluginName;

      $.fn.pluginName = function (option) {
        return this.each(function () {
          var $this   = $(this);
          var data    = $this.data('pluginName');
          var options = typeof option === 'object' && option;
          if (!data){
            $this.data('pluginName', (data = new ClassName(this, options)));
          }
        });
      };

      $.fn.pluginName.Constructor = ClassName;

      $.fn.pluginName.noConflict = function() {
        $.fn.pluginName = old;
        return this;
      };

    })(jQuery);
    ``` 

#### publish [(tiny pub/sub)](https://github.com/cowboy/jquery-tiny-pubsub)

##### Tab Trigger:  _publish

     ```js
      $.publish('whatever.event.name',payload);
    ``` 

#### subscribe [(tiny pub/sub)](https://github.com/cowboy/jquery-tiny-pubsub)

##### Tab Trigger:  _subscribe

    ```js
      function handlerFunction(){
        return function(_,data){
          console.log('subscribe ',data);
        };
      }

      $.subscribe('whatever.event.name',handlerFunction());
    ```        

              

             

## html snippets

#### .html page

##### Tab Trigger:  _html

  ```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>page</title>
    <meta name="description" content="">
    <meta name="viewport" content="width=device-width">

    <link rel="stylesheet" href="">

    </head>
    <body>
      <main>

      </main>
      <script type="text/javascript" src=""></script>
  </body>
</html>
``` 

#### video tag

##### Tab Trigger:  _video

```html
<video controls preload="auto" width="640" height="264" poster="PATH_TO_ASSETS.png">
 <source src="PATH_TO_ASSETS.mp4" type='video/mp4' />
 <source src="PATH_TO_ASSETS.webm" type='video/webm' />
 <source src="PATH_TO_ASSETS.ogv" type='video/ogg' />
</video>
``` 
        

## css snippets


#### responsive breakpoint

##### Tab Trigger:  _breakpoint

```css
@media all and (min-width: 50em) {

}
``` 


#### animation @keyframes

##### Tab Trigger:  _keyframes

```css
    @-webkit-keyframes ANIMATION_NAME {
      0%   {  }
      100% {  }
    }
    @-moz-keyframes ANIMATION_NAME {
      0%   {  }
      100% {  }
    }
    @-o-keyframes ANIMATION_NAME {
      0%   {  }
      100% {  }
    }
    @keyframes ANIMATION_NAME {
      0%   {  }
      100% {  }
    }
```

#### transition

##### Tab Trigger:  _transition

```css
    -webkit-transition-property: all;
    transition-property: all;

    -webkit-transition-duration: 750ms;
    transition-duration: 750ms;

    -webkit-transition-timing-function: ease-in;
    transition-timing-function: ease-in;

    -webkit-transition-delay: 500ms;
    transition-delay: 500ms;
``` 

              

             

## regular expression snippets

#### alphanumeric

##### Tab Trigger:  _regex_alphanumeric

 ```js
 /^[0-9a-zA-Z]+$/
``` 

#### email

##### Tab Trigger:  _regex_email

 ```js
 /^\s*[\w\-\+_]+(\.[\w\-\+_]+)*\@[\w\-\+_]+\.[\w\-\+_]+(\.[\w\-\+_]+)*\s*$/;
``` 

#### url

##### Tab Trigger:  _regex_url

 ```js
 /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
``` 


## misc. snippets


#### .gitignore

##### Tab Trigger:  _gitignore

 
```bash
# osx noise
.DS_Store

# svn & cvs
.svn
CVS

*.log
node_modules
bower_components

# project specific
```