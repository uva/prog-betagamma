# Lijsten

Behalve enkele waardes zoals integers en booleans, kent Python ook verzamelingen. Door middel van verzamelingen kun je data groeperen, en hier ook operaties op doen. Eén zo'n verzameling is een `list`. Dit ziet er als volgt uit:


    docenten = ["Martijn", "Jelle", "Anne", "Maarten", "Aniek", "Dominique", "Marleen"]


In het bovenstaande stukje code wordt een list aangemaakt met een zevental strings erin. De blokhaken staan hier voor een list, en de elementen van de list staan tussen de blokhaken gescheiden door komma's. Een list is een geordende muteerbare verzameling: je kan er elementen aan toevoegen, uit verwijderen en vervangen. Kijk eens naar het volgende stukje code:


	docenten.append("Piet")
	docenten.append("Wouter")
	print "De eerste docent is:", docenten[0]
	print "De laatste docent is:", docenten[-1]
	del docenten[-2]
	docenten[2] = "Marianne"
    print "Er zijn", len(docenten), "docenten en dit zijn:", docenten


Om een element aan een list toe te voegen kunnen we de `append` methode gebruiken zoals op de regel: `docenten.append("Piet")`. Hier wordt de string `"Piet"` toegevoegd aan de list van docenten. 

Om een element uit de list te halen moeten we weer gebruik maken van de blokhaken. Echter dit keer gebruiken we ze voor het aangeven van de index in de list, zoals op de regel: `print "De eerste docent is:", docenten[0]`. Oftewel, `docenten[0]` betekent geef mij het nulste (eerste) element uit de list `docenten`. Bij deze welkom in de informatica, hier tellen we vanaf 0. Voor het gemak laat Python je ook indexeren vanaf het uiteinde van de list: `-1` betekent het laatste element, `-2` het een-na-laatste, enzovoort.

Een element verwijderen uit een list gaat door middel van de `del` statement, zoals op de regel: `del docenten[6]`.

Elementen vervangen doe je net zoals met variabelen door middel van `=`. Zo wordt op de regel: `docenten[2] = "Marianne"` de string `"Anne"` vervangen door `"Marianne"`.

Werk nu voor jezelf uit hoe de list `docenten` eruit ziet na het runnen van deze code. Check daarna je antwoord door de code daadwerkelijk te runnen.


# For-loops met lijsten

Eerder hebben we gekeken naar for-loops en toen maakten we gebruik van `range`. Bijvoorbeeld in het volgende stukje code:


	for i in range(8):
	    print i


Het blijkt dat `range` een functie is die een lijst produceert. In dit geval omdat we `8` meegeven als argument, produceert `range(8)` een lijst van 0 **tot** 8. Dit betekent dat het bovenstaande stukje code gelijk is aan het volgende:


	for i in [0,1,2,3,4,5,6,7]:
	    print i


Een `for`-loop in Python is een herhalende (looping) constructie die je het beste zo kan lezen: Voor elk element `i` in verzameling `[0,1,2,3,4,5,6,7]` doe `print i`. Dit betekent dat de code die bij de for-loop hoort net zo vaak wordt uitgevoerd als er elementen in de verzameling zitten over waar de for-loop itereert. De naam `i` wordt elke iteratie gekoppeld aan de bijbehorende waarde uit de verzameling. De eerste iteratie zal `i` dus worden gekoppeld aan `0`, de tweede aan `1`, etc. Elke iteratie wordt de code die bij de for-loop hoort uitgevoerd, dat is in dit geval `print i`. Het runnen van bovenstaande code zal dus de getallen 0 tot en met 7 op je scherm produceren.

We kunnen `for`-loops goed gebruiken om iets te doen voor elk element in een lijst. Bijvoorbeeld het volgende stukje code kijkt voor alle getallen in de lijst of het getal even of oneven is, en print dit uit:


	numbers = [2, 27, 15, 5, 32]

	for number in numbers:
	    if number % 2 == 0:
	        print "Number", number, "is even!"
	    else:
	    	print "Number", number, "is odd!"
        

We kunnen ook lijsten aanpassen door middel van `for`-loops, maar dan is het handiger om gebruik te maken van de `range` functie. Zoals bijvoorbeeld in de code hieronder:


	numbers = [2, 27, 15, 5, 32]

	for i in range(len(numbers)):
	    numbers[i] = numbers[i] * 2

	print numbers


In dit stukje code maken we gebruik van een `for`-loop die over de lijst geproduceerd door `range(len(numbers))` itereert. In `range(len(numbers))` wordt eerst de lengte van `numbers` berekend door middel van de functie `len`, en vervolgens maakt `range` een lijst aan afhankelijk van de uitkomst. Dit betekent dus dat in ons voorbeeld de lijst `[0,1,2,3,4]` wordt aangemaakt, want `numbers` kent een lengte van 5. Binnen de `for`-loop kunnen we dan gebruik maken van de waarde van `i`. `i` is namelijk de eerste iteratie `0`, daarmee het geeft de eerste plek aan in de lijst `numbers`. De tweede iteratie neemt `i` de waarde `1` aan, ofwel de tweede plek in `numbers, enzovoort. Door middel van een `for`-loop als hierboven loopen we niet over de lijst `numbers` zelf heen, maar over de plekken (indices) in `numbers`. Doordat je toegang hebt tot de plek, kan je ook de waarde op die plek binnen `numbers` veranderen zoals op de regel `numbers[i] = numbers[i] * 2`. Het resultaat is dat we alle getallen in `numbers` vermenigvuldigen met 2.