# Monte Carlo

Schrijf een functie die middels de Monte Carlo-methode de integraal berekent van een willekeurige wiskundige functie.

## Specificatie

- Maak een nieuw bestand genaamd `montecarlo.py`.

- Schrijf een functie `montecarlo()` die integralen kan berekenen met behulp van een Monte Carlo simulatie. 

- De functie `montecarlo()` moet vijf argumenten accepteren:

	- `func` een functie waarvan we de integraal gaan bepalen
	- `x1` de eerste x waarde
	- `y1` de eerste y waarde
	- `x2` de tweede x waarde
	- `y2` de tweede y waarde

- De functie `montecarlo()` moet de oppervlakte onder de grafiek teruggeven als resultaat.


## Tips

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

- Maak een plaatje van je grafiek zodat je duidelijk ziet welk gebied je aan het integreren bent.

- Maak ook een grafiek met rode en groene punten zoals in bovenstaand voorbeeld. Mocht je een fout gemaakt hebben in je logica dan zie je dat in een plaatje in 1 keer terwijl je daar anders uren naar moet zoeken in de code zelf.

- test je programma op een (vergelijkbare) integraal die je wel analytisch kan uitrekenen. 

- specifiek voor Monte Carlo: bij 'negatieve' integratieregio's de gebieden splitsen

- In 'echte' toepassingen wordt voor efficientie maximalisatie de box zo gekozen dat hij de integraal zo nauw mogelijk omsluit: grootste fractie 'goede' worpen.


## Testen

	checkpy montecarlo
