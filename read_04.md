# OOP
### Object
An object is anyting around you that has a state and behavior. A lamp for example is an object and it has a state it can be either on or off

and it has a behavior like turn on, turn off and change lamp.

in software objects are prertty much the same for example and object cat of type animal could have a name, color, and type and it has a behavior like eat, drink, meow and sleep

### Class
A class is a blueprint that allows object creation. for example class *Animal* can have fields(states) like name, type, color and some methods(behavior) like eat(), sleep(), makeSound() and so the forth.

```java
  class Animal{
    //states or fields
    String name;
    String type;
    String color;
    // constructor to make objects out of the class
    public Animal(String name, String type, String color){
      this.name = name;
      this.type = type;
      this.color = color;
    }

    //behavior or methods
    public void makeSound(String sound){
      System.out.println(sound);
    }
  }
 ```

 ```java 
  class AnimalDemo{
    public static void main(String[] args){
      Animal cat = new Animal("Snow", "cat", "white");
      cat.makeSound("meow"); // outputs meow
      Animal dog = new Animal("Oscar", "dog", "brown");
      dog.makeSound("bark"); // outputs bark
    }
  }
 ```