## CLASS AND OBJECT
  Class is the blueprint and the objects are instances of the blueprint. 

  Let us take an example of Car class and its objects:
  
  ![Screenshot (124)](https://user-images.githubusercontent.com/72231697/155797465-9668527f-eb8e-4e9e-b5c8-c2d8076655ca.png)
  
  Hence, class is the blueprint which consists of data members and functions. Objects are instances of class. Each object has a different value of data members mentioned in class.

## How to create Classes and Objects
//
public class Student {
    // information -> data members
    String name;
    int rollno;
    
    // what it can do with this information -> functions/ methods

}
//

## how to access its variables/ data members and how to change values of data members

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



