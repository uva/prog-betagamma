# Reële getallen

We hebben geleerd dat je een geheel getal als volgt print:

    x = 100
    print("x heeft de waarde {}".format(x))

Zodra de computer de string naar het scherm print zet hij op de plek waar `{}` staat de waarde die in de variabele *x* opgeslagen staat. In ons geval 100.

Soms wil je kunnen aangeven hoe een getal geprint wordt. Je kan bijvoorbeeld aangeven hoeveel decimalen achter de komma je wil printen.

    breuk = 3/17
    print("breuk = {:.2f}".format(breuk))

Als je dit print zal je zien dat, hoewel de variabele `breuk` de waarde 0.17647058823529413 heeft, dit programma de waarde 0.18 op het scherm print. Dat komt omdat je met {:.2f} hebt aangegeven dat je het getal op twee decimalen nauwkeurig wilt printen.

Probeer zelf een aantal opties.

> Het is handig om je probeersels op te slaan in een apart bestand, zodat je nog kunt terugkijken en stukjes code overnemen voor latere opdrachten. Dit testbestand hoef je niet in te leveren.

## Een rij reële getallen met behulp van `numpy.arange()`

In Module 1 hebben we de for-loop gebruikt om een variabele steeds met 1 op te hogen. In de for-loop constructie gebruikten we daarvoor de `range()` functie. De getallen 1 tot (en niet tot en met) 10, printen op het scherm, ze in een lijst stoppen en die printen aan het eind van het programma deden we als volgt.

    l = []
    for x in range(1,10):
        print("x heeft nu de waarde {}".format(x))
        l.append(x)
    print(l)

In Module 1 hebben we tijdens het tekenen van grafieken gezien hoe we punten (een lijst met x-waardes en een lijst met y-waardes) op het scherm kunnen tekenen. Om een functie te tekenen met een hoge precisie, in ons geval sin(x) leerden we dat we als we de functie wilde tekenen tussen 0 en 2pi we kleine stapjes, stel 0.01 moeten nemen. In Python is er een standaard functie die dat voor je kan doen, de `arange()` functie. Het is een functie die opgenomen is in de numpy bibliotheek.

    import numpy as np               # numpy mdule: nodig voor arange-functie
    import math                      # math module: nodig voor sin()-functie
    l_x = []
    l_y = []

    # x loopt van 0 tot 2pi in stapjes van 0.01
    for x in np.arange(0,2*math.pi, 0.01):
        y = math.sin(x)
        l_x.append(x)
        l_y.append(y)

Als je bijvoorbeeld de getallen van 2 tot 3 op het scherm wilt printen in stapjes van 0.02 dan kan doe je dat als volgt:

    import numpy as np
    x_begin = 2
    x_eind = 3
    dx = 0.02
    for x in np.arange(x_begin, x_eind, dx):
        print(x)

## Bekende valkuil: subtiel verschil tussen 'tot' en 'tot en met'

In het laatste voorbeeld zal het getal 2.0 wel, maar het getal 3.0 niet op het scherm geprint worden. In een van de opdrachten zal je wel degelijk het eindpunt moeten gebruiken. Let daarop. Probeer bovenstaande voorbeeld iets aan te passen zodat het eindpunt wel degelijk geprint wordt.
