# 2D-lijsten

Nu weer wat Python om te zorgen dat we dit algoritme kunnen bouwen. Je kunt al
met lijsten werken, en we gaan nu een tabel maken door een lijst met daarin lijsten te definiëren. Stel je hebt de volgende lijst:

    >>> l = ['a', 'b', 'c', 'd']

Om het tweede element te pakken gebruik je de brackets `[` en `]`.

    >>> print l[2]
    c

Laten we er een naam aan geven:

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

Hoe pak je daar dan een element uit? Aangezien je met lijsten werkt gebruik je
gewoon weer de brackets `[` en `]`!

Stel we willen de `h` pakken. Dan moeten we eerst uit `l` het derde element
pakken (index 2) om de lijst met de `h` te krijgen. Vervolgens moeten we van
die lijst het tweede element pakken (index 1) om de `h` te krijgen. Je kan dat
in één keer noteren:

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

Je kan dit dan zien als een tweedimensionaal veld waar je x- en y-coördinaten
kunt gebruiken! Om een tweedimensionale lijst aan te maken kun je het volgende doen:

    >>> l = []
    >>> for y in range(number_of_columns):
    >>>     l.append([]) # add row
    >>>     for x in range(number_of_rows):
    >>>         l[y].append( 'your element here' )

Om zoiets netjes te printen kun je het volgende doen:

    >>> for row in l:
    >>>     for xy in row:
    >>>         print xy, # comma makes sure no newline is printed
    >>>     print  # print a newline for the next row
