# Printen

Laten we beginnen met programmeren in Python. Python is een geïnterpreteerde programmeertaal. Dit houdt in dat Python jouw geschreven code leest, en meteen uitvoert. Laten we meteen beginnen en wat Python code schrijven om dit vervolgens te *runnen*. Open het bestand `print.py` dat je eerder hebt aangemaakt. Type of copy-paste daarin de volgende regels Python code:


	print "Nobody expects the Spanish Inquisition!"
	print "Tis but a scratch"
	print "What Is the Airspeed Velocity of an Unladen Swallow?"


Zie hoe sommige delen van de tekst anders kleuren in de editor. Dit is "syntax highlighting" wat door de editor wordt toegevoegd om stukken code voor jou als programmeur uit te lichten. Run nu je code door het volgende commando uit te voeren in de terminal:


	python2 print.py


Met dit commando vertel je Python om het bestand `print.py` uit te voeren. Nu zie je in de terminal een drietal regels geprint staan. Het commando `print` in Python doet dan ook precies dat, het print uit wat ernaast staat en voegt een enter toe. De aanhalingstekens rondom de tekst zijn nodig om aan te geven dat dit tekst is, een `string` (een serie tekens), en niet uitvoerbare code. Voeg nu eens de volgende regels code toe, en run nog een keer.


	print 1
	print 1 + 1
	print 2 - 1, 3 + 4
	print "4 + 5"
	print "1 + 2 =", 1 + 2


Behalve strings printen, kan Python dus ook getallen printen en rekenen met getallen. Ga alle regels langs en probeer te begrijpen waarom die regel dat print wat je ziet in de terminal. Let daarbij op dat de komma (`,`) bij `print` gebruikt kan worden om meerdere dingen op één regel te printen, Python scheidt deze automatisch door een spatie.