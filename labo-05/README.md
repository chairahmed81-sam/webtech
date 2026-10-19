# Labo 5 - reflecties

Naam: Chair Ahmed

## 1. Letterraster

- Wat gebeurt er als je in de template één gebied een L-vorm geeft, en waarom?

Een gebied moet altijd een rechthoek zijn. Als ik van “a” een L-vorm maak, klopt de tekening niet meer en negeert de browser de hele grid-template-areas. Je krijgt geen foutmelding, de vlakken staan gewoon niet meer op hun plaats (F5.6).

- Hoeveel declaraties zou dezelfde plaatsing met `grid-column` en `grid-row` vragen?

Dan moet elk vlak 2 regels krijgen, één voor de kolom en één voor de rij. Bij 8 vlakken is dat 16 regels. Met areas heb ik 1 tekening en 8 keer grid-area, dus 9 regels, en ik zie meteen hoe het raster eruitziet.

## 2. Citaten

- Waarom lijnt de tweede rij bij 1280 px niet uit met de eerste zoals een grid dat zou doen?

Flexbox werkt maar in één richting. Elke rij verdeelt zijn eigen plaats en weet niets van de rij erboven. Grid heeft echte kolommen die door alle rijen lopen, flex niet. Hier lijkt het uit te lijnen omdat er 4 en 4 staan, maar als de laatste rij minder citaten heeft, worden die breder.

- Wat verandert er als je de basis van 18rem naar 30rem zet, en waarom?

Elk citaat wil dan 30rem breed zijn in plaats van 18rem. Daardoor passen er bij 1280 px maar 2 op een rij en bij 800 px nog maar 1. Ze worden wel nog breder tot de rij vol is, omdat grow op 1 staat.

## 3. Fotolijst

- Waar belanden de vlakjes als je `position: relative` van de lijst weghaalt, en waarom?

Zonder position: relative op de lijst → Een absolute vlakje zoekt de eerste ouder met een position. Als de lijst die niet heeft, vindt hij niemand en rekent hij vanaf de hele pagina. Groen en roze staan dan linksboven in het venster en lime en rood rechtsonder in het venster, niet meer op de foto (F5.1).

- Waarom ligt roze zonder `z-index` onder groen?

Roze onder groen zonder z-index → Zonder z-index beslist de volgorde in de HTML wie bovenop ligt: wat later komt, ligt hoger. In de HTML staat roze vóór groen, dus groen wordt later getekend en ligt erop. Dat roze op het scherm verder naar rechts en lager staat, maakt niet uit. Alleen de volgorde in de code telt.

## 4. Toonzaal

- Wat gebeurt er als je `top: 0` weghaalt, en waarom?
- Wat is het verschil met `position: fixed` voor de rest van de pagina, en welke extra declaratie zou fixed nodig hebben?

## 5. Koffiebar Kaai 12

- Welke drie vragen van deze week (container, item, plaatsing) beantwoordde je waar in deze pagina?
- Haal `aspect-ratio` weg bij de foto's: wat gebeurt er met het rooster, en waarom?

## Thuis: B5.1 (met AI of zonder AI)

Welke route koos je? Bij de AI-route: prompt en onbewerkte output staan in `site/review/`, en dit corrigeerde ik (met verwijzing naar de sectie of het foutnummer):

1. 
2. 
3. 
