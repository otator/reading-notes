# Java Packages and Loops

## Packages
packages are folders contain java classes like Drawing.java, a package can have any number of classes within.

```java
  package test;
  import main.Test2;
  class Test{
    . . .
  }

```

package keyword MUST be the first statement in the class code, before import statements.

there are three types of importing 
1. Import all classes inside a package using asterisk character * 

```java
  import javax.swing.*;
```

2. Import one class only
```java
  import javax.swing.JOptionPane;
```

3. No Import statement, you can use the class you want by typing its packages inside the code.

```java
  class Test{
    javax.swing.JOptionPane.showMessageDialog(null, "");
  }
```

There are 166 packages containing 3279 classes and interfaces in [Java 5](https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html)

you can use these classes and interfaces whenever you want in your code instead of rewriting them from scratch. This is the power of object-oriented programming



## Loops
Loops mainly used to reduce code redundancy whenever it exists and to make code more readable by writing less code.

In java there are three types of loops:
1. for loop
2. while loop
3. do-while loop

### For Loop
For loop in java has three statements(part) in order to make it working as desired.
* Loops are a block of code and the code within is being written inside curly braces *{ }*.

* The first statement is the counter variable, it could be declared inside the loop or outside it as well.

this counter tells the loop from which number to start the loop.

* The second statement is the condition (limit) to stop the loop from executing. if this part left empty, the loop will run infinitely.

* The third statement is the increment which tells the loop by which value it is being incremented

```java
  //this code will print the even numbers from 0 - 100 using for loop
  for(int i=0; i<=100; i+=2){
    System.out.println(i);
  }
```

there is an enhanced for loop that came in version 5. This kind is being used mainly for iterating over arrays.

```java
  //This code prints out the array elements from 0 to 10 using enhanced loop
  int arr[] = {0,2,4,8,10};
  for(int i: arr){
    System.out.println(i);
  }

```

### While Loop
while loop in java does pretty much as the normal for loop.

it has the same three statements as well. but only the condition statement is written within the while parentheses.

The counter initialization is done before the while loop body, while the increment is written inside the while loop body.

```java
  //this code will print the even numbers from 0 - 100 using while loop
  int i=0;
  while(i<=100){
    System.out.println(i);
    i+=2;
  }
```
in order to make for loop and while loop work the same you need to add if statement and use the **break** within to stop the loop execution whenever the condition inside the if will meet.


### Do-While Loop
if you want a loop to execute at least once, java offers this kind of loop; called a *do-while* loop.

in the do-while loop the code that needs to be executed in repetition is written inside the *do* body, while the condition is being tested  is written inside *while* parentheses.

```java
  //this code will print the even numbers from 0 - 100 using do-while loop
  int i=0;
  do{
    System.out.println(i);
    i+=2;
  }
  while(i<=100);

```