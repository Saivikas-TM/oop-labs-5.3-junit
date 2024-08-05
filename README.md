# Module 5: Collections and Generics

## Objective
The objective of this module is to get hands-on experience with the following topics:
1. Introduction to Collection Framework
2. Working with Set
3. Working with List
4. Working with Map
5. Working with Generics

## Lab 5.1

### Objectives
1. Understand and implement `Set` in Java.
2. Understand and implement Generics in Java.

### Problem Statement
Create a set of `Employee` objects and eliminate duplicate `Employee` objects.

### Tasks
--> Create a new project for collections and implement all the classes  Employee, Designer, Developer,
    payRoll interface and payRollImpl with the same properties.
1. **Create a new package** named `com.trainingmug.ecommerce.repository`.
2. **Create a new class** named `EmployeeRepository` under the `com.trainingmug.ecommerce.repository` package.
3. **Create the following property** in `EmployeeRepository`:
    ```java
    Set<Employee> employeeSet;
    ```
4. **Create a no-argument constructor** with the following logic:
   - Initialize `employeeSet` to `HashSet`.
   - Add all `Employee` objects, `Developer` objects, and `Designer` objects to `employeeSet`.
   - Add one duplicate `Employee`/`Developer`/`Designer` object to `employeeSet`.

5. **Create the following method** in `EmployeeRepository` that returns the `Set<Employee>`:
    ```java
    public Set<Employee> getEmployeeSet()
    ```

6. **Create a new class** named `CollectionTest` under the `com.trainingmug.ecommerce.main` package with a `public static void main(String[] args)` method.

7. **Create the `EmployeeRepository` object** in `CollectionTest`.

8. **Get the `Employee` set** by calling `getEmployeeSet()` method.

9. **Print the total number of employees**.

10. **Run the `CollectionTest` class** and observe that it will print "No of Employees: 7" even though one duplicate object was added.

11. **In `Employee.java`, `Developer.java`, and `Designer.java`**:
    - Generate the following methods to identify duplicate objects:
        ```java
        @Override
        public int hashCode()
        
        @Override
        public boolean equals(Object obj)
        ```
    - *Hint: To generate these methods, right-click in the workspace -> Source -> Generate hashCode() and equals() methods.*

12. **Re-run the `CollectionTest`** and observe that it now prints "No of Employees: 6".

13. **Create an object of `PayrollImpl`**.

14. **Iterate through `employeeSet`** and display each `Employee` profile by calling `displayProfile(Employee)` on the `PayrollImpl` object.





   
# Lab 5.2

## Objectives
1. Understand and implement `List` in Java.

## Problem Statement
Create a `List` of `Employees` and iterate through the list.

### Tasks
1. **Create the following property** under the `EmployeeRepository` class:
    ```java
    List<Employee> employeeList;
    ```

2. **Inside the no-argument constructor**, perform the following steps:
   - Initialize `employeeList` to `ArrayList`.
   - Add all `Employee` objects, `Developer` objects, and `Designer` objects to `employeeList`.
   - Add one duplicate `Employee`/`Developer`/`Designer` object to `employeeList`.

3. **Create the following method** in `EmployeeRepository` that returns the `List<Employee>`:
    ```java
    public List<Employee> getEmployeeList()
    ```

4. **In the `CollectionTest` class**, get the `Employee` list by calling `getEmployeeList()` method.

5. **Print the total number of employees**.

6. **Run the `CollectionTest` class** and observe that it will print "No of Employees: 7" even though one duplicate object was added. 
   - *Note: `ArrayList` allows duplicates, which is why you will get "No of Employees: 7" even though you have implemented `hashCode()` and `equals()`.*

7. **Iterate through `employeeList`** and display each `Employee` profile by calling `displayProfile(Employee)` on the `PayrollImpl` object.






# Lab 5.3

## Objectives
1. Understand and implement `Map` in Java.

## Problem Statement
Create a `Map` of `Employees` with `empId` as the key and `Employee` object as the value, and iterate through the `Map`.

### Tasks
1. **Create the following property** under the `EmployeeRepository` class:
    ```java
    Map<Integer, Employee> employeeMap;
    ```

2. **Inside the no-argument constructor**, perform the following steps:
   - Initialize `employeeMap` to `HashMap`.
   - Add all `Employee` objects, `Developer` objects, and `Designer` objects to `employeeMap`, mapping their `empId` as the key and the object as the value.
   - Add one duplicate `Employee`/`Developer`/`Designer` object to `employeeMap`.

3. **Create the following method** in `EmployeeRepository` that returns the `Map<Integer, Employee>`:
    ```java
    public Map<Integer, Employee> getEmployeeMap()
    ```

4. **In the `CollectionTest` class**, get the `Employee` map by calling `getEmployeeMap()` method.

5. **Print the total number of employees**.

6. **Run the `CollectionTest` class** and observe that it will print "No of Employees: 6" since we have added one duplicate key. 
   - *Note: `Map` doesn't allow duplicate keys but will allow duplicate values.*

7. **Iterate through `employeeMap`** and display each `Employee` profile by calling `displayProfile(Employee)` on the `PayrollImpl` object.
