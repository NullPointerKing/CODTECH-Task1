# 📱 Calculator Application

## 📋 Project Overview

This project contains a simple calculator application developed in Java during my internship at Codtech IT Solutions. The calculator can perform basic arithmetic operations such as addition, subtraction, multiplication, and division.

## 👨‍💼 Intern Details

- **Name:** Abhinav Dyan Samantara
- **Company:** Codtech IT Solutions
- **ID:** CT12DS1738
- **Domain:** Java Programming
- **Duration:** July to September 2024
- **Mentor:** Neela Santhosh Kumar

## 📜 Description

The calculator application allows users to perform the following operations:
- Addition
- Subtraction
- Division
- Multiplication

The user is prompted to choose an operation from a menu and input the required numbers. The application continues to prompt the user for operations until the user chooses to exit.

## 💻 How to Use

1. **Compile the Java code**:
   ```bash
   javac Calculator.java

2. **Run the compiled Java program**:
   ```bash
   java Calculator
3. **Follow the on-screen instructions to choose an operation and input numbers.**

4. **To exit the program, select option 0.**

## 📝 Code

**The main code for the calculator application is as follows:**

```bash
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Calculator cal = new Calculator();

        while (true) {
            System.out.println("""
                1. Addition
                2. Subtraction
                3. Division
                4. Multiplication
                0. Exit
                """);
            System.out.print("Enter your choice: ");
            int choice = sc.nextInt();

            if (choice == 0) {
                System.out.println("Exiting...");
                break;
            }

            int a = 0, b = 0;

            if (choice >= 1 && choice <= 4) {
                System.out.print("Enter 1st number: ");
                a = sc.nextInt();
                System.out.print("Enter 2nd number: ");
                b = sc.nextInt();
            }

            switch (choice) {
                case 1:
                    System.out.println("Answer: " + cal.add(a, b));
                    break;
                case 2:
                    System.out.println("Answer: " + cal.subtract(a, b));
                    break;
                case 3:
                    System.out.println("Answer: " + cal.divide(a, b));
                    break;
                case 4:
                    System.out.println("Answer: " + cal.multiply(a, b));
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
                    break;
            }
        }

        sc.close();
    }

    int add(int a, int b) {
        return a + b;
    }

    int subtract(int a, int b) {
        return a - b;
    }

    int divide(int a, int b) {
        if (b == 0) {
            System.out.println("Error: Division by zero is not allowed.");
            return 0;
        }
        return a / b;
    }

    int multiply(int a, int b) {
        return a * b;
    }
}
```

## ✨ Features

* Addition: Adds two numbers.

* Subtraction: Subtracts the second number from the first number.

* Division: Divides the first number by the second number. Handles division by zero with an error message.

* Multiplication: Multiplies two numbers.

## 👨‍🎓 Author

* Abhinav Dyan Samantara

## 📄 License
This project is for educational purposes during the internship and is not licensed for commercial use.
