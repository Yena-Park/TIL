Function
=========
Basic
-----
```javascript
<!DOCTYPE>
<h1>Function</h1>
    <h2>Basic</h2>
    <ul>
      <script>
        function two(){
          document.write('<li>2-1</li>');
          document.write('<li>2-2</li>');
        }
        document.write('<li>1</li>');
        two();
        document.write('<li>3</li>');
        two();
      </script>
    </ul>
```
Argument & Parameter
--------------------
```javascript
<h1>Function</h1>
    <h2>Basic</h2>
    <ul>
      <script>
        function two(){
          document.write('<li>2-1</li>');
          document.write('<li>2-2</li>');
        }
        document.write('<li>1</li>');
        two();
        document.write('<li>3</li>');
        two();
      </script>
    </ul>
    <h2>Parameter & Argument</h2>
    <script>
      function onePlusOne(){
        document.write(1+1+'<br>');
      }
      onePlusOne();
      function sum(left, right){
        document.write(left+right+'<br>');
      }
      sum(2,3); // 5
      sum(3,4); // 7
    </script>
```