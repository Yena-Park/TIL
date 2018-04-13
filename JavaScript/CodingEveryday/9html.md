Function
=========
Basic
-----
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
```
Argument & Parameter
--------------------
```javascript
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
  sum(3,4); // 7 </script>
```
Parameter
---------
```javascript
<h2>Return</h2>
  <script>
    function sum2(left, right){
      return left+right;
    }
    document.write(sum2(2,3)+'<br>');
    document.write('<div style="color:red">'+sum2(2,3)+'</div>');
    document.write('<div style="font-size:3rem;">'+sum2(2,3)+'</div>');
  </script>
```
