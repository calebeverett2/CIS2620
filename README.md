using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using static System.Console;

namespace GreenvilleRevenue
{
    class Program
    {
        static void Main(string[] args)
        {
            string number;
            double entranceFee;
            string lastYear, currentYear;
            const double ENTRANCE_FEE = 25;
            bool whichYearHadMore;
            int last, current, total;
            Write("Enter your name >> ");
            number = ReadLine();
            Write("Enter the number of contestants in last years contest >> ", number);
            lastYear = ReadLine();
            last = Convert.ToInt32(lastYear);
            Write("Enter the number of contestants from this years contest >> ");
            currentYear = ReadLine();
            current = Convert.ToInt32(currentYear);
            total = last + current;
            entranceFee = ENTRANCE_FEE * total;
            whichYearHadMore = string.Equals(currentYear, lastYear);
            WriteLine("The total of last year and this year is {2}", last, current, total);
            WriteLine("The entrance fee is {1}", total, entranceFee);
            WriteLine("It is {0} that this year had more than last year",
                whichYearHadMore, lastYear, currentYear);
        }
    }
}
