# 2D-lijsten

Een tabel in Python is makkelijk te bouwen. Je kunt al met lijsten werken
en een tabel is niets anders dan een lijst in een lijst. Stel je hebt de
volgende lijst:

    >>> l = ['a', 'b', 'c', 'd']

Om het tweede element te pakken gebruik je de brackets `[` en `]`.

    >>> print l[2]
    c

Alternatief kan hier ook eerst een naam aan geven:

    >>> element = l[2]
    >>> print element
    c

Nou stel je voor dat de elementen die in je lijst zitten ook lijsten zijn.

    >>> l = [ ['a', 'b', 'c'], ['d', 'e', 'f'], ['g', 'h', 'i'] ]
    >>> print l[2]
    ['g', 'h', 'i']

Alternatief:

    >>> element = l[2]
    >>> print element
    ['g', 'h', 'i']

Hoe pak je daar dan een element uit? Aangezien je met lijsten werkt gebruik
je weer de brackets `[` en `]`! Stel we willen de `h` pakken. Dan moeten we
eerst uit `l` het derde element pakken (index 2) om de lijst met de `h` te
krijgen. Vervolgens moeten we van die lijst het tweede element pakken (index 1)
om de `h` te krijgen. Je kan dat in één keer noteren:

    >>> print l[2][1]
    h

Of met een tussenstap:

    >>> element = l[2]
    >>> print element[1]
    h

Alternatief:

    >>> element = l[2]
    >>> letter = element[1]
    >>> print letter
    h

Je kan dit dan zien als een twee dimensionaal veld waar je x en y coördinaten
kan gebruiken!

Om een twee dimensionale lijst te maken (ook wel nested list genoemd) kun je het
volgende doen:

    >>> l = []
    >>> for y in range(number_of_columns):
    >>>     l.append([]) # add row
    >>>     for x in range(number_of_rows):
    >>>         l[y].append( 'your element here' )

Om zoiets netjes te printen kan je het volgende doen:

    >>> for row in l:
    >>>     for xy in row:
    >>>         print xy, # comma makes sure no newline is printed
    >>>     print  # print a newline for the next row
