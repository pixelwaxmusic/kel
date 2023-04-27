```java
// class names are CamelCase
class Acronym {

    // class member names (variables, methods, functions) are lowerCamelCase

    // field variable or class variable
    // gets initialized (assigned) the value passed to constructor ("this is my phrase")
    private final String phrase;

    // constructor with public access modifier 
    // (I can be called from outside the class)
    // This just returns the phrase that was used to construct this class
    public Acronym(String phrase) {
        this.phrase = phrase
    }

    // get() is a method. methods are operations that interact with class state 
    // that is external to the method itself (e.g. state held in class variables)
    // e.g. this.phrase;
    public String get() {

        // this is a reference to private final string phrase;
        return this.phrase
    }

    // this is a function. It doesn't depend on external state. It can be called
    // in isolation. Does not interact with anything else
    // hello("kel")
    // > "Hello, kel"
    // private modifier means it can only be called within this class's code
    private String hello(String name) {
        return "Hello, " + name
    }
    

}
```

```java


class Main {

    // We run everything from the main method in the Main class
    public static void main(String[] args) {

        // Construct an instance of Acronym with a phrase and assign it to a variable (faq)
        Acronym faq = new Acronym("this is my phrase");

        // call get method on faq (which is an instance of Acronym)
        // and assign it to variable foo
        // return the phrase from the previous line
        String foo = faq.get();

        // printing foo (which has a value of "this is my phrase") to the console / std out
        System.out.println(foo);
    }
}

```

- Access modifiers allow you to control access to class member (variables, methods, constructors)
    - public, private, package private, protected
    - public allows the class member to be called from outside the class
    - private allows the class member to be called from only inside the class