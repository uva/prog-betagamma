# Levensteihnafstand

De levensteihnafstand is gedefinieerd als het minimale aantal bewerkingen die er
nodig zijn om van de ene string de andere te maken. Het geeft dus aan in welke
mate een string op een andere lijkt.

Deze maatstaf wordt bijvoorbeeld gebruikt in informatietheorie om berichten te
ontcijferen. Het kan ook gebruikt worden om spell checkers te verbeteren, of
de fouten van een optisch karakterherkenningsprogramma te verbeteren. In ons
geval kunnen we deze toepassen om uit te rekenen hoeveel de ene DNA-sequentie op
de andere lijkt of om twee DNA-sequenties zo over elkaar te schuiven dat ze het
meest op elkaar lijken. Verdere toepassingen zijn te vinden in machine
vertaling, informatie extractie en spraakherkenning.

Er zijn drie soorten bewerkingen op een string mogelijk:
 * Er kan een letter weggehaald worden  
 * Er kan een letter toegevoegd worden  
 * Er kan een letter gesubstitueerd worden  

De eerste twee bewerkingen hebben als arbitraire kost 1. De laatste bewerking
kost twee want dit is hetzelfde als 1 letter weghalen en vervolgens 1 letter
toevoegen.

Dus om de levensteihnafstand te berekenen willen we het aantal bewerkingen weten
om van een string `a` naar een string `b` te komen. Je krijg dan iets als
`levensteihnafstand(a, b)`. Om dit te berekenen delen we het probleem op in
kleinere stukken. De afstand om een string te krijgen van een lege string is
simpelweg de lengte van de string aan toevoegingen. Dus `levensteihnafstand("",
"test")` is vier want je moet vier keer een letter toevoegen om de lege string
naar het woord test om te zetten.

Laten we kijken wat het verschil is tussen de woorden `majeur` en `mineur`

Eerst beginnen met de kost om van een lege string naar `m` te komen (1
toevoeging), dan naar `ma` (2 toevoegingen), naar `maj` te komen (3), tot `majeur`
(6). We schrijven dit op in een tabel:

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |

En we doen hetzelfde voor mineur:

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| m | 1 |
| i | 2 |
| n | 3 |
| e | 4 |
| u | 5 |
| r | 6 |

Hier kun je dus in de tabel in kolom x en rij y aflezen hoeveel het kost om het
woord `a` tot de xde letter om te bouwen vanaf het woord `b` tot de yde letter.
Uiteindelijk willen we dus helemaal rechts onderin komen om te zien hoeveel het
kost om het hele woord a om te bouwen tot b of andersom.

We gaan elk vakje invullen met de levensteihnformule. Gegeven dat we nu
weten hoeveel het kost om een kleinere string om te bouwen kunnen we makkelijker
berekenen hoeveel het kost om een iets langere string om te bouwen, waarna we
weer een iets langere string kunnen opbouwen tot het einde.

Nu de levensteihnformule. Het ziet er ingewikkelder uit dan het is, dus schrik
niet. De waarde die we in een vakje invullen is afhankelijk van drie manieren
waarop we er kunnen komen (wat de geschiedenis is):
 1) voor een toevoeging/verwijdering vanaf string `a` nemen we de waarde op plek
`(x-1, y)` + 1 
 2) voor een toevoeging/verwijdering vanaf string `b` nemen de waarde op plek
`(x, y-1)` + 1 
 3) als karakter x op plek `a` hetzelfde is als karakter y op plek `b` dan nemen
we de de waarde op plek `(x-1, y-1)`+0 want dan is er niets aan de hand. Als
deze niet gelijk is moeten we substitueren en nemen we de vorige waarde + 2, dus
`(x-1, y-1)` + 2 We nemen hiervan diegene die het kleinste resultaat oplevert en
die vullen we in in het vakje.

We nemen het voorbeeld erbij. We kijken bij het eerste lege vakje of we de
string opbouwen
 1) van `""` naar `m` (kost 1)
 2) van `""` naar `m` (kost 1)
 3) of dat er een substitutie nodig is (kost 2), of dat de letter al klopt (kost
0)

In ons voorbeeld klopt de letter al en vullen we een 0 in.

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| m | 1 | 0 
| i | 2 |
| n | 3 |
| e | 4 |
| u | 5 |
| r | 6 |

Volgende vakje (naar rechts).
 1) van `m` naar `ma` kost 1 toevoeging, we komen via het pad van dezelfde
letter van het vorige vakje want we kijken 1 naar links, dus totale kost = 1
 2) van `ma` naar `m` kost 1 verwijdering, we komen via het pad 2 toevoegingen,
dus de totale kost is hier 3 want we kijken 1 naar boven, dus totale kost = 3
 3) van `m` naar `ma` kost 2, we komen via links boven, dus totale kost = 3

Dus we vullen 1 in:

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| m | 1 | 0 | 1
| i | 2 |
| n | 3 |
| e | 4 |
| u | 5 |
| r | 6 |

Zo gaan we door. Bij het volgende vakje kunnen we vanaf `ma` `maj` maken met 1
toevoeging:

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| m | 1 | 0 | 1 | 2
| i | 2 |
| n | 3 |
| e | 4 |
| u | 5 |
| r | 6 |

Rij compleet:

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| m | 1 | 0 | 1 | 2 | 3 | 4 | 5 |
| i | 2 |
| n | 3 |
| e | 4 |
| u | 5 |
| r | 6 |

`mi` van `m` maken:

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| m | 1 | 0 | 1 | 2 | 3 | 4 | 5 |
| i | 2 | 1 |
| n | 3 |
| e | 4 |
| u | 5 |
| r | 6 |

Nu is er weer een interessante. We moeten van `mi` naar `ma`. Alle drie de
kosten komen op 2 uit: 2 toevoegingen of 1 substitutie:

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| m | 1 | 0 | 1 | 2 | 3 | 4 | 5 |
| i | 2 | 1 | 2 |
| n | 3 |
| e | 4 |
| u | 5 |
| r | 6 |

En helemaal op het einde:

|   |   | m | a | j | e | u | r |
|   | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| m | 1 | 0 | 1 | 2 | 3 | 4 | 5 |
| i | 2 | 1 | 2 | 3 | 4 | 5 | 6 |
| n | 3 | 2 | 3 | 4 | 5 | 6 | 7 |
| e | 4 | 3 | 4 | 5 | 4 | 5 | 6 |
| u | 5 | 4 | 5 | 6 | 5 | 4 | 5 |
| r | 6 | 5 | 6 | 7 | 6 | 5 | 4 |

De goedkoopste manier om van mineur naar majeur te komen is vier en dat lees je
af rechts onderin.

