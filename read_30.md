# Hash Tables

### OverView 
[Hash Table](https://en.wikipedia.org/wiki/Hash_table) is a data structure that implements an associative array abstract data type, a structure that can map keys to values. A hash table uses a hash function to compute an index, also called a hash code, into an array of buckets or slots, from which the desired value can be found. During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored.

### Terminology

A hash table has the following terminology:

* **Hash** in the case of hash table data structure, the hash used to determine the index of the array

* **Buckets**  A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs. each bucket is a linked list that contains many key-value pairs in case of collision.

* **Collisions** when the hash result in the same index for different keys.

### Structure 

adding and getting values from the hash table is done using an index that has been evaluated using the hash, so the time complexity to add and to get data from the hash table is **O(1)**

* To create a hash table you first need to create an array with a fixed size (1024 size is recommended)

* At each index create a linked list to add key-value pairs in case of collision.

* add the following methods:

  1. `getHash(String <key>)` method that takes in a key as an argument and returns an integer the represents the index in the main array.

  evaluating a key to an integer can be done in many ways. For example, sum the ASC of each character of the key:

  ```java
    key = "name"
    sum = ASC('n') +  ASC('a') + ASC('m') +ASC('e')
    sum = 110 + 97 + 109 + 101
    sum = 417
    // the sum needs to be in the range of the array size (0 - 1023) so that take the modulus of the array size
    sum = sum % 1024 // the index of name will be 417
  ```

  2. `add(String <key>, String <value>)` method that adds to the hash table.
  
   In order to add the key-value pair to the hash table, first pass the key to the `getHash(String <key>)` method to get the index where to add the data then checks if the bucket has already data or not, if it has data, then add the key-value pair at the end of the linked list

  3. `find(String <key>)` method that gets the value of the key if exists.

    to get the index of the key pass it to `find(String <key>)` method, then search for the key-value at that index and return its value if exists

  4. `contains(String <key>)` method that checks if a key-value pair exists

    works pretty much the same as `find(String <key>)` method, but it returns `true` if the key is found and returns false if not.






### Why do we use a Hash Table
* To hold unique values
* Dictionary
* Library

