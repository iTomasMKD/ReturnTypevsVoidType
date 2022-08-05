# ReturnTypevsVoidType Remove Duplicate char in string
Remove Duplicate with string return type and void type


using System;

namespace TestConsoleApp
{
    class Program
    {
        //return string
        public string RemoveDuplicate(string str)
        {
            string result = string.Empty;

            for (int i = 0; i < str.Length; i++)
            {
                if (!result.Contains(str[i]))
                {
                    result += str[i];
                }
            }

            return result;
            Console.WriteLine();
        }
        //void type
        public static void removeduplicate(string str)
        {
            string result = string.Empty;

            for (int i = 0; i < str.Length; i++)
            {
                if (!result.Contains(str[i]))
                {
                    result += str[i];
                }
            }
            Console.WriteLine(result);
        }

        static void Main(string[] args)
        {
            string y = "aabbbccc";
            //call string return method logic
            Program pr = new Program();
            var test = pr.RemoveDuplicate(y);
            Console.WriteLine(test);
            //call void return
            TestConsoleApp.Program.removeduplicate(y);
            Console.WriteLine();
        }
    }
}
