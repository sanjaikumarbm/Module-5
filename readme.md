## Constructors in Python: Student Name and id using constructors
## 🎯 Aim
To write a Python program that creates a **Student** class with a **default constructor**,which will take the name and userid of the person as parameters print the userid  of the person.

## 🧠 Algorithm
1. **Get user input**: Accept the student's name from the user.
2. **Define the class**: Create a class `Student` with a default constructor (`__init__`).
3. **Default Constructor**: In the constructor, assign the user input (student name) to an instance variable `self.a`.
4. **Display Message**: Define a method `display` show the name and userid of the person as parameters print the userid  of the person
5. **Execute the Program**: Instantiate the `Student` class and call the `display` method.

## 🧾 Program
```
class Student:
    def __init__(self,name,userid):
        self.name=name
        self.userid=userid
        self.display()
    def display(self):
        print(self.userid)
name=input()
userid=input()
obj = Student(name,userid)
obj.display()      
```


## Output
<img width="1096" height="429" alt="image" src="https://github.com/user-attachments/assets/c167dc48-fd56-4e95-b101-0de50354cb9a" />


## Result
The Python program that creates a **Student** class with a **default constructor**,which will take the name and userid of the person as parameters print the userid  of the person.


# Destructor in Python

This project demonstrates how to implement a **destructor** in Python using a simple class.

## 🚀 Overview

The program defines a class `Demo` with:

- A **constructor** `__init__` that initializes an instance variable and prints a message.
- A **destructor** `__del__` that prints a message when the object no longer exists.

## 🧠 Algorithm

1. Define a class named `Demo`.
2. Inside the class, define the `__init__` method:
   - Initialize an instance variable `status` with the value `"Alive"`.
   - Print the value of `status`.
3. Define the `__del__` method:
   - Print a message indicating the object no longer exists.
4. Outside the class:
   - Create an instance of the `Demo` class.
   - Delete the object using the `del` keyword.
## Program
```
class Demo:
    def __init__(self):
        print("Alive")
    def __del__(self):
        print("The object no longer exists")
obj=Demo()
del obj
```
## 🧪 Output
<img width="702" height="186" alt="image" src="https://github.com/user-attachments/assets/d73d2263-c86a-483b-bf0f-e753c2cfbb25" />


## Result
This project demonstrates how to implement a **destructor** in Python using a simple class is executed sucessfully.

# Hierarchical Inheritance in Python

This Python project demonstrates **Hierarchical Inheritance** using a base class `Details` and two derived classes `Employee` and `Patient`. The program collects and displays details for both employees and patients.

## 🎯 Aim

To write a Python program that uses **Hierarchical Inheritance** to input and display **Employee** and **Patient** details.

## 📘 Description

- **Base Class:** `Details`
  - Stores common attributes: `name`, `age`
  - Provides methods: `getName()`, `getAge()`

- **Derived Class 1:** `Employee`
  - Inherits from `Details`
  - Adds: `employee_id`, `department`
  - Method: `getEmployeeDetails()`

- **Derived Class 2:** `Patient`
  - Inherits from `Details`
  - Adds: `patient_id`, `disease`
  - Method: `getPatientDetails()`

## 🧠 Algorithm

1. Create base class `Details` with common attributes.
2. Create `Employee` class extending `Details`, adding employee-specific data.
3. Create `Patient` class extending `Details`, adding patient-specific data.
4. Get user input for employee and patient data.
5. Display collected information using class methods.

## Program
```
class Details:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def getName(self):
        return self.name
    def getAge(self):
        return self.age
class Employee(Details):
    def __init__(self, name, age, employee_id, department):
        super().__init__(name, age)
        self.employee_id = employee_id
        self.department = department
    def getEmployeeDetails(self):
        print("Employee Information:")
        print("Name:", self.getName())
        print("Age:", self.getAge())
        print("Employee ID:", self.employee_id)
        print("Department:", self.department)
class Patient(Details):
    def __init__(self, name, age, patient_id, disease):
        super().__init__(name, age)
        self.patient_id = patient_id
        self.disease = disease
    def getPatientDetails(self):
        print("Patient Information:")
        print("Name:", self.getName())
        print("Age:", self.getAge())
        print("Patient ID:", self.patient_id)
        print("Disease:", self.disease)

emp_name = input()
emp_age = int(input())
emp_id = input()
emp_dept = input()
employee = Employee(emp_name, emp_age, emp_id, emp_dept)
pat_name = input()
pat_age = int(input())
pat_id = input()
pat_disease = input()
patient = Patient(pat_name, pat_age, pat_id, pat_disease)
employee.getEmployeeDetails()
patient.getPatientDetails()

```
## Sample Output
<img width="518" height="399" alt="image" src="https://github.com/user-attachments/assets/9d5b5d48-b3c7-4395-a3b1-cfda203c56c1" />


# Multilevel Inheritance Example in Python

This Python project demonstrates the concept of **Multilevel Inheritance** to collect and display the **name**, **age**, and **salary** of a person.

## 🎯 Aim

To write a Python program that get input from user name, age and salary of a person and display using Multilevel inheritance.

## 🧠 Algorithm

1. **Parent Class**  
   - `__init__(name)` initializes the `name` attribute.  
   - `getName()` returns the `name`.

2. **Child Class (inherits Parent)**  
   - `__init__(name, age)` initializes `name` using `super()` and adds `age`.  
   - `getAge()` returns the `age`.

3. **Grandchild Class (inherits Child)**  
   - `__init__(name, age, location)` initializes `name` and `age` using `super()` and adds `location`.  
   - `getLocation()` returns the `location`.

4. **Input & Output**  
   - Take user input for name, age, and location.  
   - Create an instance of `Grandchild`.  
   - Print all details using class methods.

## Program
```
class student:
    def __init__(self,x,y,z):
        self.x=x
        self.y=y
        self.z=z
class s(student):
    def show(self):
        print(f"{self.x} {self.y} {self.z}")
x=input()
y=int(input())
z=int(input())
obj=s(x,y,z)
obj.show()
```

## Sample Output
<img width="1662" height="600" alt="image" src="https://github.com/user-attachments/assets/68ed9994-3521-4567-ad35-e3feede20645" />



# Arithmetic Operations Using Multiple Inheritance in Python

This Python program demonstrates **multiple inheritance** by performing basic arithmetic operations — Addition, Subtraction, and Division — using three classes.

## 🎯 Aim

To write a Python program to calculate **Add, Sub & Division** using **Multiple Inheritance**.

## 🧠 Algorithm

1. **Define `Calculation1` class**
   - Contains `Summation(a, b)` method to return the sum of two numbers.
2. **Define `Calculation2` class**
   - Contains `multi(a, b)` method to return the product of two numbers.
3. **Define `Derived` class**
   - Inherits from both `Calculation1` and `Calculation2`.
   - Contains `Division(a, b)` method to return the division result.
4. **Input**
   - Prompt the user to enter two numbers.
5. **Process**
   - Create an object of the `Derived` class.
   - Call `Summation`, `multi`, and `Division` methods.
6. **Output**
   - Display the results of the three operations.

## 💻 Program 
```
class Calculation1:
    def Summation(self, a, b):
        return a + b

class Calculation2:
    def multi(self, a, b):
        return a * b

class Derived(Calculation1, Calculation2):
    def Division(self, a, b):
        if b != 0:
            return a / b
        else:
            return "Division by zero is not allowed"
num1 = float(input())
num2 = float(input())
obj = Derived()
sum_result = obj.Summation(num1, num2)
mul_result = obj.multi(num1, num2)
div_result = obj.Division(num1, num2)
print(sum_result)
print(mul_result)
print(div_result)


```
## Output Example
<img width="688" height="431" alt="image" src="https://github.com/user-attachments/assets/fde8ad2f-28d7-4161-8297-4d95b91ee30d" />


