# Delegates



using System;

namespace delegates
{
    public delegate void Calculation(int a, int b);
    
    class Program
    {
        public static void Maths(int a, int b)
        {
            int sum = a + b;
            Console.WriteLine(sum);
        }
        static void Main(string[] args)
        {
            Calculation obj = new Calculation(Maths);
            obj.Invoke(20, 10);

        }
    }
}
