# Basic-Java-programs
/*1.Create a calculator program. The user must enter two numbers and select one arithmetic operation:
Addition, Subtraction, Multiplication, or Division.*/
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double a = sc.nextDouble();
        double b = sc.nextDouble();
        int choice = sc.nextInt();

        switch (choice) {
            case 1:
                System.out.println("Result: " + (a + b));
                break;

            case 2:
                System.out.println("Result: " + (a - b));
                break;

            case 3:
                System.out.println("Result: " + (a * b));
                break;

            case 4:
                if (b != 0)
                    System.out.println("Result: " + (a / b));
                else
                    System.out.println("Invalid division");
                break;

            default:
                System.out.println("Invalid choice");
        }
    }
}

/*2.Create a program that asks the user to enter a number from 1 to 7. Display the corresponding day of the
week.*/
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int day = sc.nextInt();

        switch (day) {
            case 1:
                System.out.println("Day: Monday");
                break;
            case 2:
                System.out.println("Day: Tuesday");
                break;
            case 3:
                System.out.println("Day: Wednesday");
                break;
            case 4:
                System.out.println("Day: Thursday");
                break;
            case 5:
                System.out.println("Day: Friday");
                break;
            case 6:
                System.out.println("Day: Saturday");
                break;
            case 7:
                System.out.println("Day: Sunday");
                break;
            default:
                System.out.println("Invalid input");
        }
    }
}

//3.Create a program that asks the user to enter a number from 1 to 5. Display the number as a word.
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        switch (n) {
            case 1:
                System.out.println("Word: One");
                break;
            case 2:
                System.out.println("Word: Two");
                break;
            case 3:
                System.out.println("Word: Three");
                break;
            case 4:
                System.out.println("Word: Four");
                break;
            case 5:
                System.out.println("Word: Five");
                break;
            default:
                System.out.println("Invalid input");
        }
    }
}

/*4.Create a program that asks the user to enter marks. Based on the marks, display the student result
category using these ranges: below 35 = Fail; 35 to 59 = Pass; 60 to 69 = Second Class; 70 to 89 = First
Class; 90 and above = highest grade/category.*/


import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int marks = sc.nextInt();

        if (marks < 0 || marks > 100) {
            System.out.println("Invalid marks");
        } else if (marks < 35) {
            System.out.println("Result: Fail");
        } else if (marks <= 59) {
            System.out.println("Result: Pass");
        } else if (marks <= 69) {
            System.out.println("Result: Second Class");
        } else if (marks <= 89) {
            System.out.println("Result: First Class");
        } else {
            System.out.println("Result: Highest Grade");
        }
    }
}

/*5.Create a simple ATM program. Display a menu with: 1. Deposit, 2. Withdrawal, 3. Balance Check. Ask
the user to select one option and perform the corresponding operation.*/

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        double balance = sc.nextDouble();
        int choice = sc.nextInt();

        if (choice == 1) {
            double deposit = sc.nextDouble();
            balance = balance + deposit;
            System.out.println("Updated balance: " + balance);
        }
        else if (choice == 2) {
            double withdrawal = sc.nextDouble();

            if (withdrawal <= balance) {
                balance = balance - withdrawal;
                System.out.println("Updated balance: " + balance);
            } else {
                System.out.println("Insufficient balance");
            }
        }
        else if (choice == 3) {
            System.out.println("Current balance: " + balance);
        }
        else {
            System.out.println("Invalid choice");
        }
    }
}
