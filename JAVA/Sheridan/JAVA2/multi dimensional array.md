```java
public class Car
{
  private String model;
  private String colour;
  private String licensePlate;

  public Car (String model, String colour, String licensePlate)
  {
    this.model = model;
    this.colour = colour;
    this.licensePlate = licensePlate;
  }

  public String getModel ()
  {
    return model;
  }

  public String getColour ()
  {
    return colour;
  }

  public String getLicensePlate ()
  {
    return licensePlate;
  }
}
```

```java
public class ParkingLot
{
  private String lotName;
  private Car[][] cars;

  public ParkingLot (String lotName)
  {
    cars = new Car[2][];
    cars[0] = new Car[3];
    cars[1] = new Car[2];
    lotName = this.lotName;
  }

  public String parkCar (Car car)
  {
    for (int level = 0; level < cars.length; level++) {
      for (int location = 0; location < cars[level].length; location++) {
        if (cars[level][location] == null) {
          cars[level][location] = car;
          return car.getLicensePlate() + " was parked on Level " + level + " in position" + location;
        }
      }
    }
    return "Sorry... the parking lot is full";
  }

  public Car retrieveCar (String licensePlate)
  {
    for (int level = 0; level < cars.length; level++) {
      for (int location = 0; location < cars[level].length; location++) {
        if (cars[level][location] != null && cars[level][location].getLicensePlate().equals(licensePlate)) {
          Car newCar = cars[level][location];
          cars[level][location] = null;
          return newCar;
        }
      }
    }
    return null;
  }

  public void printStatus ()
  {
    String output = this.lotName + "\n";
    for (int level = 0; level < cars.length; level++) {
      output += "Lot Level: " + level + ":  ";
      for (int location = 0; location < cars[level].length; location++) {
        if (cars[level][location] == null) {
          output += "EMPTY ";
        }
        else {
          output += cars[level][location].getLicensePlate() + " ";
        }
      }
      output += "\n";
    }
    System.out.println(output);
  }
}
```

```java
public class ParkingLot
{
  private String lotName;
  private Car[][] cars;

  public ParkingLot (String lotName)
  {
    cars = new Car[2][];
    cars[0] = new Car[3];
    cars[1] = new Car[2];
    this.lotName = lotName;
  }

  public String parkCar (Car car)
  {
    for (int level = 0; level < cars.length; level++) {
      for (int location = 0; location < cars[level].length; location++) {
        if (cars[level][location] == null) {
          cars[level][location] = car;
          return car.getLicensePlate() + " was parked on Level " + level + " in position " + location;
        }
      }
    }
    return "Sorry...the parking lot is full!!!";
  }

  public Car retrieveCar (String licensePlate)
  {
    for (int level = 0; level < cars.length; level++) {
      for (int location = 0; parkingPosition < cars[level].length; location++) {
        if (cars[level][location] != null && cars[level][location].getLicensePlate().equals(licensePlate)) {
          Car returnedCar = cars[level][location];
          cars[level][location] = null;
          return returnedCar;
        }
      }
    }
    return null;
  }

  public void printStatus ()
  {
    String output = this.lotName + "\n";
    for (int level = 0; level < cars.length; level++) {
      output += "Lot Level: " + level + ":  ";
      for (int parkingPosition = 0; parkingPosition < cars[level].length; parkingPosition++) {
        if (cars[level][parkingPosition] == null) {
          output += "EMPTY ";
        }
        else {
          output += cars[level][parkingPosition].getLicensePlate() + " ";
        }
      }
      output += "\n";
    }
    System.out.println(output);
  }
}
```
