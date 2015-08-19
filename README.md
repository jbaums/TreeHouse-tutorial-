# TreeHouse-tutorial-

import java.io.Console;
 
public class TreeStory {
    
    public static void main(String[] args) {
        Console console = System.console();
        /*  Some terms:
            noun - Person, place or thing
            verb - An action
            adjective - A description used to modify or describe a noun
            Enter your amazing code here!
        */
      String ageAsString = console.readLine("How old are you?  ");
      int age = Integer.parseInt(ageAsString);
      if (age < 13) {
        //Insert exit code
        console.printf("Sorry you must be at least 13 to use this program.\n");
        System.exit(0);
      }
      String name = console.readLine("Enter your name:  ");
      String adjective = console.readLine("Give me your favorite adjective:  ");
      String noun;
      boolean isInvalidWord;
      do {
        noun = console.readLine("Enter a noun:  ");
        isInvalidWord = (noun.equalsIgnoreCase("dork") ||
                         noun.equalsIgnoreCase("jerk"));
        if (isInvalidWord) {
          console.printf("That language is not allowed.  Try again. \n\n");
            }
        } while(isInvalidWord);
      String adverb = console.readLine("Enter an adverb:  ");
      String verb = console.readLine("How about a good verb ending in -ing:  ");
      
      console.printf("Your TreeStory:\n----------------\n");
      console.printf("%s is a(n) %s %s. ", name, adjective, noun);
      console.printf("They are always %s %s.\n", adverb, verb);
      
    }
    
}
