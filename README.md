midterm
=======


1. What is a Java class? (10 points)

A: A java class is a blueprint from which an object is created.



2. What is the difference between declaring a variable and instantiating a variable (10 points)

A: declaring a variable tells the compiler the type.
   instantiating a variable gives it a value.





3. Write a Odd/Even game, where the user is asked to guess whether a system generated number is Odd or Even (50 points)




4. Allow the user to play until the user no longer interested (20 points)




5. Keep track of number of wins and loses and inform user upon game completion (10 points)




6. Use a class to generate the randome odd/even number (5 points)




7. Add a method to test whether the number is odd/even, and use it in the game (10 points)




// odd even game


import java.util.Scanner;

public class OddEvenGame

{

        public static void main ( String[] args)

        {


                Scanner input = new Scanner (System.in );


                int computerNumber;

                int odd = 1;

                int even = 2;

                int userAnswer;

                int countTimesUserIsCorrect= 0;
                
                int countTimesUserIsWrong=0;

                String userPlaysAgain;
 

// Random Number 
                
        do
        {
        	computerNumber = 1 + (int) (Math.random() *1000);
        	System.out.printf("The Computer chose %d.\n", computerNumber);
        	
// user Input 
        	
        	System.out.print("Did the computer generate an odd (1) or even (2) number?");
        	userAnswer = input.nextInt();
        	
        	if ( userAnswer == odd && computerNumber % 2 !=0);
        	
        	{ 
        		System.out.println(" You Guessed it right!!");
        		++countTimesUserIsCorrect;
        		
        	}
        	
        	else (userAnswer == odd && computerNumber %2 ==0);
        	{
        		System.out.println(" You Guessed Wrong!!");
        		++countTimesUserIsWrong;
        		
        	}
        	
        	else (userAnswer == even && computerNumber %2 ==0);
        	{
        		System.out.println(" You Guessed Right!!");
        		++countTimesUserIsCorrect;
        	}
        	
        	
        	        	
        	System.out.println("Do You Want To Play Again??");
        	userPlaysAgain = input.next();
        	
// Keep playing??
        	
        } while(userPlaysAgain.equalsIgnoreCase("Y"));
        if (userPlaysAgain.equalsIgnoreCase("N"));
        		System.out.printf("Good Bye");
        		
//Player's right and wrong answers.
        		++countTimesUserIsCorrect;
        		++countTimesUserIsWrong;
        
  
}
}
