# Exceptions, primitives, File I/O


## Primitives
java primitives and the memory size they take.

**They live inside the _stack_, faster to access**
* boolean – 1 bit
* byte – 8 bits
* short, char – 16 bits
* int, float – 32 bits
* long, double – 64 bits

java wrappers classes of primitives, they take more memory

**They live inside the _heap_, slower than primitives access**
* Boolean – 128 bits
* Byte – 128 bits
* Short, Character – 128 bits
* Integer, Float – 128 bits
* Long, Double – 192 bits

_As mentioned above the Boolean class instance occupies 128 bit which equls to 128 variable of boolean primitive type._




## Exceptions
An [exception](https://docs.oracle.com/javase/tutorial/essential/exceptions/definition.html) is an event that occurs during the execution of a program that disrupts the normal flow of instructions.

The following code that shows the basic operation of calculator(add, sub, multiply, divide) has an exception when divide by **zero**.

```java
public class ExptionsDemo {
    public static void main(String[] args){
        //this method will cause an exeption 
          showBasicOperations(20,0);
    }

    public static int divide(int a, int b){
        return a / b;
    }
    public static int sum(int a, int b){
        return a + b;
    }
    public static int subtract(int a, int b){
        return a - b;
    }
    public static int multiply(int a, int b){
        return a * b;
    }

    public static void showBasicOperations(int a, int b){
      try{
        System.out.println("a" + "+" + "b = " + sum(a,b));
        System.out.println("a" + "-" + "b = " + subtract(a,b));
        System.out.println("a" + "*" + "b = " + multiply(a,b));
        System.out.println("a" + "/" + "b = " + divide(a,b));
      }catch(Execption e){
          e.printStackTrace();
        } 
    }
}
```

when the code is complied and starts running
- method main added to stack
- when the method _showBasicOperations_ called with arguments 20 and zero (add in stack at the top of main)
- _sum()_, _subtract()_, and _multiply()_ are called and show thier result on the screen
- when _divide()_ method is called with arguments 20 and zero it is added to stack on the top until it executes.
- divide method will cause an error, this method will createan object and hands it off to the runtime system, this object called _exception object_
and this operation call _throwing an error_.

- the run time system will try to find any method that had handled this exception among the call stack(which is the methods added to the stack).
- the run time system will search for handler from the method which causes the error through the call stack reversely.
- When an appropriate handler is found, the runtime system passes the exception to the handler. An exception handler is considered appropriate if the type of the exception object thrown matches the type that can be handled by the handler.

- it will found that the showBasicOperations() has handled that exception, so the catch block will be executed.

**Exceptions can prevent the code from stop executing (crashes)**.



## File I/O

Scanner, FileReader, and BufferedReader classes are being used in order to read file in java.

the below example reads text.txt file and prints out its text to the screen

```java
  public class ReadFiles {
      public static void main(String[] args){
          Scanner scanner = null;
          try{
              scanner = new Scanner(new BufferedReader(new FileReader("text.txt")));
              while(scanner.hasNext()){
                  System.out.println(scanner.nextLine());
              }
          }catch(IOException e){
              e.printStackTrace();
          }
      }
  }
```

**Note:** _FileReader constructor argument must be the name of the file or the path for that file including its name and extension._

