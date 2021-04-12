# OO Design 
[SOLID](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design) is an acronym for the first five object-oriented design (OOD) and it stands for:

**S** - Single-responsiblity Principle
**O** - Open-closed Principle
**L** - Liskov Substitution Principle
**I** - Interface Segregation Principle
**D** - Dependency Inversion Principle

### Single-responsiblity Principle
means that the class must have only one job 

### Open-closed Principle
Objects or entities should be open for extension but closed for modification.

### Liskov Substitution Principle

Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T. [link](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design#liskov-substitution-principle)

This means that every subclass or derived class should be substitutable for their base or parent class.

### Interface Segregation Principle

A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use. [link](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design#interface-segregation-principle)

### Dependency Inversion Principle
Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions. 
[link](https://www.digitalocean.com/community/conceptual_articles/s-o-l-i-d-the-first-five-principles-of-object-oriented-design#dependency-inversion-principle)
