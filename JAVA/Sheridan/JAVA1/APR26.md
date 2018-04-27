```java
public class Customer {
	private int customerID;
	private String firstName;
	private String lastName;
	
	public Customer() {
		customerID = 1;
		firstName = "a";
		lastName = "a";
	}
	
	public Customer(int cID, String fName, String lName) {
		customerID = cID;
		firstName = fName;
		lastName = lName;
	}
	
	public void setcustomerID(int cID) {
		customerID = cID;
	}
	
	public int getcustomerID() {
		return customerID;
	}
	
	public void setfirstName(String fName) {
		firstName = fName;
	}
	
	public String getcfirstName() {
		return firstName;
	}
	
	public void setlastName(String lName) {
		firstName = lName;
	}
	
	public String getlastName() {
		return lastName;
	}
}
```
```java
public class Order {
	private int CustomerID;
	private int orderNo;
	private String itemName;
	private double itemUnitPrice;
	private int totalQuantitySold;
	
	public Order(){
		CustomerID = 1;
		orderNo = 1;
		itemName = "aaa";
		itemUnitPrice = 0;
		totalQuantitySold = 0;
	}
	
	public Order(int cID, int oNo, String iName, double iUnitPrice, int tQuantitySold) {
		CustomerID = cID;
		orderNo = oNo;
		itemName = iName;
		itemUnitPrice = iUnitPrice;
		totalQuantitySold = tQuantitySold;
	}
	
	public void setCustomerID(int c1) {
		CustomerID = c1;
	}
	
	public int getCustomerID() {
		return CustomerID;
	}
	
	public void setorderNo(int o1) {
		orderNo = o1;
	}
	
	public int getorderNo () {
		return orderNo;
	}
	
	public void setitemName(String i1) {
		itemName = i1;
	}
	
	public String getitemName() {
		return itemName;
	}
	
	public void setitemUnitPrice(double u1) {
		itemUnitPrice = u1;
	}
	
	public double getitemUnitPrice() {
		return itemUnitPrice;
	}
	
	public void settotalQuantitySold(int t1) {
		totalQuantitySold = t1;
	}
	
	public int gettotalQuantitySold() {
		return totalQuantitySold;
	}
	
	public double calculateTotal() {
		double totalAmount = itemUnitPrice*totalQuantitySold;
		return totalAmount;
	}
}
```
```java
public class TestAssignment4 {

	public static void main(String[] args) {
		Customer C1 = new Customer();
		
		Customer C2 = new Customer(2, "Yena", "Park");

		Order O1 = new Order(2, 77, "apple", 7.50, 40);
		
		System.out.println("Customer Id of C2 is "+C2.getcustomerID());
		System.out.println("Item name of O1 is "+O1.getitemName());
		System.out.println("Item unit price of O1 is "+O1.getitemUnitPrice());
		System.out.println("Total Quantity Sold of O1 is "+O1.gettotalQuantitySold());
		System.out.println("Total Amount of O1 is "+O1.calculateTotal());
	}
}
```
