# Oppgave - Gjettespill

## Beskrivelse

Lag et enkelt tekstbasert gjettespill i C#. Spillet skal generere et tilfeldig tall mellom 1 og 100, og spilleren skal gjette hvilket tall det er. Etter hvert gjetning skal spillet gi tilbakemelding om gjetningen er for høy eller for lav, og til slutt skal spillet gratulere spilleren når riktig tall er gjettet.

## Instruksjoner:

1. Lag en funksjon `GenerateRandomNumber` som genererer et tilfeldig tall mellom 1 og 100. Du kan bruke `Random`-klassen i C# for å generere tilfeldige tall.
2. Implementer en løkke der spilleren får gjette tallene. Du kan bruke en `do-while`-løkke for å la spilleren gjette minst én gang.
3. Inne i løkken kan du be spilleren om å gjette et tall ved å bruke `Console.ReadLine()`. Husk å konvertere inntastet tekst til et heltall ved hjelp av `int.Parse()`.
4. Sammenlign det gjettete tallet med det tilfeldige tallet generert av `GenerateRandomNumber`. Gi tilbakemelding til spilleren om tallet er for høyt eller for lavt. Du kan bruke `Console.WriteLine()` for å gi tilbakemelding.
5. Fortsett løkken til spilleren gjetter riktig tall. Da skal spillet gratulere spilleren og avslutte løkken.

Om du ikke har sjans til å starte, så kan du gå inn på [hjelp/Oppgave_2](hjelp/Oppgave_2-Gjettespill.md) der er et forslag på en løsning. 

## Mål
Repetere grunnleggende C#-konsepter som bruk av løkker, inndatahåndtering og betinget logikk.