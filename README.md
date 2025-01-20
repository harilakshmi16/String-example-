# String-example-
String Example

public class StringPrograms {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
       
        System.out.print("Enter the first string: ");
        String str1 = scanner.nextLine(); 

        System.out.print("Enter the second string: ");
        String str2 = scanner.nextLine();

        System.out.println("\nChoose a string operation:");
        System.out.println("1. Find Length");
        System.out.println("2. Convert to Uppercase");
        System.out.println("3. Convert to Lowercase");
        System.out.println("4. Reverse the String");
        System.out.println("5. Concatenate Strings");
        System.out.println("6. Compare Strings");
        System.out.println("7. Check if Substring Exists");
        System.out.println("8. Replace a Character");
        System.out.println("9. Find Character at Index");
        System.out.println("10. Split the String");
        System.out.println("11. Trim Whitespaces");
        System.out.println("12. Check if String is Empty");
        System.out.println("13. Convert to Character Array");
        System.out.println("14. Exit");
        
        int choice;
        do {
            System.out.print("\nEnter your choice: ");
            choice = scanner.nextInt();
            scanner.nextLine(); 

            switch (choice) {
                case 1:
                    System.out.println("Length of first string: " + str1.length());
                    System.out.println("Length of second string: " + str2.length());
                    break; 

                case 2:
                    System.out.println("First string in uppercase: " + str1.toUpperCase());
                    System.out.println("Second string in uppercase: " + str2.toUpperCase());
                    break; 

                case 3:
                    System.out.println("First string in lowercase: " + str1.toLowerCase());
                    System.out.println("Second string in lowercase: " + str2.toLowerCase());
                    break; 

                case 4:
                    System.out.println("Reversed first string: " + new StringBuilder(str1).reverse());
                    System.out.println("Reversed second string: " + new StringBuilder(str2).reverse());
                    break; 

                case 5:
                    System.out.println("Concatenated string: " + str1.concat(str2));
                    break; 

                case 6:
                    int comparison = str1.compareTo(str2);
                    if (comparison == 0) {
                        System.out.println("Strings are equal.");
                    } else if (comparison > 0) {
                        System.out.println("First string is lexicographically greater.");
                    } else {
                        System.out.println("Second string is lexicographically greater.");
                    }
                    break; 

                case 7:
                    System.out.print("Enter a substring to check in the first string: ");
                    String substring = scanner.nextLine();	
                    
                        if (str1.contains(substring)) {
                        System.out.println("Substring exists in the first string: " + str1.contains(substring));
                    } else {
                        System.out.println("Substring does not exist in the first string.");
                    }
                    break; 

                case 8:
                    System.out.print("Enter the character to replace: ");
                    char oldChar = scanner.next().charAt(0);
                    System.out.print("Enter the new character: ");
                    char newChar = scanner.next().charAt(0);
                    System.out.println("First string after replacement: " + str1.replace(oldChar, newChar));
                    System.out.println("Second string after replacement: " + str2.replace(oldChar, newChar));
                    break; 

                case 9:
                    System.out.print("Enter the index to find the character (0-based): ");
                    int index = scanner.nextInt();
                    try {
                        System.out.println("Character at index " + index + " in first string: " + str1.charAt(index));
                        System.out.println("Character at index " + index + " in second string: " + str2.charAt(index));
                    } catch (IndexOutOfBoundsException e) {
                        System.out.println("Index out of range!");
                    }
                    break; 

                case 10:
                    System.out.print("Enter the delimiter to split the first string: ");
                    String delimiter = scanner.nextLine();
                    String[] parts = str1.split(delimiter);
                    System.out.println("First string split into parts:");
                    for (String part : parts) {
                        System.out.println(part);
                    }
                    String[] parts2 = str2.split(delimiter);
                    System.out.println("Second string split into parts:");
                    for (String part : parts2) {
                        System.out.println(part);
                    }

                    break; 

               /* For example, if str1 = “apple,banana,orange”  and the user inputs , (comma) as the                 delimiter.       
              The string will be split into the array [“apple”, “banana”, “orange”]
               Each of these substrings will be printed in the new line:
                    apple 
                    banana 
                   orange
               */

                case 11:
                    System.out.println("First string after trimming: [" + str1.trim() + "]");
                    System.out.println("Second string after trimming: [" + str2.trim() + "]");
                    break; 
    
                 //The trim() method only removes spaces or other whitespace characters (like tabs or newlines) from the beginning and end of the string, not from the middle.

                case 12:
                    System.out.println("Is the first string empty? " + str1.isEmpty());
                    System.out.println("Is the second string empty? " + str2.isEmpty());
                    break; 

                case 13:
                    System.out.println("Character array of first string:");
                    for (char c : str1.toCharArray()) {
                        System.out.print(c + " ");
                    }
                    System.out.println();

System.out.println("Character array of second string:");
                    for (char c : str2.toCharArray()) {
                        System.out.print(c + " ");
                    }
                    System.out.println();
                    break;

                case 14:
                    System.out.println("Exiting...");
                    break; 

                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        } while (choice != 14);

        scanner.close();
    }
}

OUTPUT:

Enter the first string: ajithaa sri 
Enter the second string: aj maayon

Choose a string operation:
1. Find Length
2. Convert to Uppercase
3. Convert to Lowercase
4. Reverse the String
5. Concatenate Strings
6. Compare Strings
7. Check if Substring Exists
8. Replace a Character
9. Find Character at Index
10. Split the String
11. Trim Whitespaces
12. Check if String is Empty
13. Convert to Character Array
14. Exit

Enter your choice: 1
Length of first string: 12
Length of second string: 9

Enter your choice: 2
First string in Uppercase: AJITHAA SRI 
Second string in Uppercase: AJ MAAYON

Enter your choice: 3
First string in Lowercase: ajithaa sri 
Second string in Lowercase: aj maayon

Enter your choice: 4
Reversed first string:  irs aahtija
Reversed second string: noyaam ja

Enter your choice: 5
Concatenated string: ajithaa sri aj maayon

Enter your choice: 6
First string is lexicographically greater.

Enter your choice: 7
Enter a substring to check in the first string: aji
Substring exists in the first string: true

Enter your choice: 8
Enter the character to replace: a
Enter the new character: u
First string after replacement: ujithuu sri 
Second string after replacement: uj muuyon

Enter your choice: 9
Enter the index to find the character(0-based): 4
Character at index:4 in first string: h
Character at index 4 in second string: a

Enter your choice: 10
Enter the delimiter to split the first string:  
First string split into parts:
ajithaa
sri
Second string split into parts:
aj
maayon

Enter your choice: 11
First string after trimming: [ajithaa sri]
Second string after trimming: [aj maayon]

Enter your choice: 12
Is the first string empty? false
Is the second string empty? false

Enter your choice: 13
Character array of first string:
a j i t h a a   s r i   
Character array of second string:
a j   m a a y o n 

Enter your choice: 14
Exiting...
