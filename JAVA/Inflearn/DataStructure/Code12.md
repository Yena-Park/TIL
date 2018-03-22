```java
import java.util.Scanner;
public class Code12 {
  public static void main(String[] args) {
    int n;
    Scanner  input = new Scanner(System.in);
    n = input.nextInt();
    int [] data = new int [n];
    for(int i=0; i<n; i++)
      data[i]=input.nextInt();
    input.close();
  }
}
```
