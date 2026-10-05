# Labo 3 - reflecties

Naam: Ahmed Chair

## 1. Kleurenstalen

- Welke twee waarden uit de user agent stylesheet moest je op de lijst wegwerken, en waar las je ze af?
 
  De browser past standaard padding en opsommingstekens toe op de ul (padding-left: 40px en list-style-type: disc).
  Ik heb dit ontdekt met behulp van DevTools: in de Styles-sectie zag ik de "user agent stylesheet", en in het boxmodel-diagram zag ik de waarde 40 links in het groene paddingvak. Ik heb ze weggewerkt met padding: 0 en list-style: none.

- Wat verandert er aan de banden als je het venster hoger maakt, en wat verandert er niet?

  Als het venster hoger wordt, worden de banden ook hoger, omdat de hoogte van de banden altijd 50% van de vensterhoogte is (50vh). Ook de ruimte boven de tekst neemt toe, omdat padding-top 20vh is. Maar de tekstgrootte, de letterafstand en de afstand tussen de codes blijven constant, omdat ze in rem staan, en rem hangt af van de lettergrootte en niet van het venster.

## 2. Slogan

- Welke property centreerde de tekst, en welke de kolom?
  
text-align: center → centreert de tekst in de kolom.

margin: 12rem auto 0 → centreert de kolom zelf; auto verdeelt de vrije ruimte links en rechts gelijk.

- Waarom werkte de padding op de knop pas na `display: inline-block`?

display: inline → een a negeert verticale padding.

display: inline-block → de a krijgt een volledig boxmodel, dus padding werkt wel.

## 3. Tabblad

- Wat is de visuele breedte van het tabblad, en waarom is dat exact 15rem en geen 15rem plus padding plus border?

- width: 15rem → het tabblad is visueel precies 15rem breed.
- box-sizing: border-box (in reset.css) → padding en border zitten binnen de width, en worden er niet bovenop geteld.
- zonder border-box → 15rem + 2 × 2rem padding + 2 × 0.25rem border = 19,5rem breed.

## 4. Donut

- Waarom werkt `height: 70%` op de cirkel, terwijl F3.2 zegt dat een procentuele hoogte meestal niets doet?

height: 70% → werkt alleen als de ouder zelf een vaste hoogte heeft.

height: 90vh op main → de ouder heeft hier een vaste hoogte, dus de browser kan 70% daarvan uitrekenen.

- Tegen welke maat van de ouder rekende de browser `margin: 15%`: de breedte of de hoogte?

margin: 15% → rekent altijd tegen de breedte van de ouder, ook boven en onder.

Computed-tabblad → hier zijn breedte en hoogte van main gelijk, dus de marge is aan alle kanten even groot.

## 5. Landingspagina

- Gaf je `main` een `height` of een `min-height`, en waarom?
- Wat gebeurt er met de twee helften als je een regeleinde zet tussen `</article>` en `<div class="afbeelding">`?

## Thuis: B3.1 (met AI of zonder AI)

Welke route koos je? Bij de AI-route: prompt en onbewerkte output staan in `site/review/`, en dit corrigeerde ik (met verwijzing naar de sectie of het foutnummer):

1. 
2. 
3. 
