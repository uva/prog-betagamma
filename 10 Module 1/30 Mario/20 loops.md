# For-loops

Een computer kan één ding heel goed, en dat is herhalend werk. Om in Python iets meerdere keren te doen, kan je met copy-paste aan de slag, maar dit wordt al snel onbehapbaar. Om bijvoorbeeld iets 10x, 10,000x, of misschien 1,000,000x uit te voeren, kan je de `for`-loop gebruiken. Dit ziet er als volgt uit:


	for i in range(8):
	    print i


Een `for`-loop is een herhalende (looping) constructie, die een stukje code een aantal keer uitvoert. Zou je de code hierboven runnen, dan krijg je de getallen 0 **tot** 8 op je scherm. `for i in range(8):` laat Python alle code binnen de for-loop, in dit geval `print i`, 8 keer uitvoeren. Ook koppelt Python elke ronde (iteratie) een nieuwe waarde aan `i`, beginnend met 0 en eindigend met 7. Bij deze welkom in de informatica, hier tellen we vanaf 0.

Het is belangrijk om op te merken dat de naam `i` maar een naam is, dit mag je ook iets anders noemen. Het is echter conventie om `i` te gebruiken mocht je geen betere naam kunnen verzinnen.


# While-loops

Soms weet je van te voren niet hoe vaak je iets wilt doen. Stel je voor dat we willen berekenen hoe vaak we het getal 1024 door 2 kunnen delen. Met een `for`-loop wordt zo'n taak lastig. Om deze reden heeft Python een `while`-loop. Zie onderstaande code:


	n = 1024
	counter = 0

	while n >= 2:
	    n /= 2
	    counter += 1

	print counter


Een `while`-loop is eigenlijk een herhalende `if`-statement. Evalueert `n >= 2` naar `True` dan wordt de code uitgevoerd. Enkel wordt na het uitvoeren van de code weer teruggesprongen naar `n >= 2`, en wordt er weer gekeken of `n` groter of gelijk is aan `2`. Zodra `n >= 2` evalueert naar `False`, dan stopt de `while`-loop en gaat Python verder met de eerst volgende regel en dat is `print counter`.

Deze `while`-loop gaat net zolang door totdat `n >= 2` niet meer naar `True` evalueert. Dit betekent dat als je de regel `n /= 2` weghaalt je een zogenaamde *infinite loop* krijgt. Een loop die zonder handmatig ingrijpen niet stopt. Let daarom als je `while`-loops gebruikt goed op dat deze ook ooit stopt.