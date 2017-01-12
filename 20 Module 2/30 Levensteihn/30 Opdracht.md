# Opdracht 5: `levensteihn_distance`

Maak een functie `levensteihn_distance` die twee strings als invoer krijgt en de
levensteihnafstand berekent en teruggeeft.

Er zijn een aantal stappen. Het eerste wat je wilt doen is vooraan beide strings
een leeg karakter stoppen (de null string) zodat we kunnen gaan rekenen vanaf
een lege string (het `""` naar `m` gedeelte van het voorbeeld).

Vervolgens wil je de tabel initialiseren met als afmetingen de lengtes van de
invoerstrings. De waardes van de tabel kan je in het begin allemaal op nul
zetten.

Hierna komt de fase om het aantal stappen te noteren waarmee je vanaf een lege
string de delen van het woord kunt verkrijgen.  Dit is het aantal karakters
tellen en opslaan in de tabel. Neem `n` voor de lengte van invoerwoord `a` en
`m` als lengte voor invoerwoord `b`.  De formule is dan:

    table[0][x] = x, for x = 0 ... n
    table[y][0] = y, for y = 0 ... m

In Python kan je dit doen met een for loop.

Nu komt het moeilijke gedeelte: het invullen van de vakjes. Je kan hiervoor
een dubbele for loop gebruiken. De eerst loopt over de kolommen, de tweede over
de rijen. Dit levert je twee coördinaten op. Vervolgens moet je de drie waardes
berekenen zoals eerder omschreven. Denk er aan dat je door de twee loops twee
coördinaten hebt (bijvoorbeeld x voor bij welke kolom je bent en y voor bij
welke rij je bent). De kleinste van de waardes die je berekent zet je in de
tabel.

Voor de duidelijkheid:

                        table[y-1][x] +1
    table[y][x] = min ( table[y][x-1] +1                                )
                        table[y-1][x-1] + (2 if a[i] == b[j], else 0)

Uiteindelijk return je de waarde van de tabel die rechts onderin staat.
