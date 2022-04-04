# Lesson9_methods_and_recursion
//Quadratic equation solver
using System;

namespace Quadraticfunction
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            Console.Write("a = ");
            int a = int.Parse(Console.ReadLine());
            Console.Write("b = ");
            int b = int.Parse(Console.ReadLine());
            Console.Write("c = ");
            int c = int.Parse(Console.ReadLine());
            Console.WriteLine(Quadraticfunction1(a, b, c));
            Console.WriteLine(Quadraticfunction2(a, b, c));

        }

        static double Quadraticfunction1(int a, int b, int c)
        {
            if ((b * b - 4 * a * c) >= 0)
            {
                double result1 = (b + (Math.Pow((b * b - 4 * a * c),(1/2))) / (2 * a));
                double result2 = (b - (Math.Pow((b * b - 4 * a * c), (1 / 2))) / (2 * a));
                return result1;
            }
            
            else 
            {
                return 0;
            }
            
        }

        static double Quadraticfunction2(int a, int b, int c)
        {

            if ((b * b - 4 * a * c) >= 0)
            {
                double result1 = (b + (Math.Pow((b * b - 4 * a * c),(1/2)) )/ (2 * a));
                double result2 = (b - (Math.Pow((b * b - 4 * a * c), (1 / 2))) / (2 * a));
                return result2;
            }

            else 
            {
                return 0;
            }
            
        }
    }

}

//Factorial of a number
using System;

namespace Factorial
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            Console.Write("Enter the number= ");
            int number = int.Parse(Console.ReadLine());
            
            Console.WriteLine(Factorial(number));
        }
        static int Factorial(int number)
        {
            int multiplier = 1;
            while (true)
            {
                
                if (number <= 1)
                {
                    break;
                }
                multiplier *= number;
                number--;
            }
            return multiplier;
        }
    }
}

//Numbertowords
using System;

namespace numbertowords
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            Console.Write("Please enter your number= ");
            int number = int.Parse(Console.ReadLine());
            Console.WriteLine(Numbertowords(number));


        }

        static string Numbertowords(int number)
        {
            if (number == 0)
                return "zero";

            string words = "";

            
            if ((number / 100) > 0)
            {
                words += Numbertowords(number / 100) + " hundred ";
                number %= 100;
            }

            if (number > 0)
            {
                if (words != "")
                    words += "and ";

                var unitsMap = new[] { "zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine", "ten", "eleven", "twelve", "thirteen", "fourteen", "fifteen", "sixteen", "seventeen", "eighteen", "nineteen" };
                var tensMap = new[] { "zero", "ten", "twenty", "thirty", "forty", "fifty", "sixty", "seventy", "eighty", "ninety" };

                if (number < 20)
                    words += unitsMap[number];
                else
                {
                    words += tensMap[number / 10];
                    if ((number % 10) > 0)
                        words += "-" + unitsMap[number % 10];
                }
            }
            return words;
    
        }
}   }

//Stringcounter
using System;

namespace Stringcounter
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            Console.Write("Please enter your name= ");
            string name = Console.ReadLine();
            Console.WriteLine(Stringcounter(name));
        }
        static int Stringcounter(string name)
        {
            int k = name.Length;
            return k;
            
        }
    }
}


//Exercises on Recursion
//Sum of arithmetic series
using System;

namespace Lesson_9_Methods
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            Console.Write("number= ");
            int number = int.Parse(Console.ReadLine());
            double sum = SumOfValues(number);
            Console.WriteLine(sum);
        }

        static double SumOfValues(int number)
        {


            if (number==0)
            {
                return 0;
            }       
                
            else
            {
                
                return number + SumOfValues(number - 1);
            }

        } 
    }
}

//Recursive stringcounter
using System;

namespace RecursiveStringCounter
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            Console.WriteLine("Hello World!");
            Console.Write("Please enter your name= ");
            string name = Console.ReadLine();
            int number = name.Length;
            Console.WriteLine(Stringcounter(number));
        }

        static int Stringcounter(int number)
        {

            if (number == 0)
            {
                return 0;
            }

            else
            {

                return 1 + Stringcounter(number - 1);
            }

        }
    }
}

//Printing prime numbers
using System;

namespace printing_prime_using_recursion
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            Console.WriteLine("Hello World!");
            Console.Write("Range for prime number= ");
            int rule = int.Parse(Console.ReadLine());
            Printprime(rule);
        }
        static void Printprime(int rule)
        {
            int i = 1;
            while (i <= rule)
            {
                Console.WriteLine(i);
                i += 2;
                
                

            }
        }
    }

}

//Printing random numbers
using System;

namespace Randomnumbers
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
            Console.Write("Please enter the range= ");
            int range = int.Parse(Console.ReadLine());
            Randomly(range);
     
        }
        static void Randomly(int range)
        {
            int[] test = new int[range];
            Random array = new Random();
            for (int i = 0; i < range; i++)
            {
                test[i] = array.Next(10);
                Console.WriteLine(test[i]);
                for (int j = 0; j < range; j++)
                {
                    if (test[i] == test[i + j])
                    {
                        break;
                    }
                }
                
                
                
            }
        }

    }
}

