# Labo 4 - reflecties

Naam: Chair Ahmed

## 1. Drie kolommen

- Op welk element staat `display: flex`, en op welke elementen staat `flex`?

display: flex → staat op main (de container); main zet zijn kinderen, de drie div’s, naast elkaar op één rij.

flex → staat op de drie div’s (de items); elk item zegt hoeveel van de vrije ruimte in de rij het neemt: flex: 1, flex: 2 en flex: 1, dus de middelste wordt dubbel zo breed.

- Waarom staan die twee niet op hetzelfde element?

display: flex → werkt op de kinderen van een element; het maakt van main een container die zijn kinderen op een rij zet.

flex → werkt alleen op een item binnen een flex-container; zet je flex op main, dan doet het niets, want main is zelf geen item van een flex-container.

## 2. Navigatiebalk

- Welke property verdeelt de ruimte langs de hoofdas, en welke lijnt uit op de kruisas?

justify-content → verdeelt de ruimte langs de hoofdas (horizontaal ↔); in de header zet space-between de naam helemaal links en de navigatie helemaal rechts.

align-items → lijnt de items uit op de kruisas (verticaal ↕); met center staan de naam en de navigatie verticaal in het midden van de balk.

- Wat gebeurt er met de links als je `gap` vervangt door `margin-right` op elke `li`?

margin-right → elke li krijgt rechts extra ruimte, ook de laatste (Contact); daardoor staat er een overbodige witruimte aan de rechterkant van de lijst en schuift de hele navigatie naar links, weg van de rand.

gap → zet ruimte alleen tússen de items en niet aan de buitenkant; bij 5 links zijn er dus precies 4 openingen en blijft Contact netjes tegen de padding van de balk staan.

## 3. Mondriaan

- Welke twee vlakken moest je expliciet plaatsen, en waarom volstond de impliciete vulling voor de andere vier?

grid-column → lila en olijf moesten van lijn 1 tot lijn 4 lopen, want ze zijn 3 kolommen breed; dat weet de browser niet vanzelf, dus moest ik het zelf zeggen.

grid-column (marine) → bij het testen bleek dat twee niet genoeg was: marine kwam vanzelf in kolom 2 terecht, want dat was het eerstvolgende vrije vakje na geel; daarom gaf ik marine ook een plaats: grid-column 4 / 5.

impliciete vulling → bruin, geel en rood hoefden niets: de browser zet ze vanzelf in het eerstvolgende vrije vakje, in de volgorde van de HTML, zoals letters in een schrift van links naar rechts.

- Waarom is `gap` hier beter dan een border op elk vlak?

gap → maakt de blauwe lijnen alleen tússen de vlakken, overal precies even dik (2vh), en het blauw is gewoon de achtergrond van het schilderij die erdoor schijnt; samen met padding krijg je ook de buitenrand.

border → als elk vlak een eigen rand krijgt, liggen er tussen twee vlakken twee randen tegen elkaar: die lijn wordt dan dubbel zo dik als de lijn aan de buitenkant; en de lege vakjes hebben geen rand, dus daar klopt het ook niet.

## 4. Trap

- Wat zie je als je de `grid-row`-declaraties weghaalt, en waarom?

grid-row weg → alle vier de treden springen naar de bovenste rij, naast elkaar; elke trede blijft wel in haar eigen kolom, maar de browser kiest zelf de rij en neemt de eerste vrije rij, en dat is rij 1.

waarom → zonder grid-row weet de browser alleen de kolom (de letter bij zeeslag), niet de rij (het cijfer); dan vult hij vanzelf van boven naar onder, en bovenaan is er in elke kolom nog plaats.

- Wat betekent `grid-column: 4 / -1` voor de laatste trede, en waarom werkt het hier ook?

grid-column: 4 / -1 → de trede begint bij lijn 4 en stopt bij de laatste lijn; -1 betekent “tel van achteren”, dus de allerlaatste lijn van het raster.

waarom het werkt → het raster heeft 4 kolommen en dus 5 lijnen; de laatste lijn is lijn 5, dus 4 / -1 is hier precies hetzelfde als 4 / 5.

## 5. Dierenasiel Zonnehoek

- Hoeveel layoutcontainers telt deze pagina, en welk gereedschap koos je voor elk?

aantal → 6 soorten containers, samen 10 stuks (want er zijn 5 kaarten).

body → grid: drie rijen onder elkaar (header, main, footer); main krijgt met 1fr alle rest, zodat de footer altijd onderaan plakt.

header → flex: één rij met de naam links en het menu rechts (space-between), verticaal in het midden (align-items: center).

nav ul → flex: de vier menu-links naast elkaar op één rij, met gap ertussen.

main → grid: titel, intro en kaarten onder elkaar met gap; align-content: start houdt ze bovenaan bij elkaar.

.kaarten → grid: drie kolommen, Nala loopt van lijn 1 tot lijn 3; twee assen, dus grid.

.kaart (5 keer) → flex in richting column: soort, naam, tekst en knop onder elkaar; de beschrijving krijgt flex: 1 en duwt de knop naar onderen.

- Verklein het venster tot de helft: wat breekt er, en in welk hoofdstuk wordt dat opgelost?

wat breekt → de drie kolommen blijven drie kolommen, ook op een smal scherm; de kaarten worden heel smal (± 176 px), de tekst wordt in korte stukjes gebroken en de kaarten worden heel hoog; op een gsm zou het menu ook niet meer passen.

waarom → het raster heeft altijd repeat(3, 1fr): het weet niet dat het scherm smaller is en past zich niet aan.

hoofdstuk → H6 Responsive (volgens de planning): daar leer je de layout aanpassen aan de breedte van het scherm, bijvoorbeeld minder kolommen op een smal scherm.

## Thuis: B4.1 (met AI of zonder AI)

Welke route koos je? Bij de AI-route: prompt en onbewerkte output staan in `site/review/`, en dit corrigeerde ik (met verwijzing naar de sectie of het foutnummer):

1. 
2. 
3. 
