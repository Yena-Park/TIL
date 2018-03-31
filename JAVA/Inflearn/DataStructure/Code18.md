Call by value
=============
```java
import java.util.Scanner;
public class Code18 {

  public static void main(String[] args) {
    Scanner input = new Scanner(System.in);
    int n = input.nextInt();
    int [] data = new int [n];
    for(int i=0; i<n; i++) {
      data[i] = input.nextInt();
    }
    bubbleSort(n, data);
		
    System.out.println("Sorted data:");
    for(int i=0; i<n; i++) {
      System.out.println(data[i]);
    }
  }
  static void bubbleSort(int n, int [] data) {
    for(int i=n; i>0;i--) {
      for(int j=0; j<i; j++) {
        if(data[j] > data[j+1]) {
          int tmp = data[j];
          data[j] = data[j+1];
          data[j+1] = tmp;
        }
      }
    }
  }
}
```
