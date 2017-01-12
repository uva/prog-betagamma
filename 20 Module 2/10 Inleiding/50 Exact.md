# Opdrachten

## Opdracht 1: `count_exact_matches`

Maak een functie `count_exact_matches` die in ieder geval twee argumenten
heeft: de `haystack`, de string waarin we zoeken, en `'needle`', de string die
we zoeken. De functie moet het aantal keer tellen dat de needle in de haystack
voorkomt en dat als integer returnen.

Voorbeeld:

    >>> result = count_exact_matches("atgacatgcacaagtatgcat","atgc")
    >>> print result
    2

Hints:
 * Maak gebruik van de functie `find`.
 * Hou een variabele bij waarin je bijhoudt vanaf welke index find moet gaan
zoeken.

## Opdracht 2: `exact_matches`

Maak een functie `exact_matches` vergelijkbaar aan de functie die je
net gemaakt hebt. Alleen deze keer moet er een lijst gereturned worden met de
indices van de matches van de needle in haystack.

Voorbeeld:

    >>> result = exact_matches("atgacatgcacaagtatgcat","atgc")
    >>> print result
    [5, 15]

Hint:
 * Dit is bijna hetzelfde als de functie `count_exact_matches` alleen ga je nu
niet tellen maar moet je de indices aan een lijst toevoegen met behulp van
`append`.
