using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace TriA
{
    class Program
    {
        static void Exist(double A, double B, double C)
        {
            if ((A < (B + C)) && (B < (A + C)) && (C < (B + A)))
            {
                Console.WriteLine("Треугольник OK!!!");
            }
            else
            {
                Console.WriteLine("Треугольник ERROR!!!");
            }
        }

        static public double P(double A, double B, double C)
        {
            double D = A + B + C;
            return D;
        }
        static public double S(double A, double B, double C)
        {
            double D = A + B + C;
            double p = D / 2;
            double S = Math.Sqrt(p * (p - A) * (p - B) * (p - C));
            return S;
        }
        static public double Dlina(int x1, int y1, int x2, int y2)
        {
            double AB;
            AB = Math.Sqrt(Math.Pow((x2 - x1), 2) + Math.Pow((y2 - y1), 2));
            Console.WriteLine("Длина отрезка равна:" + AB);
            return AB;
        }

        static void Main(string[] args)
        {

            int X1, Y1, X2, Y2, X3, Y3, AA, BB, CC;
            Console.Write("Введите координаты точки A: " + "\n");
            X1 = int.Parse(Console.ReadLine());
            Y1 = int.Parse(Console.ReadLine());

            
            Console.WriteLine("Введите координаты точки B: ");
            X2 = int.Parse(Console.ReadLine());
            Y2 = int.Parse(Console.ReadLine());


            Console.WriteLine("Введите координаты точки C: ");
            X3 = int.Parse(Console.ReadLine());
            Y3 = int.Parse(Console.ReadLine());
            Console.WriteLine(" X1: " + X1 + " Y1: " + Y1);
            Console.WriteLine(" X2: " + X2 + " Y2: " + Y2);
            Console.WriteLine(" X3: " + X3 + " Y3: " + Y3);

            
            Console.WriteLine("Cторона AB");
            
            double Z1 = Dlina(X1, Y1, X2, Y2);
            Console.WriteLine("Cторона BC");
            double Z2 = Dlina(X2, Y2, X3, Y3);
            Console.WriteLine("Cторона AC");
            double Z3 = Dlina(X3, Y3, X1, Y1);
            Exist(Z1, Z2, Z3);
            Console.WriteLine("Периметр треугольника равен: " + P(Z1, Z2, Z3));
            Console.WriteLine("Площадь треугольника равен: " + S(Z1, Z2, Z3));
            Console.Write("Введите cтороны: " + "\n");
            AA = int.Parse(Console.ReadLine());
            BB = int.Parse(Console.ReadLine());
            CC = int.Parse(Console.ReadLine());

            Exist(AA, BB, CC);

            Console.ReadLine();
        }
    }
}

