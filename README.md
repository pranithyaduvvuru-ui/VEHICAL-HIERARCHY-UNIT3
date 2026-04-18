# VEHICAL-HIERARCHY-UNIT3
This project demonstrates inheritance by creating a hierarchy of vehicles such as car, bike, and truck. It shows how common properties and behaviors are shared and extended using Java OOP concepts like inheritance and polymorphism.
# 🚗 Vehicle Management System (Java OOP)

## 📌 Overview

This project is a simple **Vehicle Management System** built using Java.
It demonstrates **Inheritance** in Object-Oriented Programming (OOP) by extending a base class (`Vehicle`) into specialized classes (`Car` and `Bike`).

---

## 🎯 Objective

To design a system that:

* Stores general vehicle details
* Differentiates between cars and bikes
* Displays specific details based on vehicle type

---

## 🧠 Concepts Used

* **Inheritance**
* **Classes & Objects**
* **Method Reusability**
* **User Input using Scanner**

---

## 🛠️ Technologies

* Java
* Scanner Class

---

## 📂 Project Structure

```
VehicleProject/
│
├── Solution.java   (Main File)
```

---

## 💻 Source Code

```java
import java.util.*;

class Vehicle {
    String make;
    String model;
    int year;

    Vehicle(String make, String model, int year) {
        this.make = make;
        this.model = model;
        this.year = year;
    }

    void displayVehicleInfo() {
        System.out.println("Vehicle Details:");
        System.out.println("Make: " + make);
        System.out.println("Model: " + model);
        System.out.println("Year: " + year);
    }
}

class Car extends Vehicle {
    int numberOfDoors;
    String fuelType;

    Car(String make, String model, int year, int numberOfDoors, String fuelType) {
        super(make, model, year);
        this.numberOfDoors = numberOfDoors;
        this.fuelType = fuelType;
    }

    void displayCarInfo() {
        System.out.println("Car Details:");
        System.out.println("Number of Doors: " + numberOfDoors);
        System.out.println("Fuel Type: " + fuelType);
    }
}

class Bike extends Vehicle {
    String bikeType;
    int engineCapacity;

    Bike(String make, String model, int year, String bikeType, int engineCapacity) {
        super(make, model, year);
        this.bikeType = bikeType;
        this.engineCapacity = engineCapacity;
    }

    void displayBikeInfo() {
        System.out.println("Bike Details:");
        System.out.println("Bike Type: " + bikeType);
        System.out.println("Engine Capacity: " + engineCapacity + " cc");
    }
}

public class Solution {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        String type = s.nextLine();
        String make = s.nextLine();
        String model = s.nextLine();
        int year = s.nextInt();
        s.nextLine();

        if (type.equalsIgnoreCase("car")) {
            int doors = s.nextInt();
            s.nextLine();
            String fuel = s.nextLine();

            Car car = new Car(make, model, year, doors, fuel);
            car.displayVehicleInfo();
            car.displayCarInfo();
        }
        else if (type.equalsIgnoreCase("bike")) {
            String bikeType = s.nextLine();
            int engine = s.nextInt();

            Bike bike = new Bike(make, model, year, bikeType, engine);
            bike.displayVehicleInfo();
            bike.displayBikeInfo();
        }
    }
}
```
<img width="958" height="436" alt="1" src="https://github.com/user-attachments/assets/f1606e32-3f90-4098-b0fd-f65ec640ed83" />
<img width="960" height="436" alt="2" src="https://github.com/user-attachments/assets/60b7a41f-dac1-4ed8-9f19-43428e451e11" />
<img width="957" height="434" alt="3" src="https://github.com/user-attachments/assets/447e7815-7090-4ff9-a99d-5c799dd88af9" />



---

## ▶️ How to Run

1. Save file as `Solution.java`
2. Compile:

```
javac Solution.java
```

3. Run:

```
java Solution
```

---

## 📥 Sample Input

### Car Example

```
car
Toyota
Camry
2022
4
Petrol
```

### Bike Example

```
bike
Yamaha
R15
2021
Sports
155
```

---

## 📤 Sample Output

### Car Output

```
Vehicle Details:
Make: Toyota
Model: Camry
Year: 2022
Car Details:
Number of Doors: 4
Fuel Type: Petrol
```

### Bike Output

```
Vehicle Details:
Make: Yamaha
Model: R15
Year: 2021
Bike Details:
Bike Type: Sports
Engine Capacity: 155 cc
```

---

## 🚀 Future Enhancements

* Add more vehicle types (Truck, Bus)
* Store data in database
* Add GUI using Java Swing
* Add validation and error handling

---
## 📌 Conclusion

This project demonstrates how **inheritance** helps in creating reusable and organized code by extending a base class into specialized classes.
