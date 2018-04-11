Static variable
---------------
```java
public class StaticExample{

 static int count = 0;
  int a;
  int b;
  StaticExample(){
   count ++;
  }
  StaticExample(int j, int k){ //overiding     
   a = j;
   b = k;
   count ++;
   }

  static int getNumberofCount(){
   return count;
  }
}
```
```java
public class StaticBase{
  
 public static void main(String[] args){
  StaticExample s1 = new StaticExample();
  System.out.println("s1 count is " + s1.count);
  System.out.println("s1 i is " + s1.count);
  StaticExample s2 = new StaticExample(5,3);
  System.out.println("s2 count is " + s2.count);
  System.out.println("s1 count is after s2 count is displayed " + s1.count);
   
  
  System.out.println("get number of count " + StaticExample.getNumberofCount())
  System.out.println(" s1 get number of count " + s1.getNumberofCount());
  System.out.println(" s2 get number of count " + s2.getNumberofCount());

  System.out.println(" static vaiable with class" + StaticExample.count);
  System.out.println(" a" + StaticExample.a);
  System.out.println("s2 a is " + s2.a);
 }
}
```
