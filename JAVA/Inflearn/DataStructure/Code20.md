```java
class Code20 {
  static String[] name;
  static String[] number;
  static int count = 0;

  public static void main(String[] args) {
    name = new String[1000];
    number = new String[1000];
    try {
      Scanner inFile = new Scanner(new File("input.txt"));
      while(inFile.hasNext()) {
        name[count] = inFile.next();
        number[count] = inFile.next();
        count++;
      }
      inFile.close();
    }catch(FileNotFoundExeption e) {
      System.out.println("No data file exists.");
      return;
    }
  }
}
```
