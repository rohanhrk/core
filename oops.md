## CLASS AND OBJECT
  Class is the blueprint and the objects are instances of the blueprint. 

  Let us take an example of Car class and its objects:
  
  ![Screenshot (124)](https://user-images.githubusercontent.com/72231697/155797465-9668527f-eb8e-4e9e-b5c8-c2d8076655ca.png)
  
  Hence, class is the blueprint which consists of data members and functions. Objects are instances of class. Each object has a different value of data members mentioned in class.

## HOW TO CREATE CLASS
```
// Strudent -> class name
// public -> access modifier
public class Student {
    // information -> data members
    String name;
    int rollno;
    
    // what it can do with this information -> functions/ methods

}
```

## HOW TO CREATE OBJECT
Student st = new Student();

## HOW TO ACCESS DATA MEMBER AND HOW TO CHANGE VALUE OF DATA MEMBER

```
public static void main(String[] args) {
    // create object
		Student s1 = new Student(); // new keyword -> memory allocate in heap
		System.out.println(s1.rollno + " " + s1.name); 
    /* 
        The output will be 0 null, as these are the default values of int and string in Java
    */ 
    
    // value change
		s1.rollno=1;
		s1.name="Akshima";
    System.out.println(s1.rollno + " " + s1.name);
    /* 
        The output will be 1 Akshima, as these are the default values of int and string in Java
    */ 
}
```

## ACCESS MODIFIER
1. public
Public access modifier can be accessed from anywhere. Variables and functions with public access modifier can be accessed from anywhere. 

2. Private
Private access modifier restricts access to the same class. Variables and functions with private access modifier can be accessed within the same class.
 
3. Default
Default access modifier restricts access to the same package. Variables and functions with default access modifier can be accessed within the same package.


## COMSTRUCTOR
-> The job of the constructor is to allocate memory to the object and create it in the heap. 

-> The access specifier can be either public or private or default. The constructor doesn’t have any return type and its name is the same as that of the class name. 

**1. default constructor** -> The default constructor creates object and gives default values to the data members
```
public Student () {

}
```

**2. Parameterised Constructor** -> Apart from the default constructor, we can give custom values as arguments and those arguments can be used to initialise the values of data members. 




