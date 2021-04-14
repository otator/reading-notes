# Stacks and Queues

### Stacks 
A stack is a data structure that consists of nodes, each node has a value and pointer that points to the next node.

Stacks follow the following two principles:

* LIFO (Last In First Out), this means that the last element added to the stack will be the first element popped out of the stack.
* FILO (First In Last Out), this means that the first element added to the stack will be the last element pooped ou of the stack.

A stack must implement the following methods:

1. `push(Node node)` method that pushes the elements to the stack
2. `pop()` method that pops the last element added to the stack(*the popped element will be removed from the stack*)
3. `peek()` method that returns the top element of the stack without removing it (*just view the top element)
4. `isEmpty()` returns true if the stack is empty and false if it is not.

and the stack also has a variable called *top* that keeps pointing to the last element pushed to the stack.


### Queues 
A queue is also a data structure that consists of nodes, each node has a value and a pointer that points to the next node.

Queues follow the following principles:

* FIFO (First In First Out), this means that the first element that entered the queue will be the first element to go out.
* LILO (Last In Last Out), this means that the last element that entered the queue will be the last element to go out.

A queue must implement the following methods:
1. `enqueue(Node node)` method that adds a node to the queue.
2. `dequeue()` method that returns the first element entered the queue (*dequeue method will remove the element from the queue*)
3. `peek()` method that views the front (the first element entered the queue) without removing it from the queue.
4. `isEmpty()` method that returns true if the queue is empty else it will return false

and the queue also has a variable called *front* that points to the first element entered the queue, and another variable called *rare* that points to the last element added to the queue.


