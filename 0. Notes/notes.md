# Calling a Void Method

In the last section we discussed how to use basic methods with an object.

In this section we still won't be making our own methods for objects, but are now adding in the use of parameters.

---

## Method Signatures

Just like constructors, methods have unique **signatures**, made up of their names and parameter lists. In this section, we start using methods that have parameter lists, so the differentiators for signatures will be a combination of names and parameter lists. Here is an example `Person` class with a couple of methods from `Person.java`

```java
public class Person {
    private int age;
    private boolean isStudent;

    public Person(int a, boolean s){
        age = a;
        isStudent = s;
    }

    public void saySomething(String s){
        System.out.println(s);
    }

    public void ageAfterYears(int y){
        System.out.println(age + y);
    }
}
```

We can see here that there are two methods, called `saySomething` and `ageAfterYears`, which just function as simple print statements. The keyword **`void`** is important here, as it lets us know that the method does not **return** information to wherever it was called to, and instead just performs it's action.

---

## Calling Methods with Parameters

To call a method with parameters, we need to get the data types of parameters right, just like when we were using constructors. Here is an example of calling both of the methods we saw above from the `NotesMethodCall1.java` file:

```java
Person person1 = new Person(25, false);
person1.saySomething("Hello!");
person1.ageAfterYears(10);
```

Here, these are successful method calls because they use the parameter types indicated by the method parameter lists. When run, this produces the following output:

```
Hello!
35
```

---

## Method Overloading

When working with constructors, we said they could be **overloaded** when they share the same name (which all constructors for a class do), but have different parameter lists. Methods work the same way, we say a method is overloaded when they share the same name but have different signatures due to different parameter lists. Here is an example of an overloaded method from the `Person` class:

```java
public void saySomething(String s){
    System.out.println(s);
}

public void saySomething(int s){
    System.out.println(s);
}
```

While these two methods function similarly, the computer has to decide which overloaded method to use based on what types of parameters you provide it. If you provide a `String`, it will use the first, whereas if you provide an `int`, it uses the second.

---

## Assignment

Now that you have gone through the notes for this section, you can check out the `Try.md` and `Try.java` files to try a short assignment using this material.
