namespace MeuApp
{}  

    internal class Program
    {
        static void Main(string[] args)
        {
            char vezesDividirMaisMenos, igual;
            decimal x, y, resultado;

            Console.WriteLine("CALCULADORA:");

            string[] vet = Console.ReadLine().Split(' ');
            x = decimal.Parse(vet[0]);
            vezesDividirMaisMenos = char.Parse(vet[1]);
            y = decimal.Parse(vet[2]);
            igual = char.Parse(vet[3]);
            resultado = 0;

            if (vezesDividirMaisMenos == '+')
            {
                resultado = x + y;
                Console.WriteLine("-----------------------------------------------------------");
                Console.WriteLine(resultado);
            }
            else if (vezesDividirMaisMenos == '-')
            {
                resultado = x - y;
                Console.WriteLine("-----------------------------------------------------------");
                Console.WriteLine(resultado);
            }
            else if (vezesDividirMaisMenos == 'x')
            {
                resultado = x * y;
                Console.WriteLine("-----------------------------------------------------------");
                Console.WriteLine(resultado);
            }
            else if (vezesDividirMaisMenos == '/')
            {
                resultado = x / y;
                Console.WriteLine("-----------------------------------------------------------");
                Console.WriteLine(resultado);
            }
             else if (vezesDividirMaisMenos == '^')
            {
                resultado = (decimal)Math.Pow((double)x, (double)y);
                Console.WriteLine("-----------------------------------------------------------");
                Console.WriteLine(resultado);
            }
             else if (vezesDividirMaisMenos == '%')
            {
                resultado = x * y / 100;
                Console.WriteLine("-----------------------------------------------------------");
                Console.WriteLine(resultado);
            }
            else
            {
                Console.WriteLine("-----------------------------------------------------------");
                Console.WriteLine("ERRO");
            }

        while (igual == '=')
        {
            string[] vet2 = Console.ReadLine().Split(' ');
            vezesDividirMaisMenos = char.Parse(vet2[0]);
            x = decimal.Parse(vet2[1]);
            igual = char.Parse(vet2[2]);

            switch (vezesDividirMaisMenos)
            {
                case '+':
                    resultado += x;
                    Console.WriteLine("-----------------------------------------------------------");
                    Console.WriteLine(resultado);
                    break;
                case '-':
                    resultado -= x;
                    Console.WriteLine("-----------------------------------------------------------");
                    Console.WriteLine(resultado);
                    break;
                case 'x':
                    resultado *= x;
                    Console.WriteLine("-----------------------------------------------------------");
                    Console.WriteLine(resultado);
                    break;
                case '/':
                    resultado /= x;
                    Console.WriteLine("-----------------------------------------------------------");
                    Console.WriteLine(resultado);
                    break;
                case '^':
                    resultado = (decimal)Math.Pow((double)resultado, (double)x);
                    Console.WriteLine("-----------------------------------------------------------");
                    Console.WriteLine(resultado);
                    break;
                case '%':
                    resultado = resultado * x / 100;
                    Console.WriteLine("-----------------------------------------------------------");
                    Console.WriteLine(resultado);
                    break;
                default:
                    Console.WriteLine("-----------------------------------------------------------");
                    Console.WriteLine("ERRO");
                    break;
            }
        }
    }
}
