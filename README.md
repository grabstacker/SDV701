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
## 04/03/2020 Class notes

  try stay away from arrays and use dictionarys and lists instead as they are better for expansion.

  Arrays are good for dealing with things that are fixed in size like days of the week.

  composite is filled in sideways triangle

  many students in many courses

  DECOUPLING is the goal

  Ownership is the key who owns what and why when refactoring code

  Drawing diagrams in UML helps figure out the structure and dependancies

  clsArtist needs its own methods to get and set etc the private fields

Refactoring.com/catalog/

setters and getters can be used to create good error catching for the input data

get{}
set{
  if value != null <-- for example>

}

artistdialog should not be pointing to a frmClass


ELSE{
Throw new exception("use this instead of else in some error try catches");
}

avoiding using windows relient things like a messagebox inside business classes
try keep it in the frmMain or any forms

use code snippeets to encapsulate try catch on criticle code that should run with no errors


try{

}
catch(Exception ex){
  messagebox.show(ex.GetBaseException().Message)  <--- base exception

}

## Week 3 class 09/03/2020

Design patterns

Look into null objects to handle object != null throughout the program.

"each patter describes a problem which occurs over and over again in our enviroment, and then describes
the core of the solution to that problem in such and way that u can use this solution,"

patterns are literal things like all websites might have a login or logout and a shopping cart
This is apart of the analysis of the website. reoccuring and real world problems and solution

Architechural patterns are the structure of all systems
MVC etc

---------------------
PATTERNS
  analysis design acrhitechural
  general gang of Four
  Fundemental grasp creational stuctula behavioual
  --------------------
   coupling is the link between things which you want to reduce

   This is like a fundemental like reducing coupling
   
   GRasp is your general logical thinking when making common decisions about where to store something

   A good example of what is the good place for something is an art and should be relient 

   Gang of four - BOOK

   Design patterns pdf book

   analysis pattern for example is the undo function when working with word

   design pattern enable large scsale reuse of software architectures 

   patterns explicitly capetr expert knowledge and deisng tradeiffs and make this expertise more widle avaialable

   patterns heko unoirive developer communication
    
   Patterns helo ease the transistion to object oriented technnology

## Week 3 Class 2 10/03/2020

-----BOOK GANG OF FOUR DESIGN PATERNS------

PATTERN: Problem <--> Solution 
  tried and tested

  Achitechual pattern MVC

  Design patterns: general, --- 
    P
    
    General responsibility assignment software patterns

    ******Responibilty should be assigned to the class that has all the information

    Expert Cohesion

    Low coupling is the task of trying to stop a web of connections and create simple structures in the program

    save and retrieve were moved out of the form and into the closer to where the data is which is the clsArtistList
    class

    Polymorphisim is the ability for something like a class to adapt to the current situation

    DONT TALK TO STRANGERS law of delimiter  --- places constaint on what objects you should send messages to

    frmMain needs to know about the ArtistList because it is literally displaying the information so the coupling is warrented

    circular refenerece is bad

    Exceptions
      Button clicks are the main area where you will need things like a try catch statement to get the exception
      inside the event routines

  ----CREATIONAL PATTERNS----
  factory method virtual construtor --- provide an interface for creating a link 

  ----SINGLETON PATTERN-----

 the intent of the singleton pattern as defind in the design patterns is to ensure a class has only one instance and probide a global point of access to it.

 A global static variable counter is a good example of how only one reference is wanted throughout the entire program

 if there is no constructor in a class it will call its inherited class constructor

 PROTECTED means you cannot create new instances

 PRivate consrtutor does a similar this is used to only be used by the immediate intances class

The below class makes its so only one class Singleton can instantiate the Singlton();

 sealed class Singleton
 {
    private Singleton(){}
    public static readonly Instance = new Singlton();
 }

The constructor allways needs to be public if you want to call it from other locations

frmArtist for example needs to be public to be called in other locations like when you call the form from another class or method.

Generating a static readonly intance of the class above

private frmArtist(){
  InitialiseComponent()
}
public static readOnly frmArtist Instance = new frmArtist(); <---> using instance to call private methods 

private static frmArtist _ArtistDialog = frmArtist.Instance;

SEALED is also called FINAL in java



## Week 4

 USing sql server for the database


  Complex pattern example:
 AIM
    flexability 
      GUI BUSINESS LOGIC DATA(BASIC)
    
    standairsed 
    expectation by team or company
    conventions/ patterns
    
    ease of management
      current programmer future programmer new features


      TIER vs LAYER
       teir is on different machines processes the run independantly
        can be different hardware
        different threads

       layer is organisational elements and seperation of concearns

       layer is multple processes on one thread and tier is different nodes completely



       tech change                     Most likly

       business rules

       business data change            Least likley


--------OPTIMISIM DEPENDANCY----------

VARIABLE COMPONENT ---> STABLE COMPONENT

    GUI ---> BUSINESS/LOGIC ----> DATA

    OBSERVER PATTERN

      OBSERVER ---- SUBJECT


      mechanism to transform direct into indirect dependancy

      Notifying the cleints rather than the client pulling the dat cn sometimes be more effecient
      This is a good eaxmple of a client on a stock market client server or an airport monitors being
       pushed data rather than ALL of the clients pulling information at the same time
      using lots of resources
    

    a delegate is simply and address of a function or a pointer to a function

      single delegate is a programming pattern

      one to many dependancy so that when one object changes state it notifies many

      Multiple delegates