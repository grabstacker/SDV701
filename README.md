# SDV701

## Class 02/03/2020

Looking at serializable 

## Program to Interface, not to an implementation ##

Implementing means writing code

An interface must have atleast one method
An interface is a very abstract class and contains only abstract methods no code

  An abstract class is a class that is declared abstract — it may or may not include abstract methods. Abstract classes cannot be    instantiated, but they can be subclassed. An abstract class may have static fields and static methods.

  It is legall to have a form of multiple inheritance safely 

  Interface 
    -contract
      .responsibilty
      .benefit
      -only abstract methods => no code
      -Ability
      -no data

      interfaces often have i infront to identify it as an interface

      anything that streams down the inheritance tree can be accessed if inheirted in the subclasses

      "the interface segregation principle"

      A dictionary is a lookup table

      key and value!


      When extracting a method it is wise to take note of breaking the code with fields and paramemeters that are attached to the code.

      PROTECTED is sharing with all of the sub classes through inheritance

      Private is only to the current class but is irrelevant if setters and getters are present

      ABSRACT has no methods and is only inheritated from using protected fields You can declear
      methods in the superclass to be overridden in the sub classes
  
      public abstract void PrintDetails() <-- needs to be over ridden in the subclass
      public abstract void PrintNames()  <-- needs to be over ridden in the subclass

      public override void PrintDetails() <-- overriden in the subclass
      public override void PrintName() <-- over ride in the subclass

        Paralell heirachy is when there is two uml heriachies of say the frms and the classes

HOMEWORK - OO and refactoring with interfaces and inheritance
  " : " colon means inherite or implements
## 