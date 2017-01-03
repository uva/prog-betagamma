# For-loops

Een computer kan één ding heel goed, en dat is herhalend werk. Om in Python iets meerdere keren te doen, kan je met copy-paste aan de slag, maar dit wordt al snel onbehapbaar. Om bijvoorbeeld iets 10x, 10,000x, of misschien 1,000,000x uit te voeren, kan je de `for`-loop gebruiken. Dit ziet er als volgt uit:


	for i in range(8):
	    print i


Zou je dit stukje code runnen, dan krijg je de getallen 0 tot en met 7 op je scherm. Om dit te begrijpen kijken we eerst naar de `range()` functie. Dit is een functie die een list produceert. In dit geval omdat we `8` meegeven als argument, produceert `range(8)` een list van 0 *tot* 8. Dit betekent dat het bovenstaande stukje code gelijk is aan het volgende:


	for i in [0,1,2,3,4,5,6,7]:
	    print i


Een `for`-loop in Python is een herhalende (looping) constructie die je het beste zo kan lezen: Voor elk element `i` in verzameling `[0,1,2,3,4,5,6,7]` doe `print i`. Dit betekent dat de code die bij de for-loop hoort net zo vaak wordt uitgevoerd als er elementen in de verzameling zitten over waar de for-loop itereert. De naam `i` wordt elke iteratie gekoppeld aan de bijbehorende waarde uit de verzameling. De eerste iteratie zal `i` dus worden gekoppeld aan `0`, de tweede aan `1`, etc. Elke iteratie wordt de code die bij de for-loop hoort uitgevoerd, dat is in dit geval `print i`. Het runnen van bovenstaande code zal dus de getallen 0 tot en met 7 op je scherm produceren.

Het is belangrijk om op te merken dat de naam `i` maar een naam is, dit mag je ook iets anders noemen. Het is echter conventie om `i` te gebruiken mocht je geen betere naam kunnen verzinnen.


# While-loops

