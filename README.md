# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

First you need to FORK this repo into your account, then you need to CLONE that foreked repo, the one in your account. 
When you are finished with your code, be sure to ADD/COMMIT and PUSH your code to your repo.

Use the URL from your repo as the submission to the portal. 

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created. 40$
* Use `insertMoney` method to simulate inserting an amount of money into the machine. 50$
* Use `getBalance` to check that the machine has a record of the amount inserted. 50$ + 40$
    * You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.
    
### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?
String "Ticket price:40 cents. Your total is 90$"
### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
    * Do you notice anything strange about the machine’s behavior? Yes, we were charged for 40 cents, however still had a total balance of 90
    * What happens if you insert too much money into the machine – do you receive any refund? I inserted 90$, however, did not get a refund. I went
    * What happens if you do not insert enough and then try to print a ticket? I inserted 10$ and still got a ticket. Also, went to getbalance, and realized it was at 0, very odd.

### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
    * Buy a ticket from that machine.
    * Does the printed ticket look different?
    The ticket price changed to my new ticket price (10$), however it still printed me a ticket even though I didn't insert any money.

### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
Public class Student{}
Public class LabClass{}

### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

Yes, I believe so

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
    * Do you notice a change in the class diagram? Yes, it will not compile, and gives me an error.
    * What error message do you get when you now press the compile button? <identifier> expected also class, interface, enum or record expected.
    * Do you think this message clearly explains what is wrong? I don't think so, if I didn't know we swapped class with public,I wouldnt really understand the error message. However because I went through this excercise, I now know what to look out for.
### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
    It is possible. I was able to compile everything
### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
    * Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
    * 
    * Constructor = public TicketMachine(Integer ticketCost)
    * Fields = price, balance, total, ticketNumber
      Methods = calculateTotal(), getBalance(), getPrice(), insertMoney(integer amount), incrementTicketNumber(), printTicket(),
    
    
        
    * Hint: There is only one constructor in the class.

### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class? The constructors name was the same of the Class, it also does not return anything.

### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count; - Integer
private Student representative; - Student
private Server host; - Server

### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive; alive
private Person tutor; tutor
private Game game; game
```
### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in? yes
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
    * Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are
possible? Yes, order is very important.
    * Check by pressing the compile button to see if there is an error message.
    * Make sure that you reinstantiate the original version after your experiments!

### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration? Yes, this tells the program to stop
* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.
* private int status;

### Exercise 2.16
* To what class does the following constructor belong? Student
```
public Student(String name)
```

### Exercise 2.17
* How many parameters does the following constructor have and what are their types? 2
```
public Book(String title, double price)
```

### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be? title, price, author, hardCover, 
* Can you assume anything about the names of its fields? that you must input a string Title as a parameter and a numerical value for double. However we do not know all the fields. 

READ upto and INCLUDING section 2.15 of this chapter.
