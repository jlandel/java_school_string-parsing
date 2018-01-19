# java_school_string-parsing
This is my first assignment for my Java II Programming class
/**
 * @author Josh Landel
 * Java Programming II
 * Chapter 4
 * 1/18/2018
 */
package stringparsing1;
import java.util.Scanner;

public class StringParsing1 {
    public static void main(String[] args) {
        /// Variables 
        String first;
        String last;
        String full;
        String[] names;
        //Scanner class to recieve input
        Scanner sc = new Scanner(System.in);
        //Ask for input
        System.out.println("Enter your full name:");
        //Type your name
        full = sc.nextLine();
        //Space infront of the name is removed
        full = full.trim();
        //Sepereates the names into 2 parts and adds them to the array
        names = full.split(" ", 2);
        first = names[0];
        //If the second part of the name has extra spaces at the beginning of it
        //then they are removed
        last = names[1].trim();
        // prints the names in the order regardless if they are last, first or
        // first last
        if (first.endsWith(",") == true)
        {
            //If their is a comma after the first word, then the program will 
            //know that it is by last, first and keep the order
            System.out.println("Your full name is: " + first + " " + last);
        }
        else {
           // else the names will flip and a comma is addded
           System.out.println("Your full name is: " + last + ", " + first);
        }
    }    
}
