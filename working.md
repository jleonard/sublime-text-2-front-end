# Front End Snippets <sub>For Sublime Text</sub>

## basic js

          <!-- js comment -->

#### Multiline comment

##### Tab Trigger:  _*

```js
/*
* message
*/
```  

          <!-- js comment -->

#### console.log()

##### Tab Trigger:  _log

 
```js
console.log();
```  

          <!-- for -->

#### for loop

##### Tab Trigger:  _for

 
`var len = array.length;
for(var ii = 0; ii < len; ii++){
  var cur = array[ii];
  /* code ... */
}
`  

          <!-- for in -->

#### for-in loop

##### Tab Trigger:  _forin

 
`for (var key in object){
 if (object.hasOwnProperty(key)){
   var value = object[key];
 }
}
`  

          <!-- google analytics -->

#### Google Analytics

##### Tab Trigger:  _ga

 
`var _gaq = _gaq || [];
  _gaq.push(['_setAccount', '${1:UA-XXXXX-X}']);
  _gaq.push(['_trackPageview']);

  (function() {
    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
  })();
`
 

          <!-- switch -->

#### switch statement

##### Tab Trigger:  _switch

 
`switch(var){
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
`  

          <!-- terary -->

#### ternary statement

##### Tab Trigger:  _?

 
`condition ? true : false;
`  

          <!-- try/catch -->

#### try / catch / finally

##### Tab Trigger:  _try

 
`try {
  /* code... */
} 
catch (e) {
   /* code... */
}
finally (e) {
   /* code... */
}
`  

          <!-- filter -->

#### Array.filter()

##### Tab Trigger:  _filter

 
`var filtered = array.filter(
    function(element){ 
      return true|false; 
    }
  );  
`    

          <!-- array filter -->

#### Array.sort()

##### Tab Trigger:  _sort

 
`items.sort(function (a, b) {
  if (${1:a > b}){
    return 1;
  }
  if (${2:a < b}){
    return -1;
  }
  // a must be equal to b
  return 0;
});  
`  

          <!-- setTimeout -->

#### setTimeout

##### Tab Trigger:  _timeout

 
`setTimeout(function(){},delay);
`  

          <!-- function -->

#### named function

##### Tab Trigger:  _function

 
`function method(arguments){
  /* code ... */
}
`  

## advanced js

          <!-- iife -->

#### iife

##### Tab Trigger:  _iife

 
`(function(){
  /* code */
})();
` 

          <!-- class -->

#### Class

##### Tab Trigger:  _class

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
    ` 

              <!-- singleton -->

    #### Singleton

    ##### Tab Trigger:  _singleton

     `var ClassName;
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
    ` 

              <!-- promise -->

    #### Promise

    ##### Tab Trigger:  _promise

     `var promise = new Promise(function(resolve, reject) {

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
    ` 

              <!-- then -->

    #### Promise (then)

    ##### Tab Trigger:  _then

     `promise.then(
      function(result) {
        console.log(result);
      },
      function(err) {
        console.log(err);
      }
    );
    ` 

              

             

    ## jQuery snippets

              <!--ajax-->

    #### $.ajax()

    ##### Tab Trigger:  _$ajax

     `
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
    ` 

              <!--document ready-->

    #### $(document).ready()

    ##### Tab Trigger:  _$dr

     `
    $(document).ready(function(e){
      /* code ... */
    });
    ` 

              <!--function-->

    #### $(function)

    ##### Tab Trigger:  _$fn

     `
    $(function() {
      /* code ... */
    });
    ` 

              <!--on-->

    #### $('.selector').on()

    ##### Tab Trigger:  _$on

     `
    $('selector').on('event', function(e){
      /* code ... */
    });
    ` 

            <!-- plugin -->

    #### plugin boilerplate

    ##### Tab Trigger:  _plugin

     `
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
    ` 

    #### publish [(tiny pub/sub)](https://github.com/cowboy/jquery-tiny-pubsub)

    ##### Tab Trigger:  _publish

     `
      $.publish('whatever.event.name',payload);
    ` 

    #### subscribe [(tiny pub/sub)](https://github.com/cowboy/jquery-tiny-pubsub)

    ##### Tab Trigger:  _subscribe

      `
      function handlerFunction(){
        return function(_,data){
          console.log('subscribe ',data);
        };
      }

      $.subscribe('whatever.event.name',handlerFunction());
    `        

              

             

    ## html snippets

              <!-- html -->

    #### .html page

    ##### Tab Trigger:  _html

     `&lt;!DOCTYPE html&gt;
    &lt;html&gt;
      &lt;head&gt;
        &lt;meta charset="utf-8"&gt;
        &lt;meta http-equiv="X-UA-Compatible" content="IE=edge"&gt;
        &lt;title>page&lt;/title&gt;
        &lt;meta name="description" content=""&gt;
        &lt;meta name="viewport" content="width=device-width"&gt;

        &lt;link rel="stylesheet" href=""&gt;

        &lt;/head&gt;
        &lt;body&gt;
          &lt;main&gt;

          &lt;/main&gt;
          &lt;script type="text/javascript" src=""&gt;&lt;/script&gt;
      &lt;/body&gt;
    &lt;/html&gt;
    ` 

              <!-- video -->

    #### video tag

    ##### Tab Trigger:  _video

     `&lt;video 
      controls preload="auto" width="640" height="264"
      poster="PATH_TO_ASSETS.png"&gt;
     &lt;source src="PATH_TO_ASSETS.mp4" type='video/mp4' /&gt;
     &lt;source src="PATH_TO_ASSETS.webm" type='video/webm' /&gt;
     &lt;source src="PATH_TO_ASSETS.ogv" type='video/ogg' /&gt;
    &lt;/video&gt;
    ` 

              

             

    ## css snippets

              <!-- breakpoints -->

    #### responsive breakpoint

    ##### Tab Trigger:  _breakpoint

     `
    @media all and (min-width: 50em) {

    }
    ` 

            <!-- keyframes -->

    #### animation @keyframes

    ##### Tab Trigger:  _keyframes

     `
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
     `

            <!-- css transition -->

    #### transition

    ##### Tab Trigger:  _transition

     `
    -webkit-transition-property: all;
    transition-property: all;

    -webkit-transition-duration: 750ms;
    transition-duration: 750ms;

    -webkit-transition-timing-function: ease-in;
    transition-timing-function: ease-in;

    -webkit-transition-delay: 500ms;
    transition-delay: 500ms;
    ` 

              

             

    ## regular expression snippets

              <!-- alphanumeric -->

    #### alphanumeric

    ##### Tab Trigger:  _regex_alphanumeric

     `/^[0-9a-zA-Z]+$/
    ` 

              <!-- email -->

    #### email

    ##### Tab Trigger:  _regex_email

     `/^\s*[\w\-\+_]+(\.[\w\-\+_]+)*\@[\w\-\+_]+\.[\w\-\+_]+(\.[\w\-\+_]+)*\s*$/;
    ` 

              <!-- url -->

    #### url

    ##### Tab Trigger:  _regex_url

     `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
    ` 

              

             

    ## misc. snippets

              <!-- gitignore -->

    #### .gitignore

    ##### Tab Trigger:  _gitignore

     
    `# osx noise
    .DS_Store

    # svn & cvs
    .svn
    CVS

    *.log
    node_modules
    bower_components

    # project specific

          

      </main