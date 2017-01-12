# Functies

Een functie is een stuk herbruikbare code. Een functie kan uitvoer hebben en
soms verschilt de functionaliteit afhankelijk van de invoer.
Het heeft veel voordelen om functies te gebruiken.  Wanneer je bijvoorbeeld de
code hebt gemaakt om data mooi te plotten wil je niet telkens opnieuw de hele
code moeten kopiëren en plakken als je nieuwe data hebt. Ook bevordert het
gebruik van functies de leesbaarheid van je code. Met goed gekozen namen voor
functies kan je snel een overzicht van wat de code doet en wat waar staat door
alleen even snel de functienamen te lezen.

Hint: mocht je jezelf betrappen op code kopiëren en plakken, probeer dan een
manier te verzinnen hoe je de code die je wilt kopiëren kan hergebruiken] Ga dan
ofwel een loop gebruiken, ofwel een functie gebruiken.

Wat zijn functies dan? Je hebt al functies gebruikt! `len` is een functie. Net
zoals `arange`, `plot` enzovoort. In dit geval heeft iemand van Python of numpy
deze functie gemaakt.

Functies zijn dus een belangrijk aspect van leren programmeren. Het begin van
een functie wordt aangegeven met `def`, daarna komt de functienaam (die je zelf
mag kiezen), en vervolgens komen de haakjes met daartussen mogelijke parameters.

Voorbeeld:

    def print_test():
        print "abcdef"

Een hele simpele testfunctie die de string `abcdef` naar je stdout (je
console/terminal/shell) print. Als je dit in je bestand zet weet Python dat er
nu een functie is met de naam `print_test`. Python heeft dit nog niet
uitgevoerd. Dit moet je zelf nog doen door het expliciet aan te roepen. Dit doe
je zo:

    print_test()

Nu gaan we deze uitbreiden! In plaats van dat het altijd `abcdef` print willen
we iets meegeven wat geprint wordt.

    def print_test_2(parameter_1):
        print parameter_1

We kunnen het op verschillende manieren aanroepen:

    print_test_2("hijkl")

of (dit heeft hetzelfde resultaat):

    variabele_1 = "hijkl"
    print_test_2(variabele_1)

Nu weet je hoe je een functie kan maken die afhankelijk van de invoer iets
anders doet. Wat een functie ook nog kan is iets uitrekenen en dat vervolgens
teruggeven zodat je er verder mee kan werken in de rest van je programma. Dit
doe je met het woord `return`. Achter return zet je de variabele die je wilt
teruggeven als de functie aangeroepen wordt.

Bekijk de volgende functie die twee argumenten nodig heeft. De functie telt
deze waardes op returned vervolgens het resultaat.

    def add(a, b):
        c = a + b
        return c

Hier moeten dus twee waardes in! En er wordt iets teruggegeven waar we mee
door kunnen rekenen.  Dus om dit gebruiken moeten we de functie aanroepen en het
resultaat in een variabele opslaan.

    sum = add(13, 37)

Of zo:

    a = 10
    c = 23
    result = add(a, c)

Let op! De `c` in de bovenstaande code is een andere `c` dan die in de functie!
Ze hebben niks te maken met elkaar, ze heten alleen toevallig hetzelfde. Als je
een variabele aanmaakt in een functie bestaat die alleen in de functie zelf.