Loop & Array
```html
<!DOCTYPE>
<html>
 <head>
  <meta charset="utf-8">
 </head>
 <body>
  <h1>Loop & Array</h1>
  <script>
   var coworkers = ['egoing', 'leeche', 'duru', 'taeho'];
  </script>
  <h2>Co workers</h2>
  <ul>
   <script>
    var i = 0;
    while(i < 4){
     document.write('<li>'+coworkers[i]+'</li>');
     i = i + 1;
    }
   </script>
  </ul>
 </body>
</html>
```
