Method
======
Find prime number between 1 and 100000
--------------------------------------
```java
public static void main(String[] args) {
  for(int i=2; i<=100000; i++) {
    if(isPrime(i))
      System.out.println(i);
  }

public static boolean isPrime(int k) {
  for (int i=2; i*i<=k; i++)
    if(k%i==0)
      return false;
    return true;
}
```
