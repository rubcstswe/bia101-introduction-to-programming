# Inheritance

The concept of inheritance is one of the key features of object-oriented programming.

You will come across this when you have similar classes that share common attributes and methods. 

Instead of writing the **same code multiple times**, you can create a parent class that contains the common attributes and methods, and then create child classes that inherit the attributes and methods of the parent class.

Inheritance is a mechanism in which **one class acquires the properties and behavior of another class**. 

The class that is inherited is called the **parent class**, and the class that inherits the parent class is called the **child class**. 

Inheritance is a powerful feature of object-oriented programming that allows you to create a new class that is based on an existing class. 

# **Example:**

The scenario you are given is to mimic GCBS College's student and teacher system.

## Common Attributes and Behaviours
The students and teachers have the following attributes:
1. Name
2. Age
3. CID Number

The students and teachers have the following behaviours:
1. Walk
2. Talk
3. Eat
4. Sleep

## Specific Attributes and Behaviours
**Teachers:**

The Teachers have the following additional attributes:
1. Subject
2. Salary
3. Department
4. Designation

The Students have the following additional attributes:
1. Student ID
2. Course
3. Year
4. GPA (Average of all your marks)

**Students:**

The Teachers have the following additional behaviours:
1. Teach
2. Grade_students
3. Attend_meeting

The Students have the following additional behaviours:
1. Study
2. Attend_class
3. Write_exam

## Code:

First, you want to create the parent class called `Person` that contains the common attributes and methods of the students and teachers.

### Defining common Class
```python
class Person:
    # common attributes here
    def __init__(self, name, age, cid):
        self.name = name
        self.age = age
        self.cid = cid
    
    # common bevahiours / methods
    def walk(self):
        print(f"{self.name} is walking")
    
    def talk(self):
        print(f"{self.name} is talking")
    
    def eat(self):
        print(f"{self.name} is eating")

    def sleep(self):
        print(f"{self.name} is sleeping")
```

Your `Student` class will inherit the attributes and methods of the `Person` class.\
You only need to define the specific attributes and methods for the `Student` class.

### Defining Student Class
```python
class Student(Person): # Student is inheriting from Person
    # specific attributes here
    def __init__(self, name, age, cid, student_id, course, year, gpa):
        # super is referring to the parent class
        super().__init__(name, age, cid)
        self.student_id = student_id
        self.course = course
        self.year = year
        self.gpa = gpa
    
    # specific behaviours / methods for student
    def study(self):
        print(f"{self.name} is studying")
    
    def attend_class(self):
        print(f"{self.name} is attending class")
    
    def write_exam(self):
        print(f"{self.name} is writing exam")
```

> **Remember:** Since `Student` is inhering from `Person`, you don't need to define the common attributes and methods in the `Student` class.\
> The common attributes and methods are inherited from the `Person` class.\
> `stnt_obj1.walk()` is allowed.\
> `stnt_obj1.teach()` is not allowed.\

### Defining Teacher Class
Similarly, for Teacher class, the class will inherit from the Person class.\
The common attributes and behaviours are **already defined**.\
You only need to define the specific attributes and behaviours for the Teacher class.

```python
class Teacher(Person): # Teacher is inheriting from Person
    # specific attributes here
    def __init__(self, name, age, cid, subject, salary, department, designation):
        # super is referring to the parent class
        super().__init__(name, age, cid)
        self.subject = subject
        self.salary = salary
        self.department = department
        self.designation = designation
    
    # specific behaviours / methods for teacher
    def teach(self):
        print(f"{self.name} is teaching")
    
    def grade_students(self):
        print(f"{self.name} is grading students")
    
    def attend_meeting(self):
        print(f"{self.name} is attending meeting")
```

## Creating Objects

```python
# Creating Student Object
tashi = Student("Tashi", 20, "1234", "123", "BSc", 2, 3.5)
dorji = Student("Dorji", 21, "1235", "124", "BSc", 3, 3.8)

# Creating Teacher Object
penjor = Teacher("Penjor", 30, "1236", "Maths", 30000, "Science", "Lecturer")
karma = Teacher("Karma", 35, "1237", "Physics", 40000, "Science", "Senior Lecturer")

# using the objects
# student
tashi.walk()
tashi.study()
tashi.write_exam()

dorji.walk()
dorji.sleep()

# teacher
karma.attend_meeting()
karma.sleep()

karma.study() # This will give an error

if penjor.salary > karma.salary:
    print(f"{penjor.name} earns more than {karma.name}")
else:
    print(f"{karma.name} earns more than {penjor.name}")

if tashi.gpa > dorji.gpa:
    print(f"{tashi.name} has higher GPA than {dorji.name}")
else:
    print(f"{dorji.name} has higher GPA than {tashi.name}")

```

# Exercise:

1. Create a parent class called `Vehicle` and child classes for `Car` and `Motorcycle` classes.

**Vehicle:**

The common attributes are:
1. brand
2. model
3. year
4. fuel_type

The common behaviours are:
1. start
2. stop
3. displayInfo --> Prints brand, model and year
4. drive
5. honk

**Car:**

Attributes specific to `Car` are:
1. num_of_doors
2. num_of_seats
3. num_of_wheels
4. bumper_size

Behaviours specific to `Car` are:
1. open_trunk
2. close_trunk
3. drift
4. park_in_large_space

**Motorcycle:**

Attributes specific to `Motorcycle` are:
1. has_side_car --> Boolean (true / false)
2. has_helmet --> Boolean (true / false)
3. mirror_size

Behaviours specific to `Motorcycle` are:
1. drive_on_one_wheel
2. make_noise
3. park_in_small_space