# Functies

## Gemiddelde

Het volgende stukje code berekent van twee verschillende lijsten het gemiddelde:  

	# maak twee lijsten
	lijst_1 = [0.5, 0.2, 0.3, 1.2, 0.4, 1.1]
    lijst_2 = [0.8, 0.1, 0.4, 1.3, 0.6, 1.9]

	# bereken en print het gemiddelde van lijst 1
    som = 0
    for element in lijst_1:
        som += element
    gemiddelde_1 = som / len(lijst_1)
    print('gemiddelde van lijst 1: {:.2f}'.format(gemiddelde_1))

	# bereken en print het gemiddelde van lijst 2
    som = 0
    for element in lijst_2:
        som += element
    gemiddelde_2 = som / len(lijst_2)
    print('gemiddelde van lijst 2: {:.2f}'.format(gemiddelde_2))

Deze code werkt, maar het kan een stuk eleganter! Zoals je ziet bevat deze code flink wat herhaling. De maker van dit programma heeft het stuk code om het gemiddelde mee te bereken gedupliceerd. Dit kunnen we vermijden door een functie te defnieren voor het berekenen van het gemiddelde.

### Specificatie

* Noem je programma gemiddelde.py
* Copieer de bovenstaande code in het programma.
* Definieer bovenaan het programma een functie `gemiddelde(l)`. De input van de functie is een lijst van getallen. De output is het gemiddelde waarde van deze lijst. Let er op, het is **niet** de bedoeling dat dat de functie `gemiddelde` een `print`-statement bevat!
* Herschrijf de rest van de code nu zo dat je de functie gemiddelde gebruikt in plaatst van de bestaande loops. Als je dit goed doet, zou de code eens stuk eenvoudiger moeten zijn, en een stuk minder herhaling van code moeten bevatten.
