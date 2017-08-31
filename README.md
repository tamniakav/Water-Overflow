# Water-Overflow
Just another repository
using System;

namespace _3.Water_Overflow
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int capacity = 0;
            int totalLiters = 0;

            for (int i = 1; i <= n; i++)
            {
                int number = int.Parse(Console.ReadLine());

                capacity += number;

                if (capacity > 255)
                {
                    capacity -= number;
                    Console.WriteLine("Insufficient capacity!");
                }

                totalLiters = capacity;
            }

            Console.WriteLine(totalLiters);
        }
    }
}
