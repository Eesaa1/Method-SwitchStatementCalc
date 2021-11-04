using System;

namespace Functions_and_procedures
{
    class Program
    {
        static void Main(string[] args)
        {
            string temp1 = "a";
            int temp = -1;
            int a = 1;
            do
            {

                Menu();
                   
                   temp1 = Console.ReadLine();
                try { 
                    temp = Convert.ToInt32(temp1);
                    if (temp < 0 || temp > 4) { 
                        Console.WriteLine("");
                        Console.WriteLine("Error with data input");
                        Console.WriteLine("");
                    }
                    else { 
                    switch (temp)
                    {

                        case 1:
                            Add();
                            Console.WriteLine("");
                            break;

                        case 2:
                            Sub();
                            Console.WriteLine("");
                            break;
                        case 3:
                            Mult();
                            Console.WriteLine("");
                            break;
                        case 4:
                            Div();
                            Console.WriteLine("");
                            break;
                        case 0:
                            Exit();
                            Console.WriteLine("");
                            break;

                            Console.ReadKey();

                    }
                    }
                }
                catch
                {
                    Console.WriteLine("");
                    Console.WriteLine("Error with data input try agian.");
                    Console.WriteLine("");
                }




                static void Menu()
                {

                    Console.WriteLine("1. Add two numbers");
                    Console.WriteLine("2. Subtract one number from another");
                    Console.WriteLine("3. Multiply two numbers");
                    Console.WriteLine("4. Divide one number by another number");
                    Console.WriteLine("0. Exit Program");
                    Console.WriteLine("");
                }

                static void Add()
                {

                    Console.WriteLine("");
                    Console.Write("Enter one number that you want to add: ");
                    int Add1 = Convert.ToInt32(Console.ReadLine());
                    Console.Write("Enter one number that you want to add: ");
                    int Add2 = Convert.ToInt32(Console.ReadLine());
                    int Add3 = Add2 + Add1;
                    Console.WriteLine("");
                    Console.WriteLine("{0} + {1} = {2}", Add1, Add2, Add3);
                }
                static void Sub()
                {
                    Console.WriteLine("");
                    Console.Write("Enter one number that you want to subtract from: ");
                    int Sub1 = Convert.ToInt32(Console.ReadLine());
                    Console.Write("Enter one number that you want to subtract: ");
                    int Sub2 = Convert.ToInt32(Console.ReadLine());
                    int Sub3 = Sub1 - Sub2;
                    Console.WriteLine("");
                    Console.WriteLine("{0} - {1} = {2}", Sub1, Sub2, Sub3);
                }
                static void Mult()
                {
                    Console.WriteLine("");
                    Console.Write("Enter one number that you want to multiply: ");
                    int Mult1 = Convert.ToInt32(Console.ReadLine());
                    Console.Write("Enter one number that you want to multiply: ");
                    int Mult2 = Convert.ToInt32(Console.ReadLine());
                    int Mult3 = Mult1 * Mult2;
                    Console.WriteLine("");
                    Console.WriteLine("{0} * {1} = {2}", Mult1, Mult2, Mult3);
                }
                static void Div()
                {
                    Console.WriteLine("");
                    Console.Write("Enter one number that you want to divide: ");
                    int Div1 = Convert.ToInt32(Console.ReadLine());
                    Console.Write("Enter one number that you want to divide by: ");
                    int Div2 = Convert.ToInt32(Console.ReadLine());
                    int Div3 = Div1 / Div2;
                    Console.WriteLine("");
                    Console.WriteLine("{0} / {1} = {2}", Div1, Div2, Div3);
                }
                static void Exit()
                {
                    System.Environment.Exit(1);
                }


            }
            while (a == 1);
            Console.ReadKey();
        }
    }
}


