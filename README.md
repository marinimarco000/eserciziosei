namespace eserciziosei
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int[] numeri = { 2, 5, 6, 7, 8, 1, 10, 3, 4, 9 };
            Console.Write("Inserisci  valore X : ");
            int valoreX = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine($"Numeri Maggiori di {valoreX}");
            for (int i = 0; i < numeri.Length; i++)
            {
                if (numeri[i] > valoreX)
                {

                    Console.WriteLine($"[ {numeri[i]}]");
                }
            }
            Console.WriteLine($" numeri minori o uguali a {valoreX}");
            for (int i = 0; i < numeri.Length; i++)
            {
                if (numeri[i] <= valoreX)
                {

                    Console.WriteLine($"[ {numeri[i]} ]");
                }
            }
            Console.WriteLine("--------------------------------------------------------------------- metodo fatto in classe  -----------------------------------------------------------------");
            // creo v1
            int[] v1 = { 1, 5, -2, 9, 4 };
            //dichiarazione
            int x = 5, Mag = 0, Min = 0;
            //verifico quale numero è >< di x e faccio un contatore
            for (int i = 0; i < v1.Length; i++)
            {
                if (v1[i] >= x)
                {
                    Mag = Mag + 1;
                }
                else
                {
                    Min = Min + 1;
                }

            }
            // creazione  v1 e v2
            int[] v2 = new int[Min];
            int[] v3 = new int[Mag];
            int indicev2 = 0, indicev3 = 0;
            for (int i = 0; i < v1.Length; i++)
            {
                if (v1[i] < x)
                {
                    v2[indicev2] = v1[i];
                    indicev2 = indicev2 + 1;
                }
                else
                {
                    v3[indicev3] = v1[i];
                    indicev3 = indicev3 + 1;
                }
            }
            for (int i = 0; i < v2.Length; i++)
            {
                Console.Write($"[{v2[i]}]");

            }
            Console.WriteLine();
            for (int i = 0; i < v3.Length; i++)
            {
                Console.Write($"[{v3[i]}]");

            }
        }
    }
}
