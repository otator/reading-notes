# Inheritance and Interfaces
### Inheritance
Inheritance needed when some parts of code have common code with eachother. so instead of writing the same code in all these class, a parent class can be created that contains the common part of code and the other class can inherits this class and uses its code without the need to re-writing it again and again.

using the keyword **extends** after the class name followed by the class that need to inheite from, will inherite all the methods and the fields inside the parent(super) class.

**the child class can inherite only the methods and fields that defined either as public or protected ONLY**

a class *Bicycle* that contains common fields such as `speed`, `cadence` and `gear`, and methods such as `speedUp()`, `changeGear()`, `applyBreaks()` and so the forth can be inherited by other class such as *MountainBike* and *RoadBike* where all the above methods and fields can be used from within these two classess.

the *MountainBike* and *RoadBike* can implement their own code that different form eachother.


### Interfaces
interfaces in java they are like a contarct with the classes are implementing them, they have only final fileds(that their values can not be changed) and not implemeted methods(only the method name, its return type and its parameters)

the keyword that used to impelment the interface is **implements**.

once the class implemets an interface it MUST implement all the methods that defined in the interface, to do that an annotation *`@Override`* is used.

