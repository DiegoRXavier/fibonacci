# fibonacci
C#- Fibonacci. Indicando 0, o programa para. usando While, for, if e Else
namespace Course
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = 1;
            while (n != 0)
            {
                Console.Write("Digite o número : ");
                n = int.Parse(Console.ReadLine());

                if (n != 0)
                {
                    string fibonacci = SequenciaFibonacci(n);
                    Console.WriteLine(fibonacci);
                }
                else
                {
                    Console.WriteLine("Número inválido. Encerrando o programa.");
                }
            }
        }
            static string SequenciaFibonacci(int n)
            {
                if (n == 1)
                    return "1";

                int n1 = 1;
                int n2 = 1;
                string sequencia = n1 + ", " + n2;

                for (int i = 2; i < n; i++)
                {
                    int n3 = n1 + n2;
                    sequencia = sequencia + ", " + n3;
                    n1 = n2;
                    n2 = n3;
                }

                return sequencia;
            }
        }
    }

