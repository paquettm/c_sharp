# Sample Exam: Basic C# Programming

## Question 1: Control Structures (10 points)

Write a C# program that asks the user to enter an integer. If the entered integer is positive, print "Positive." If it's negative, print "Negative." If it's zero, print "Zero."

```
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter an integer: ");
        if (int.TryParse(Console.ReadLine(), out int number))
        {
            if (number > 0)
            {
                Console.WriteLine("Positive");
            }
            else if (number < 0)
            {
                Console.WriteLine("Negative");
            }
            else
            {
                Console.WriteLine("Zero");
            }
        }
        else
        {
            Console.WriteLine("Invalid input. Please enter a valid integer.");
        }
    }
}
```

## Question 2: Looping (15 points)

Write a C# program that uses a for loop to print the squares of numbers from 1 to 5.

```
using System;

class Program
{
    static void Main()
    {
        for (int i = 1; i <= 5; i++)
        {
            int square = i * i;
            Console.WriteLine($"Square of {i}: {square}");
        }
    }
}
```

## Question 3: Variables and Input/Output (15 points)

Write a C# program that asks the user for their name and age, and then prints a message saying "Hello, [Name]! You are [Age] years old."

```
using System;

class Program
{
    static void Main()
    {
        Console.Write("Enter your name: ");
        string name = Console.ReadLine();

        Console.Write("Enter your age: ");
        if (int.TryParse(Console.ReadLine(), out int age))
        {
            Console.WriteLine($"Hello, {name}! You are {age} years old.");
        }
        else
        {
            Console.WriteLine("Invalid input. Please enter a valid age.");
        }
    }
}
```

## Question 4: While Loop (10 points)

Write a C# program that uses a while loop to print the numbers from 1 to 3.

```
using System;

class Program
{
    static void Main()
    {
        int count = 1;

        while (count <= 3)
        {
            Console.WriteLine(count);
            count++;
        }
    }
}
```

## Question 5

Explain what makes while and do..while control structures pre-condition or post-condition loops. What is the effect of this on the execution of the code contained in the body of the loop?

## Question 6

Explain when you would use the for loop as opposed to the while loop.

## Further questions


        // 1- In your own words, correctly define "sequential control structure":


        // 2- In your own words, correctly define "branching":


        // 3- In your own words, correctly define "looping":


        // 4- When does code repetition stop in a while True: statement?
        // a) It is impossible to stop
        // b) once the break command is called
        // c) after 3 times, always


        // 5- What is an infinite loop?


        // 6- What is a variable?


        // 7- How do we get input from a user in C#?


        // 8- In your own words, what is a collection?
 

         // 9- There are many primitive data types supported by C#. Write 2 such data types.


        // 10- What must we use to store a value in a program?


        // 11- What is the value of the arithmetic expression 3 / 2 + 2 * 1000?



        /*
        PRACTICAL PART (3 points per correct answer) /24
        ----------------------------------------------
        */

        // Task 1:
        // Assign to a variable called "theList" the list that contains "horse", "bee", and "cat". Print this list.
        Console.WriteLine("Task 1:");

        // Task 2:
        // Add "Charley" and "knees" to the list. Remove "cat" from the list. Print the list.
        Console.WriteLine("Task 2:");

        // Task 3:
        // Ask the user to input a new element. Add this new element to the list. Sort the list. Print the list.
        Console.WriteLine("Task 3:");

        // Task 4:
        // Using for, go through the list and print each element individually, but exit the loop before printing if an element contains the string "ee".
        Console.WriteLine("Task 4:");

        // Task 5:
        // Using while, print all elements, except the second element.
        Console.WriteLine("Task 5:");

        // Task 6:
        // Ask the user to input a temperature in degrees Fahrenheit for conversion to Celsius and Kelvin. Capture store this floating-point value within a variable "temperatureF". Print that the user has entered the value inside temperatureF (display this value).
        Console.WriteLine("Task 6:");

        // Task 7:
        // Calculate the Celsius temperature and store it within the temperatureC variable. The conversion is as follows: Fahrenheit - 32, multiply everything by 5/9. Print the value of the temperature in degrees Celsius, with 2 decimal place precision. If the temperature is below 0, print this fact.
        Console.WriteLine("Task 7:");

        // Task 8:
        // Calculate the Kelvin temperature and store it within the temperatureK variable. The conversion is as follows: Celsius + 273.15. Print the value of the temperature in degrees Kelvin, with 2 decimal place precision.
        Console.WriteLine("Task 8:");
    }
}
```




# SOLUTION
        /*
        Task 1:
        Assign to a variable called "theList" the list that contains "horse", "bee", and "cat". Print this list.
        */
        Console.WriteLine("Task 1:");
        List<string> theList = new List<string> { "horse", "bee", "cat" };
        Console.WriteLine(string.Join(", ", theList));

        /*
        Task 2:
        Add "Charley" and "knees" to the list. Remove "cat" from the list. Print the list.
        */
        Console.WriteLine("Task 2:");
        theList.Add("Charley");
        theList.Add("knees");
        theList.Remove("cat");
        Console.WriteLine(string.Join(", ", theList));

        /*
        Task 3:
        Ask the user to input a new element. Add this new element to the list. Sort the list. Print the list.
        */
        Console.WriteLine("Task 3:");
        Console.Write("Input a new element for the list: ");
        string newElement = Console.ReadLine();
        theList.Add(newElement);
        theList.Sort();
        Console.WriteLine(string.Join(", ", theList));

        /*
        Task 4:
        Using for, go through the list and print each element individually, but exit the loop before printing if an element contains the string "ee".
        */
        Console.WriteLine("Task 4:");
        foreach (var item in theList)
        {
            if (item.Contains("ee"))
                break;
            Console.WriteLine(item);
        }

        /*
        Task 5:
        Using while, print all elements, except the second element.
        */
        Console.WriteLine("Task 5:");
        int count = 0;
        while (count < theList.Count)
        {
            if (count != 1)
                Console.WriteLine(theList[count]);
            count++;
        }

        /*
        Task 6:
        Ask the user to input a temperature in degrees Fahrenheit for conversion to Celsius and Kelvin. Capture store this floating-point value within a variable "temperatureF". Print that the user has entered the value inside temperatureF (display this value).
        */
        Console.WriteLine("Task 6:");
        Console.Write("Please input a temperature in degrees Fahrenheit: ");
        double temperatureF = Convert.ToDouble(Console.ReadLine());
        Console.WriteLine($"You have input {temperatureF}F");

        /*
        Task 7:
        Calculate the Celsius temperature and store it within the temperatureC variable.
        The conversion is as follows: Fahrenheit - 32, multiply everything by 5/9. Print the value of the temperature in degrees Celsius, with 2 decimal place precision.
        If the temperature is below 0, print this fact.
        */
        Console.WriteLine("Task 7:");
        double temperatureC = (temperatureF - 32) * 5 / 9;
        Console.WriteLine($"This is equivalent to {temperatureC:F2}C");
        if (temperatureC < 0)
            Console.WriteLine("This temperature is less than 0C.");

        /*
        Task 8:
        Calculate the Kelvin temperature and store it within the temperatureK variable.
        The conversion is as follows: Celsius + 273.15. Print the value of the temperature in degrees Kelvin, with 2 decimal place precision.
        */
        Console.WriteLine("Task 8:");
        double temperatureK = temperatureC + 273.15;
        Console.WriteLine($"This is equivalent to {temperatureK:F2}K");
    }
}
```

