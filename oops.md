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
```Student st = new Student();```

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
1. public : 
Public access modifier can be accessed from anywhere. Variables and functions with public access modifier can be accessed from anywhere. 

2. Private : 
Private access modifier restricts access to the same class. Variables and functions with private access modifier can be accessed within the same class.
 
3. Default : 
Default access modifier restricts access to the same package. Variables and functions with default access modifier can be accessed within the same package.


## CONSTRUCTOR
-> The job of the constructor is to allocate memory to the object and create it in the heap. 

-> The access specifier can be either public or private or default. The constructor doesn’t have any return type and its name is the same as that of the class name. 

**1. default constructor** -> The default constructor creates object and gives default values to the data members
```
public Student () {

}
```

**2. Parameterised Constructor** -> Apart from the default constructor, we can give custom values as arguments and those arguments can be used to initialise the values of data members. 

```
public Student (String name, int rollno) {
	this.name = name;
	this.rollno = rollno;
}
```

**Note:** 
    
1. Java gives you a default constructor, even if you don’t write it. 

2. If you write your own parameterised constructor, then Java deletes its default constructor.

3. You can have multiple custom constructors.  
    
    
## STATIC AND FINAL KEYWORD
**Static** : static is used to define the class member that can be used independently of any object of the class. In other word, If a variable is static, then it would be common to all the object. For example if we want to count the number of student objects created by student class, then we can keep a static variable called num_students and increment it in the constructor.   

Code :
```
public class Main {
	public class Student {
		// information
		private String name;
		private int rollno;
		static int num_students;
		
		// constructor
		public Student(String name, int rollno) {
			this.name = name;
			this.rollno = rollno;
			
			this.num_student++;
		}
	}
	
	public void main(String[] args) {
		System.out.println(Student.num_student);
		Student s1 = new Student("Bornali", 12);
		Student s2 = new Student("Sahin", 15);
		Student s3 = new Studnet("Rohan", 53);
		System.out.println(Student.num_student);
	}
}

OUTPUT : 0
	
	 3
```
**Final** :  There would be some data members whose value you would not like to change. In other word, Veriable which are final they are initialized only once. For example, we want to say that the roll number for a student is fixed and once allotted, it will never change. We can use the final keyword for the same. Once initialised, the value of the final variable can never change.

Code :

```
public class Student {
	// information
	private String name;
	// variable which are final, they are initialized only once
	private final int rollno;

	// constructor
	public Student(String name, int rollno) {
		this.name = name;
		this.rollno = rollno;
	}
}
```
Note : **The combination of static and final in Java is makes a variable constanst**

## THIS KEYWORD
*'this'* is a keyword used in member functions to access local variables with the same name as data members. *'this'* refer to the current object to which function is called



