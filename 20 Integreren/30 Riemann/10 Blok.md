# Riemann

Schrijf een functie die middels de Riemannsom de integraal berekent van een willekeurige wiskundige functie.

## Specificatie

- Maak een nieuw bestand genaamd `riemann.py`.

- Schrijf een functie `riemann()` die integralen kan berekenen met behulp van de Riemannsom. 

- De functie `riemann()` moet vier argumenten accepteren:

	- `func` een functie waarvan we de integraal gaan bepalen
	- `a` het begin van het gebied
	- `b` het einde van het gebied
	- `n` hoeveel rechthoeken we gebruiken om de integraal te bepalen.

- De functie `riemann()` moet de oppervlakte onder de grafiek teruggeven als resultaat.

## Tests

Test je procedure met de volgende functies:

1. $$\int_{0}^{1}x^{x+\frac{1}{2}} ~dx$$

	Hint: test je functie door te testen of je programma de integraal $$\int_{0}^{1}x^2 dx$$ goed voorspelt

		def functie1(x):
			return x**(x + 0.5)

2. $$\int_{0.2}^{2.2} \tan(\cos(\sin(x))) ~dx$$

	Hint: test je functie door te testen of je programma de integraal $$\int_{0}^{\pi}sin(x) dx$$ goed voorspelt

		def functie2(x): 
			return math.tan(math.cos(math.sin(x)))

3. $$\int_{0}^{\pi} \sin(x^2) ~dx$$

		def functie3(x): 
			return math.sin(x**2)

Zet deze functies in je eigen programma en zorg dat je onderaan je `riemann()`-functie aanroept voor al deze voorbeelden. Dan kun je in één keer de voorbeelden controleren.

## Hints

- In Python kun je functies meegeven als argument aan andere functies. Zo kun je de functie `functie1` die hierboven gedefineerd staat meegeven aan `riemann()` door simpelweg `rieman(functie1, 0, 1, 10000)` aan te roepen.

- Let op: als je het interval in $$N$$ stukjes verdeeld zijn er $$N+1$$ hoekpunten.

- Maak een plaatje van je grafiek zodat je duidelijk ziet welk gebied je aan het integreren bent.

## Debuggen

Lijkt het niet te werken? 

- Check "op het oog" met een grafiek of de integraal überhaupt in de buurt komt van wat je mag verwachten.

- Als dat wel goed zit, kan het zijn dat het aantal stappen te klein is om tot een precies genoeg antwoord te komen. Probeer het aantal te verhogen en bekijk ook hoe dit de uitkomsten beinvloedt.


## Testen

	checkpy riemann
