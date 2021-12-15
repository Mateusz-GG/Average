# Average

"" This program is selecting the lowest , posivite numbers and counting Average , open Console and type numbers , remember to separate them by SPACE.""



{
    class Program
    {
        static void Main(string[] args)
        {
            int possitive = 0, temp;
            double average = 0;
            Console.WriteLine("Podaj liczby (podziel je spacją) ");
            string[] input = Console.ReadLine().Split(' ');
            int elements = input.Length;

            int[] numbers = new int[elements];
            
            for (int i = 0; i < elements; i++) 
            {
                numbers[i] = Convert.ToInt32(input[i]);
                if ((numbers[i] > 0) possitive++);
                average += numbers[i];
            }
            average = average / elements;

            for (int i = 0; i < elements - 1; i++)
            {
                for (int j = 0; j < elements - 1; j++)
                {
                    if (numbers[j] > numbers[j + 1])
                    {
                        temp = numbers[j + 1];
                        numbers[j + 1] = numbers[j];
                        numbers[j] = temp;
                    }
                }
            }

            Console.WriteLine("Najmniejsza ={0}", numbers[0]);
            Console.WriteLine("Liczby dodatnie ={0}", possitive);
            Console.WriteLine("Średnia ={0}", average);
        }
    }
}
