Midterm-CS112
=============

MidTerm




package cmpr112101414;
import javax.swing.JOptionPane;
public class Midterm
{
public static void main(String[] args)
{
MidtermMath classtest = new MidtermMath();
String playAgain = "Yes";
int wins = 0;
int losses = 0;
do
{
//Receive input
String userInput = "";
do
{
userInput = JOptionPane.showInputDialog("Even or Odd");
} while (!(userInput.equals("Odd") || userInput.equals("Even")));
//Generate a random even or odd number, 50-50 chance.
int randNumber = classtest.getRandNumber(1, 2);
String compRandom = (classtest.isEven(randNumber)) ? "Even" : "Odd";
//test userInput against computer random generator
if(compRandom.equals(userInput))
{
JOptionPane.showMessageDialog(null, "You guessed correctly.");
wins++;
}
else
{
JOptionPane.showMessageDialog(null, "You guessed incorrectly because the computer selceted: " + compRandom);
losses++;
}
//display wins and losses
JOptionPane.showMessageDialog(null, "You have won "
+ wins + " times and you have lost "
+ losses + " times");
//Ask to play again
playAgain = JOptionPane.showInputDialog("Wish to play again? [Yes/No]:");
} while (playAgain.equals("Yes") || playAgain.equals("yes"));
}
}




1)	Java classes contain fields and methods and is a blueprint from which individual objects are created.

2)	When you declare a variable, you tell the computer to reserve some memory for your program to store some data while instantiating a variable means that the class’s memory is being allocated for a new object and returning a reference to that memory.
