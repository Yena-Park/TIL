System.in 대신에 데이터 파일의 이름을 지정하고, File을 만든 후 그 파일에 대한 Scanner 만들기
----------------------------------------------------------------------------
```java
public static void main(String[] args) {
  Scanner inFile = new Scanner(new File("input.txt"));
  String []name = new String[1000];
  int count = 0;
  while(inFile.hasNext()) {
    name[count] = inFile.next();
    number[count] = inFile.next();
    count++;
  }
  inFile.close();
  for(int i=0; i<count; i++) {
    System.out.println("Name: " + name[i]+", Phone : "+number[i]);
  }
}
```
