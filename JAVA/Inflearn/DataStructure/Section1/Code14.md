Bubble Sort(버블정렬)
==================
```java
import java.util.Scanner;
public class Code14 {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    int n = input.nextInt();
    int [] data = new int[n];
		
    for (int i=0; i<n; i++)
      data[i] = input.nextInt();
    input.close();
		
    for(int i=n-1; i>0; i--) {
      for(int j=0; j<i; j++) {
        if(data[j] > data[j+1]) {
          int tmp = data[j];
          data[j] = data[j+1];
          data[j+1] = tmp;
        }
      }
    }
    System.out.println("Sorted data:");
    for(int i=0; i<n; i++)
      System.out.println(data[i]);
  }
}
```
