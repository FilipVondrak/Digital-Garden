---
{"dg-publish":true,"permalink":"/Osobní/Programování/Patterny/FactoryPattern/","created":"2024-01-03T15:04:27.784+01:00","updated":"2024-04-04T15:20:12.164+02:00"}
---

- Poskytuje rozhraní pro vytváření objektů v nadtřídě, ale umožňuje podtřídám měnit typ objektů, které budou vytvořeny.
- Myšlenka spočívá v použití interfacu pro vytvoření objektu, ale nakonec se podtřída rozhodne, kterou třídu instancovat

![Pasted image 20240329153655.png](/img/user/Images/Pasted%20image%2020240329153655.png)

> [!Showcase]- ukázka implementace tovární metody v C#
> ```CSharp
>// Product
>public abstract class Vehicle
>{
>    public abstract string GetVehicleType();
>}
>
>// ConcreteProduct
>public class Truck : Vehicle
>{
>    public override string GetVehicleType()
>    {
>        return "Truck";
>    }
>}
>
>// ConcreteProduct
>public class Ship : Vehicle
>{
>    public override string GetVehicleType()
>    {
>        return "Ship";
>    }
>}
>
>// Creator
>public abstract class VehicleFactory
>{
>    public abstract Vehicle CreateVehicle();
>}
>
>// ConcreteCreator
>public class TruckFactory : VehicleFactory
>{
>    public override Vehicle CreateVehicle()
>    {
>        return new Truck();
>    }
>}
>
>// ConcreteCreator
>public class ShipFactory : VehicleFactory
>{
>    public override Vehicle CreateVehicle()
>    {
>        return new Ship();
>    }
>}
>
>class Program
>{
>    static void Main(string[] args)
>    {
>        // Vytvoření Truck pomocí TruckFactory
>        VehicleFactory truckFactory = new TruckFactory();
>        Vehicle truck = truckFactory.CreateVehicle();
>        Console.WriteLine(truck.GetVehicleType()); // Vypíše: Truck
>
>        // Vytvoření Ship pomocí ShipFactory
>        VehicleFactory shipFactory = new ShipFactory();
>        Vehicle ship = shipFactory.CreateVehicle();
>        Console.WriteLine(ship.GetVehicleType()); // Vypíše: Ship
>    }
>}
>```

> [!Showcase]- ukázka implementace tovární metody v Javě
>```Java
>package com.mano.patternsdemo;
>
>public interface Employee {
>   double earnings();
>}
>
>package com.mano.patternsdemo;
>public class SalariedEmployee implements Employee {
>   private double basic;
>   private double ta;
>   private double da;
>   public SalariedEmployee(double basic,
>         double ta, double da){
>      this.basic = basic;
>      this.ta = ta;
>      this.da = da;
>   }
>
>   @Override
>   public double earnings() {
>      return basic+(basic*ta)+(basic*da);
>   }
>}
>
>package com.mano.patternsdemo;
>
>public class HourlyEmployee implements Employee {
>   private double hoursWorked;
>   private double payPerHour;
>   public HourlyEmployee(double hoursWorked,
>         double payPerHour){
>      this.hoursWorked = hoursWorked;
>      this.payPerHour = payPerHour;
>   }
  > 
>   @Override
>   public double earnings() {
>      return hoursWorked*payPerHour;
>   }
>}
>
>package com.mano.patternsdemo;
>import java.util.Scanner;
>public class EmployeeFactory {
>   public enum EmployeeType {HOURLY, SALARIED};
>   public Employee recruit(EmployeeType employeeType){
>         Employee emp;
>      Scanner scanner = newScanner(System.in);
>      switch(employeeType){
>         case HOURLY:
>            System.out.println("Enter Hours:");
>            double h = scanner.nextDouble();
>            System.out.println("Enter pay per hour:");
>            double p = scanner.nextDouble();
>            emp = new HourlyEmployee(h,p);
>            break;
>         case SALARIED:
>            System.out.println("Enter Basic:");
>            double basic = scanner.nextDouble();
>            System.out.println("Enter TA:");
>            double ta = scanner.nextDouble();
>            System.out.println("Enter DA:");
>            double da = scanner.nextDouble();
>            emp = new SalariedEmployee(basic,ta,da);
>            break;
>         default:
>            emp = null;
>            break;
>      }
>      return emp;
>   }
>}
>
>package com.mano.patternsdemo;
>public class Main {
>   public static void main(String[] args) {
>      EmployeeFactory employeeFactory = new EmployeeFactory();
>      Employee emp1 = employeeFactory.recruit(EmployeeFactory
>         .EmployeeType.HOURLY);
>      Employee emp2 = employeeFactory.recruit(EmployeeFactory
>         .EmployeeType.SALARIED);
>      System.out.println("emp1 earns $"+emp1.earnings());
>      System.out.println("emp2 earns $"+emp2.earnings());
>   }
>}
>```
