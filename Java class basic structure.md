```java
public class Student{
String name;
int roll_no;
//contractor 
Student(String name,int roll_no){
this.name=name;
this.roll_no=roll_no;
   }
//you can also declare function 
public void sayHi(){
System.out.println("hi!");
   }
}


```

- You can access this variable and functions by dot(.) Operator.
- But first you have to make object of this class.

**How make objects**
```java 
Student student1= new Student("prashant",132);

//now you can access variable and methods of Student class
System.out.println(student1.name);
System.out.println(Student.sayHi());
```



