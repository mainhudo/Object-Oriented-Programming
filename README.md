# Object-Oriented-Programming

 #Object-Oriebted 
#Consider a class time that represents a point in time, 9am or 3:30 pm. 

Give two sets of instance variables that can be used for implementing the Time class

#Method: part of class definition

#accessor: quiery the object for some infor without changing it  e.g getTotal getCount

#
#Defines the Time Clas with this module
  class Time :

    def getValue(self):
  
    return self._value
    
  def click(self) :
  
    self._value = self.value + 1
  def reset(self) :

    self._value = 0    
    
    #Construct an object
    
    
     time1 = Time()

     #Invoke a classmethod

     result = time1.add()


     time1 = reset()

     result = time1.addItem()

     print(time1.getCount(), time1.getTotal())


#All instance of the variables should be private and most methods should be public. Python does not explicitly hide or protect private members from outside accessor
#Common practice among Python programmers to use names that begin with single underscore for private instance variables and methods

#Encapsualtion is encouraged: in which all instance variables ar private and are only manipualted with methods.

#2.Constructor defines and initializes instance variables of an object. Automatically called whenever an object is created.
To create instance of the CashRegister

    register = CashREgister()

The reference is saved in a variablesPython uses the special name__init__for the constructor because it initializes an instance of the class:
  
      def__init__(self) :
        self._itemCount = 30
        self._totalPrice =0 
    
Self is always the first parameter variables
Create an instance variables:
        self._itemCount = 0 
    
Create an empty list: 
        empty = list()

Constructor: 

         class ClassName : 
            def__init__(self)
            self.balance = 0.0 

#Python allows you to use only one constructor per class but you can define constructor with default argument values that stimulate multiple definitions

You can include a default argument for the initialBalance parameter variable 
     class BankAccount 
     def__init__(self, initialBalance = 0) :
       self._balance = initialBalance
       
    
Example #if an object is constructed as harry = Person("Harry", "Morgan")    
     class Person :
       def__init__(self,firstname, lastname) :
         self._name = lastname + "," + firstname     >>> A constructor always start with "self"
    
   it will folow the last name and first name, so Morgan Harry is the name
    
    
Example Provide  an implement for a Person constructor so that after the call p = Person()
the _name instance variable of p is "unknown"

   class Person :
     def_init_(self):
       self._name = "unknown"
    
Example of an Item class whose objects contain two instance variables, a string description and a floating-point value_price
   class Item() :
     def__init__(self) :
       self._description = ""
      
      def _init_(self):
        self._price = 0.0

Define a constructor for the Item class 

Item("Corn Flakes")
Item("Corn flakes, 3.95")
Item()

     class Item():
       def_init_(self, description, price) :
         self._price = 0.0
         self._description = ""

Example :Define and implement a method giveChange(self, payment) for the Cashregister class that gives change for the provided payment and resets the cast register for the next sale

class Register() :
  def__init__(self):
    self._price = 0.0 
    self._itemcount = 0.0 
  def__init__(self, payment) :
    self._register1 = Cashregister()
    self._totalPrice = self_totalPrice - payment
    self._itemcount = self._itemcount + 1 
    self._reset()
    return change 
#Python is a dynamic language in which all variables are created at run-time. There is nothing prevent you from creating instance variables in any methods of a class. 
Sometimes, a value properly belongs to a class = CLASS variables, that belongs to the class, not to any instance of the class 

class BankAccount : 
  _lastAssignedNumber = 1000 
  def__init__(self) :
    self._balance = 0 
    BankAccount._lastAssignedNumber = 
4.   
 A Unit test verifies that a class works correctly in isolation, outside a complete program As your class gets more complex you should write a tester programs. is a driver module that imports the class and contains statements to run methods of your class. 
 from cashregister import Cashregister 
 register1 = CashRegister()
 register1.addItem(1.95) 
 register1.addItem(0.95) 
 register1.addItem(2.50)
 print(register1.getcount())
 print("Expected:3")
 print("%.2f" % register.getTotal())   >>> This is how you print out a value with ""
 
 
 The result will print 
 3 
 expected: 3
 5.40 
 Expected: 5.40 


Determine the expected result in advance is important. Import the class you are testing into the driver module:
 5. Implement a class
 - Get informal list of the responsibilities of your objects (e.g reset the cash register?)
 - Specify the public interface :Turn the list into set of methods with speciific parameterer variables and return values. addOption(option) or getInput() for Example
 - Document the public interface: Supply a documentation comment for the class, then comment each method. class () > def > def 
 - Determine instance variables 
 - Implement the constructor : 
 - Implement the methods : def addOption(self, option) :
     self._options.append(option)
- Test your class : write a short execution program. It should call the methods that you found in Step 2 

 6. Counting events 
 e.g count the bank transactions and how many items been added in a sale.
    eaxmple : 
 def addItem(self, price):
   self._totalPrice = self_totalPrice + price 
 
 
7.  Increment the counter in those methods correspond to the events that you want to count. May need to clear the counter. 

def addChoice(self, choice) : 
  self._choice.append(choice) : 


  Excercise: Objects and Classes : 
  - Consider a Car class that simulates fuel consumption in a car. Assume fixed efficiency. Make a card for the car. 
  
  Car My Car : reset, addGallon(amount), getGasLeft
  
8. MAnage Properties of an Object 
Property is a value of an object that a user of that object can set and retrieve. A Student object may have a name an an ID. 
   Object property and be accessed with a getter method and charged with a setter methof 
   
   class Student :
     def__init__(self) :
       self._name = ""
       
     def getName(self) :
       return self._name
    def setName(self, newName) :
      self._name = newName 
    
  Sometimes we should do error checking like reject a blank name: 
  
      
9. Types of reference : Variable merely holds the memory location of an object. The object itself is stored elsewhere. So Object reference to denote the memory location of an object.  None Reference: Self Reference, Shared Reference 

***You use the is operator(and not==) to test whether an object reference is None. 
if middleInitial is None : 
  print(firstName, lastName)
else: 
  print(firstName, middleinitial + ".", lastName)
  EMPTY STRING ('') IS A VALID STRING OF LENGTH 0. NONE REFERS TO NOTHING AT ALL

The lifetime of an object  : The object first contains no instance variables. 
  self._itemcount = 0 instance variables are added to the objects. 
When the reference constructor exists, it returns a reference to the object, captured in a variable : 
    reg1 = CashRegister()
    
Excercise : Implement a VotingMachine class that can be used for a simple elections. Have methods to clear the machine states, to vote for a Democrat or Republican, and get tallies for both parties 

Class Voting : Add votes republic, add votes democrats, and reset, and display votes : 
Construct a voting register with cleared item count and total  
  class Vote(): 
    
    def Electionvote: 
      def__init__(self, vote) :
        self._votedemocrat = 0 
        self._voterepublican = 0 
        self._talliesdemocrat = 0 
        self._talliesrepublic = 0 
    
    #Adds Item to this register: 
    
    def addItem (self, vote):
      self._votedemocrat = self._votedemocrat + vote
      self._voterepublican = self.voterepublican + vote
    # Get all the votes 
    def getTotalDemocrat(self) : 
      return self._votedemocrat
    def getTotalRepublican(self) : 
      return self._voterepublican
    def clear(self) : 
      self._votedemocrat = 0
      self._voterepublican = 0 
      self._talliesdemocrat = 0 
      self._talliesrepublic = 0 
      
      
      
        
   
  
      
      
 
 
    
    
  
