# Labo 2 - reflecties

Naam: Ahmed Chair
## 2. Selectors lezen

Welke elementen raakt elke selector? Eén zin per selector.

- a. `header nav ul li a`: Elke link a die in een li staat, in een ul staat en in een nav staat en dit binnen de header  
- b. `article > p`: Elke paragraaf die direct in een article staat
- c. `.uren li:nth-child(3)`: Elk lijstitem (li) dat het 3de kind is van zijn ouder, en dat ergens binnen het element met class uren zit
- d. `h2 ~ p`: Elke paragraaf die ergens na een h2 komt, met dezelfde ouder
- e. `.rassen li:first-child`: Elk lijstitem (li) dat het eerste kind is van zijn ouder, en dat ergens binnen het element met class rassen zit

## 3. Voorspel, dan kijk

Vul de eerste twee kolommen in vóór je de pagina opent. Trede: herkomst, specificiteit, volgorde of overerving (of iets anders, benoem het).

| vraag | mijn voorspelling (kleur) | beslissende trede | uitkomst in de browser | juist? |
|---|---|---|---|---|
| 1 | Groen | Gewone CSS-regel | Groen | Ja |
| 2 | Blauw | Volgorde | Blauw | Ja |
| 3 | Rood | Specificiteit | Rood | Ja |
| 4 | Rood | De groene selector raakt de link niet | Rood | Ja |
| 5 | Blauw | Specificiteit | Blauw | Ja |
| 6 | Blauw | Eigen class wint van overerving | Blauw | Ja |
| 7 | Rood | Overerving | Rood | Ja |
| 8 | Blauw | Inline style | Blauw | Ja |
| 9 | Rood | !important | Rood | Ja |
| 10 | Groen | Fout door ontbrekende puntkomma | Groen | Ja |

Bij welke vraag zat je fout, en wat was de reden? (Alles juist? Welke vraag duurde het langst, en waarom?)

Vraag 5 vond ik het moeilijkst, omdat ik eerst niet goed wist welke selector voorrang kreeg. Daarna begreep ik dat een ID zwaarder doorweegt dan meerdere classes.

## 4. De nabouw

- Welke selector koos je voor de links in de navigatie, en waarom geen class?

Ik heb nav a gebruikt, omdat hiermee alle links in de navigatie geselecteerd worden. Een extra class was niet nodig.

- Welke regel kostte je het meeste tijd, en wat was uiteindelijk de oorzaak?

Het zebrapatroon vond ik het moeilijkst. Ik moest uitzoeken hoe ik met nth-child(odd) alleen de oneven lijstitems een achtergrondkleur kon geven.

## 6. Je site

- Welke drie waarden staan in je tokenblok, en waarom die?

Ik heb onder andere --achtergrond, --tekst en --hoofdkleur gebruikt. Hiermee kan ik de achtergrond, tekstkleur en groene hoofdkleur gemakkelijk aanpassen.

- Wat verandert er in je site als je één token wijzigt?

Als ik bijvoorbeeld --hoofdkleur verander, krijgen de bovenbalk, footer en titels automatisch een andere kleur op alle vier de pagina's.

## Thuis: R2.3 (met AI)

Prompt en onbewerkte output staan in `review/`. Minstens vijf bevindingen, elk met een verwijzing naar de sectie of het foutnummer:

1. Bij `:root` gebruikt de AI vijf kleurvariabelen. Dat is goed, want zo kan ik de kleuren gemakkelijk op één plaats aanpassen.

2. Bij `body` gebruikt de AI Verdana als lettertype en een regelafstand van 1.6. Dit komt overeen met de opdracht.

3. Bij `nav a` heeft de AI de links een accentkleur gegeven en de onderstreping weggehaald. Dit komt overeen met de opdracht.

4. Bij `.kaart li:nth-child(odd)` geeft de AI de oneven lijstitems een andere achtergrondkleur. Zo ontstaat het zebrapatroon uit de screenshot.

5. Bij `.prijs` gebruikt de AI de accentkleur voor de prijzen. In de screenshot zijn de prijzen grijs en cursief. Dit zou ik aanpassen naar `color: var(--gedempt)` en `font-style: italic`.
