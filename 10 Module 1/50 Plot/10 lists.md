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