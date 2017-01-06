# Plot

## Specification

* Laten we beginnen, maak een file `plot.py` en schrijf daarin een programma dat de grafiek van de functie $$f(x) = x^x$$ tussen x = 0 en x = 1.5 in stapjes van 0.01 plot. Gebruik hiervoor een blauwe lijn.
* Zorg dat het minimum in de grafiek wordt aangegeven door middel van een rode stip.
* Laat je programma uitprinten, in de terminal, waar dit minimum zich bevindt.

![](plotje4.png)

## Hints


	import matplotlib
	matplotlib.use('Agg')
	import matplotlib.pyplot as plt


* Let op, om `matplotlib` goed te importeren binnen de ontwikkelomgeving, moet je gebruik maken van bovenstaande drie regels in je code.
* Kijk goed naar de voorbeelden.
* Google is je vriend.


## Testing
Testen is voor deze opdracht wat lastiger, want checkpy kan niet je grafiek beoordelen. Of deze grafiek correct is moet je dus zelf nagaan. Checkpy kan wel testen of je een grafiek maakt, en of de gevonden minpunten kloppen.


    checkpy plot

