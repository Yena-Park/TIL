Method
======
Power
-----
```java
import java.util.Scanner;
public class Code16 {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    System.out.println("Please enter two integer and press ENter.");
		
    int a = input.nextInt();
    int b = input.nextInt();
		
    int result = power(a, b);
		
    System.out.println("The result is "+result);
  }
  
  static int power(int n, int m)
  {
    int prod = 1;
    for(int i=0; i<m; i++)
      prod *= n;
    return prod;
  }
}
```
