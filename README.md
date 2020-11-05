# ATM-Bank-project-using-java
import java.util.*;
public class bank {
    public static void main(String args[])
    {
       Scanner sc= new Scanner(System.in);
       int userChoice;
       boolean quit=false;
       float balance=0f;

       do {
           System.out.println("Your choice, 1 to Deposit Money:");
           System.out.println("Your choice, 2 to Withdraw Money:");
           System.out.println("Your choice, 3 to Check Balance:");
           System.out.println("Your choice, 0 to quit:");
           userChoice = sc.nextInt();
           switch (userChoice)
           {
               case 1:
                   float amount=0;
                   System.out.println("AMOUNT TO DEPOSIT:");
                   amount=sc.nextFloat();
                   if(amount<=0)
                   {
                       System.out.println("CANT DEPOSIT NON POSITIVE AMOUNT");

                   }
                   else {
                       balance += amount;
                       System.out.println("$" + amount + "has been deposited");
                   }
                   break;
               case 2:
                   System.out.println("AMOUNT TO WITHDRAW:");
                   amount=sc.nextFloat();
                   if(amount<balance)
                   {
                       System.out.println("CANT WITHDRAW");

                   }
                   else {
                       balance -= amount;
                       System.out.println("$" + amount + "has been withdrawn");
                   }
                   break;
               case 3:
                   System.out.println("YOUR BALANCE:  $"+balance);
                   break;
               case 0:
                   quit=true;
                   break;
               default:
                   System.out.println("Wrong choice");
           }
           if (userChoice == 0)
               quit = true;
       }while(!quit);
       System.out.println("Bye");
       }
    }
