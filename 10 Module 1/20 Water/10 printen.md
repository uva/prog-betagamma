# Printen

Laten we beginnen met programmeren. Snel experimenteren gaat makkelijk in de interactieve *shell* die bijgeleverd wordt met elke versie van de programmeertaal Python. Geef in de terminal het volgende commando om deze te starten:

    python2

In deze shell kun je een regel Python-code invoeren, waarna deze meteen wordt uitgevoerd. Probeer maar eens: `1 + 2` en druk op enter. Zodra je klaar bent met de Python shell kun je deze afsluiten door de volgende regel Python code uit te voeren:

	exit()

Wil je de Python shell openhouden voor experimenten en tegelijkertijd via de terminal werken? Dan kan je een tweede terminal starten door te klikken op het **+** icoon naast de oude terminal.

Laten we meteen wat Python code schrijven. Tik de volgende regels Python-code in de shell:

	print "Nobody expects the Spanish Inquisition!"
	print "Tis but a scratch"
	print "What Is the Airspeed Velocity of an Unladen Swallow?"

Het commando `print` in Python doet dan ook precies dat: het print uit wat er achter staat en voegt op het einde een enter toe. De aanhalingstekens rondom de tekst zijn nodig om aan te geven dat dit platte tekst is en geen uitvoerbare code (we noemen zo'n tekst tussen aanhalingtekens in Python een *string*). Probeer nu eens de volgende `print`-commando's:

	print 1
	print 1 + 1
	print 2 - 1, 3 + 4
	print "4 + 5"
	print "1 + 2 =", 1 + 2

Behalve strings printen, kan Python dus ook getallen printen en rekenen met getallen. Door die berekeningen wordt dus ook niet meer letterlijk uitgeprint wat je hebt ingetikt, maar het *resultaat* van de berekening. Ga alle regels langs en probeer te begrijpen waarom die regel print wat je ziet. Let daarbij op dat de komma (`,`) bij `print` gebruikt kan worden om meerdere waarden op één regel te printen: Python scheidt deze automatisch door middel van een spatie.
