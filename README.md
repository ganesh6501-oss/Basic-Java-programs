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

