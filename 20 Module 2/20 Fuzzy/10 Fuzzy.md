# Fuzzy matching

Het is ook vaak nuttig/handig om `bijna matches` te vinden. Bijvoorbeeld als er
maar 1 letter verschil is tussen de needle en een deel van de haystack. Zoiets
noemen we `fuzzy matches`.

We kijken weer naar de voorbeeldstring, ATGACATGCACAAGTATGCAT en de needle
ATGC. Als er 1 letter verschil mag zijn voor een mogelijke match vinden we op
index 0 al direct een match. We kunnen namelijk de laatste C van de needle in
een A veranderen om een fuzzy match te vinden!

Om fuzzy matches te vinden kunnen we een deel gebruiken van wat we eerder
hebben geknutseld. Om te beginnen breken we de needle op in twee substrings.
Vanaf het begin tot een karakter wordt deel `a`, en vanaf dat karakter + 1 wordt
deel `b` (we missen dus als je `a` en `b` aan elkaar plakt 1 karakter uit de
needle).

Dan vinden we de exacte matches van `a` in de haystack en de exacte matches van
`b` in de haystack (bijvoorbeeld door middel van de eerder gemaakte functie).

We nemen als voorbeeld voor de haystack ATGACATGCA voor de needle ATGC.
Voor deel `a` kiezen we `A` en voor deel `b` kiezen we `GC`. Zodanig krijgen we
twee lijsten: `[0, 3, 5, 9]` voor `a` en `[7]` voor `b`.

Nu kunnen we de fuzzy matches vinden door het verschil van de gevonden indices
te vergelijken. Hiervoor definiëren we nog drie variabelen: de index waarop een
deel `a` matcht noemen we `n`, de lengte van `a` noemen we `m` en de index
waarop een deel `b` matcht noemen we `k`. Als `n+m+1=k` waar is weten we dat er
een fuzzy match op index n te vinden is! Merk op dat we dit moeten doen voor
elk mogelijk paar tussen de matches van `a` en `b` om alle fuzzy matches te
vinden!
