# Functies als argumenten

Het onderstaande programma genereert twee lijsten van getallen:

	import numpy as np

	def genereer1(x_min, x_max):
	    lijst = []
	    for x in np.arange(x_min, x_max, 0.1):
	        y = 2 * x + 1
	        lijst.append(y)
	    return lijst

	def genereer2(x_min, x_max):
	    lijst = []
	    for x in np.arange(x_min, x_max, 0.1):
	        y = x + 3
	        lijst.append(y)
	    return lijst

	l1 = genereer1(0, 0.5)
	l2 = genereer2(0, 0.5)

	print(l1)
	print(l2)

Output:

	[1.0, 1.2, 1.4, 1.6, 1.8]
	[3.0, 3.1, 3.2, 3.3, 3.4]

De lijst van `genereer1()` is gebaseerd op de vergelijking `y = 2 * x + 1`, de lijst van `genereer2()` is gebaseerd op de vergelijking `y = x + 3`. Zoals je ziet bevatten beide functies grotendeels dezelfde code. Alleen de vergelijking verschillen. Dat kan eleganter:

	import numpy as np

	def fun1(x):
	    return 2 * x + 1

	def fun2(x):
	    return x + 3

	def genereer(fun, x_min, x_max):
	    lijst = []
	    for x in np.arange(x_min, x_max, 0.1):
	        y = fun(x)
	        lijst.append(y)
	    return lijst

	l1 = genereer(fun1, 0, 0.5)
	l2 = genereer(fun2, 0, 0.5)

	print(l1)
	print(l2)

Het bovenstaande programma werkt exact hetzelfde als het programma ervoor, maar maakt gebruik van een truc. De functie `genereer()` bevat als eerste argument een functie `fun`. Dit zorgt ervoor dat we later, bij het aanroepen van de functie (`l1 = genereer(fun1, 0, 0.5)`) pas hoeven te beslissen welke vergelijking we willen gebruiken bij het genereren van de lijst.

## Oefeningen

* Noem je programma toepassen.py
* Copieer de bovenstaande code in het programma.

### Oefening 1.1

Maak een functie `fun3()` voor de vergelijking `y = -4 * x + 4` en gebruik de bovenstaande functie `genereer` om waarden voor deze functie te genereren.

Verwachte output:

	[4.0, 3.6, 3.2, 2.8, 2.4]

### Oefening 1.2

Maak een functie `toepassen(fun, l)`. Het eerste argument is een functie, het tweede argument is een lijst. De functie `toepassen` past de functie `fun` toe op de element uit de lijst `l`. Test als volgt:

	l1 = toepassen(fun3, [-5, 0, -2, 2])
	print(l1)

Verwachte output:

	[24, 4, 12, -4]
