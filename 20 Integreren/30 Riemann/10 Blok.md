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

## Hints

Zorg dat je deze vervolgens test voor de volgende functies:

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

* In Python kun je functies meegeven als argument aan andere functies. Zo kun je de functie `functie1` die hierboven gedefineerd staat meegeven aan `riemann()` door simpelweg `rieman(functie1, 0, 1, 10000)` aan te roepen.

- Zoals je ziet het je 'alleen' de waarde van de functie nodig op de $$N+1$$ hoekpunten van de intervallen. Zorg dat je het aantal intervallen $$(N)$$ in je programma vrij kan veranderen en bepaal aan de hand daarvan de hoekpunten $$x_i$$ en de waarde van de grafiek op elk van die hoekpunten $$f(x_i)$$. Bereken aan het eind van het programma de integraal en print het op het scherm.

- Let op: als je het interval in $$N$$ stukjes verdeeld zijn er $$N+1$$ hoekpunten.

- Maak een plaatje van je grafiek zodat je duidelijk ziet welk gebied je aan het integreren bent.

- Test je programma op een (vergelijkbare) integraal die je wel analytisch kan uitrekenen.


## Testen

	checkpy riemann
