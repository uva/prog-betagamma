# Strings

Een string is een veelgebruikt datatype in allerlei programmeertalen, zo ook in
Python. In deze opdracht gaan we strings toepassen in de context van een
probleem uit de biologie.

Het goede nieuws is dat je afgelopen week al strings hebt gebruikt! In de editor
van de IDE kun je strings herkennen doordat deze groen weergegeven worden. Een
string is simpelweg een serie karakters en kan gebruikt worden om woorden en
zinnen te representeren in code.

Om aan te geven dat een string begint zet je aanhalingstekens `"` neer.
Vervolgens zet je het woord of zin neer wat je in de string wilt hebben. Je
eindigt weer aanhalingstekens `"`. Om `abcde` in een string te zetten doen we
dus:

    >>> my_string = "abcde"

Je kunt een karakter uit de string pakken door de string te indexen:

    >>> print my_string[0]
    a
    >>> print my_string[1]
    b
