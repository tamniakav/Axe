# Axe
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Axe
{
    class Axe
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int lastPart = (2 * n) - 2;

            for (int i = 0; i < n; i++)
            {
                Console.WriteLine("{0}*{1}*{2}", new string('-', n * 3), new string('-', i), new string('-',lastPart));
                lastPart--;
            }
            lastPart++;
            for (int i = 0; i < n / 2; i++)
            {
                Console.WriteLine("{0}*{1}*{1}", new string('*', n * 3), new string('-', lastPart));
            }
            int firstPart = 3 * n;
            int middlePart = lastPart;
            for (int i = 0; i < (n / 2) - 1; i++)
            {
                Console.WriteLine("{0}*{1}*{2}", new string('-', firstPart), new string('-', middlePart), new string('-', lastPart));
                firstPart--;
                lastPart--;
                middlePart += 2;
            }
            Console.WriteLine("{0}{1}{2}", new string('-', firstPart), new string('*',(5 * n) - (firstPart + lastPart)), new string('-', lastPart));
        }
    }
}
