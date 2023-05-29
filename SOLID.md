# SOLID Design Principles

## S -> Single Responsibility
## O -> Open close
## L -> Liskov substitution
## I -> Interface segregation
## D -> Dependency Inversion


### ____________________________________________________________________________________
# Single responsibility
    All of the classes, objects, modules should have a single responsibility

## Examples

Logger example -> telling user via log, if its in a seperate module we can change it to email

### REACT
    Seperate API calls into hooks. 
    Filter implementation in hooks. 
    In case if there's any change we will just need to change hook logic.

### ____________________________________________________________________________________
# Open close
    Component should be open for extension but close for modification

## Examples

### REACT
    HOC could be an examples
    Extending classes
    Passing icon to child component, rather than putting condition inside child


### ____________________________________________________________________________________
# Liskive substituion 
If you are inheriting class A from class B, so you should be able ot use class B in place of class A and it should work fine

## Examples
    If we extend rectangle class from square class, so in every place where we are using square we should be able to use rectangle class as well.

```
class Shape {

}
class rectangle extends shape{

}
class square extends shape{

}
```

### ____________________________________________________________________________________
# Interface segregation
Class implementing an interface should use all the portion of the code.

## Example
    Lets say we have a class implementing an interface, and interface has property/method A, B and C. So this principle states that the class implementing it should use all the properties/methods


### ____________________________________________________________________________________
# Dependency inverision
DIP is basically the idea that high-level modules/implementations should not depend on lower level modules/implementations

## Example
    Payment gateway example -> The basic information should always remain same, ( i.e higher level module should contain all the information ). And then pass the information to payment gateway modules, which will only deal with specific payment methods. 