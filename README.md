# PROGRAMMING-Java-

This is an Java Programming assignment based on three questions

QUSETION 1
Question 1 it all about the following:

Employee Salary Update Program
Description
This Java program reads employee data from a text file, updates their salaries based on the number of years they have worked, 
and writes the updated information back to the file. The salary increments are based on the following criteria:

Employees who have worked less than 5 years receive a 5% increase.
Employees who have worked between 5 and 10 years receive a 15% increase.
Employees who have worked more than 10 years receive a 30% increase.
File Structure
employee.txt

The employee.txt file should contain the following content:

Name Surname Years Worked Salary
John Smith 4 15000
Ayanda Dube 10 200000
Damien Naidoo 5 65000

Java Files
Testing.java
Employee.java
Usage
Ensure the employee.txt file exists in the same directory as your Java files.

Compile and run the Java program:

javac Testing.java Employee.java
java Testing
The program will read the employee data, update their salaries, and overwrite the employee.txt file with the updated information.

Code Explanation:

Testing.java
The Testing class contains the main method which:

Reads the employee.txt file.
Parses the employee details and stores them in a list of Employee objects.
Updates the salary of each employee based on the specified criteria.
Writes the updated employee details back to the employee.txt file.

Task.java
The Task class contains attributes and methods for handling task data:

Attributes: taskName, taskId, taskWage
Constructor: Initializes the attributes
Getter and Setter methods
toString() method to display task details

TaskWorker.java
The TaskWorker class extends Thread and implements the run method:

Contains attributes for a Task object and a boolean indicating whether to display additional information
Constructor: Initializes the attributes
run method: Pauses the thread, displays task details, and shows the thread's name, priority, and status
Methods to display task details with or without additional information

Exception Handling
The program uses try-catch blocks to handle InterruptedException that may occur during thread sleep operations.



QUESTION 2
Question 2 it all about the following:

Task Details Program
Description
This Java program demonstrates the use of threads to display task details. The program defines a Task class to store 
information about tasks and creates worker threads to display this information. 
The threads are configured with different priorities and sleep for a specified time before 
displaying the task details. Additionally, the program checks and displays each thread's status, name, and priority.

File Structure
Java Files
Taskdetails.java
Task.java
TaskWorker.java
Usage
Ensure all Java files are in the same directory.

Compile and run the Java program:

javac Taskdetails.java Task.java TaskWorker.java
java taskdetails.Taskdetails
The program will create two tasks and two worker threads. The threads will display task details after a brief pause and will show their priorities and statuses.

Code Explanation
Taskdetails.java
The Taskdetails class contains the main method which:

Creates two Task objects.
Creates two TaskWorker threads with different priorities.
Starts the threads.
Waits for the threads to finish execution using join().
Displays the status of each thread.

Task.java
The Task class contains attributes and methods for handling task data:

Attributes: taskName, taskId, taskWage
Constructor: Initializes the attributes
Getter and Setter methods
toString() method to display task details

TaskWorker.java
The TaskWorker class extends Thread and implements the run method:

Contains attributes for a Task object and a boolean indicating whether to display additional information
Constructor: Initializes the attributes
run method: Pauses the thread, displays task details, and shows the thread's name, priority, and status
Methods to display task details with or without additional information

Exception Handling
The program uses try-catch blocks to handle InterruptedException that may occur during thread sleep operations.



QUESTION 3
Question 2 it all about the following:

Blackjack Game
Description
This Java program simulates a simple game of Blackjack, played against a dealer. The game's objective is to have cards whose total value 
is as close to 21 as possible without exceeding it. The player wins by having a higher total than the dealer without busting (going over 21).

How to Play
Deal Cards: Both the player and the dealer are dealt two cards each.
Player's Turn: The player decides to either:
Hit: Draw another card.
Stand: End their turn without drawing more cards.
Dealer's Turn: The dealer draws cards until their total is at least 17.
Determine Winner: The winner is determined based on the total points of the player and the dealer.
Card Values
Face cards (J, Q, K) count as 10 points.
Aces count as either 1 or 11 points, whichever is more favorable without busting.
All other cards count as their numeric value.
Class Structure
Card
Stores the rank and suit of a card.
Provides methods to get the card's rank, suit, and value.
Deck
Stores a collection of 52 cards.
Provides methods to shuffle the deck and draw cards.
Hand
Stores the cards in a player's or dealer's hand.
Provides methods to add cards, calculate the total points, and display the hand.
BlackjackGame
Manages the game flow, including dealing cards, handling player and dealer turns, and determining the winner.
Usage
Ensure all Java files are in the same directory.

Compile and run the Java program:

javac -d . Card.java Deck.java Hand.java BlackjackGame.java TestingGameCard.java
java testinggamecard.TestingGameCard
Follow the on-screen instructions to play the game.

Example Gameplay
Player's hand: 10 of Hearts, 5 of Diamonds
Player's points: 15
Player action: hit
Player's hand: 10 of Hearts, 5 of Diamonds, 3 of Clubs
Player's points: 18
Player action: stand
Dealer's hand: 7 of Spades, 9 of Hearts
Dealer's points: 16
Dealer action: draw
Dealer's hand: 7 of Spades, 9 of Hearts, 6 of Diamonds
Dealer's points: 22 (bust)
Result: Player wins!
Exception Handling
The program handles invalid input during the player's turn.
The program checks if the deck is empty before drawing a card.
Code Explanation
TestingGameCard.java
The TestingGameCard class contains the main method to start the game.

Card.java
The Card class stores the rank and suit of a card and provides methods to retrieve and display them.

Deck.java
The Deck class creates a standard 52-card deck, shuffles it, and provides a method to draw cards.

Hand.java
The Hand class manages the cards in a player's or dealer's hand, calculates the total points, and displays the hand.

BlackjackGame.java
The BlackjackGame class manages the game flow, including dealing cards, handling player and dealer turns, and determining the winner.
