Her er et eksempel på koden:

```csharp

using System;

class Program
{
    static int GenerateRandomNumber()
    {
        Random random = new Random();
        return random.Next(1, 101);
    }

    static void Main()
    {
        int randomNumber = GenerateRandomNumber();
        int guess = -1;  // Initialiser guess med en standardverdi
        int attempts = 0;
        bool validGuess;

        Console.WriteLine("Velkommen til gjettespillet!");

        do
        {
            Console.Write("Gjett et tall mellom 1 og 100: ");
            string input = Console.ReadLine();
            validGuess = true;

            if (string.IsNullOrEmpty(input))
            {
                Console.WriteLine("Ugyldig inndata. Prøv igjen.");
                validGuess = false;
            }
            else if (!int.TryParse(input, out guess))
            {
                Console.WriteLine("Ugyldig inndata. Prøv igjen.");
                validGuess = false;
            }

            if (validGuess)
            {
                attempts++;

                if (guess < randomNumber)
                {
                    Console.WriteLine("Tallet er for lavt. Prøv igjen.");
                }
                else if (guess > randomNumber)
                {
                    Console.WriteLine("Tallet er for høyt. Prøv igjen.");
                }
                else
                {
                    Console.WriteLine("Gratulerer! Du gjettet riktig på {0} forsøk.", attempts);
                }
            }
        } while (guess != randomNumber || !validGuess);

        Console.WriteLine("Takk for at du spilte!");
    }
}
```
Denne koden implementerer et enkelt tekstbasert gjettespill der spilleren får gjette et tall mellom 1 og 100. Programmet genererer et tilfeldig tall, og deretter blir spillerens gjett sammenlignet med dette tallet. Spilleren får tilbakemelding om gjettet tall er for høyt eller for lavt, og når spilleren gjettet riktig, blir antall forsøk gratulert.

Det vil komme opp en advarsel med denne koden, om du ønsker å videreutvikle koden kan du forsøke å få fjernet dette varselet:

`warning CS8600: Converting null literal or possible null value to non-nullable type.`