# Opdrachten

Het lijkt misschien lastig of veel werk om dit te programmeren. Een belangrijke
vaardigheid bij het programmeren is een groot en moeilijk probleem opdelen
in kleinere problemen die makkelijker op te lossen zijn. Dit noemen we
probleemdecompositie. Nu doen we dit nog voor. Eerst moet je de mogelijk delen
voor `a` en `b` genereren. Vervolgens kun je die code gebruiken om de fuzzy
matches te vinden.

## Opdracht 3: `split_needle`

Maak een functie `split_needle` die gegeven een string van lengte >= 3 alle
mogelijke substrings genereert met één missend karakter voor `a` en `b`.

Voorbeeld:

    >>> result = split_needle("abcd"):
    >>> print result
    [('', 'bcd'), ('a', 'cd'), ('ab', 'd'), ('abc', '')]
    >>> print split_needle("abcde")
    [('', 'bcde'), ('a', 'cde'), ('ab', 'de'), ('abc', 'e'), ('abcd', '')]

Het formaat wat je hier gebruikt is een lijst met tuples. Een
tuple zijn twee variabelen die als het ware in 1 variabele wordt gestopt.
Bijvoorbeeld zo:

    >>> part_a = "left"
    >>> part_b = "right"
    >>> my_tuple = (part_a, part_b)
    >>> print my_tuple
    ('left', 'right')
    >>> print my_tuple[0]
    left

## Opdracht 4: `fuzzy_matches`

Maak een functie `fuzzy_matches` die gegeven een haystack en een needle een
lijst met indices van alle fuzzy matches maakt.

Voorbeeld:

    >>> fuzzy_matches = fuzzy_matches("atgacatgca", "atgc")
    >>> print fuzzy_matches
    [0, 5]

Er zijn meerdere manieren om dit te doen. Hier een paar tips. Het eerste wat je
hier wilt doen is alle mogelijke delen van de needle genereren door de functie
die je net hebt gemaakt te gebruiken. Dan kun je per paar gaan zoeken naar het
eerste deel en het tweede deel. Voor de matches van een paar kun je vervolgens
de formule toepassen om te checken of er een match op die index is of niet.
Uiteindelijk wil je wellicht gedupliceerde elementen uit de lijst verwijderen.

Merk op dat dit nog niet bijzonder efficiënt is. Zo worden er waarschijnlijk
meerdere malen dezelfde indices doorzocht op matches. Kun je een deel afsluiten
zodat er geen dubbel werk gedaan wordt? Kun je meer verbeteringen vinden?
