# Labo 7 - reflecties

Naam: Chair Ahmed

De telling van mijn eigen site vóór dit labo (7.1): font-sizes ... / marges en paddings ... / kleuren ...

## 1. Tintenladder

- Wat is de contrastratio van het label op de vijfde band, en op de zesde? Wat gebeurt er als je de wissel van inkt naar papier één band later legt?

    Band 5 (inkt op 55%) heeft een contrast van 4.73 en band 6 (papier op 45%) heeft 4.67. Allebei zitten ze net boven de 4.5 die minimaal moet. Als ik de wissel één band later leg (n + 7), krijgt band 6 donkere tekst en zakt het contrast naar 3.36. Dat is te laag, dus dan is het label slecht leesbaar. De wissel staat dus precies op de juiste plaats.

- Je verandert `--hue` in 25: hoeveel regels paste je aan, en wat zegt dat over 7.6?

    Ik paste maar 1 regel aan: --hue op :root. Alle 10 banden werden in één keer oranje, omdat ze allemaal var(--hue) gebruiken. Dat bewijst wat 7.6 zegt: als je de hue in een token zet, verander je met één regel een hele reeks kleuren, en je hoeft niet 10 kleuren apart te zoeken.

## 2. Leespagina

- Waarom is de kolom op 1280 px zo'n 674 px breed en niet 65 keer 16 px?

Omdat ch geen 16 px is. 1ch is de breedte van het cijfer 0 in de letter die je gebruikt, en een letter is smaller dan hij hoog is. In Atkinson Hyperlegible is 1ch ongeveer 10,4 px (gemeten in DevTools met width: 10ch). 65 × 10,4 px is ongeveer 674 px. Als je een andere letter kiest, wordt de kolom ook breder of smaller.

- Wat verandert er als je de ratio op 1.2 zet, en hoeveel regels pas je daarvoor aan?

Met ratio 1.2 wordt alles een beetje kleiner, behalve de gewone tekst (m blijft 1rem). Vooral de titel en de koppen worden kleiner, en het verschil tussen h2 en h3 is kleiner, dus de pagina wordt rustiger maar de koppen vallen minder op. Ik moest maar 5 regels aanpassen: de 5 tekstmaten op :root (s, l, xl, xxl en xxxl). Buiten :root moest ik niets veranderen, omdat alles met var() naar de tokens verwijst.

- Hoeveel verschillende waarden voor `margin` en `padding` staan er in je bestand, en komen ze allemaal uit de schaal?

Ik vond 5 verschillende waarden voor margin en padding: xs, s, m, l en xl. Ze komen allemaal uit de schaal op :root, ik gebruik ze altijd met var(). Daarnaast staan er alleen 0 en auto, en die mogen. Er staat dus geen losse waarde in mijn bestand.

## 3. Frituur 't Pleintje

- Hoeveel declaraties staan er in je donkere query? Als het er meer dan vijf zijn: welke kleur ontsnapte?
- Het label "nieuw": wat zijn de ratio's in het licht en in het donker, en welke is de krapste?
- Waarom staat de tekst van het label in `--color-surface` en niet in `white`?

## 4. De kaaien

- Waarom staat de foto als achtergrond en niet als `img`?
- Zonder de achtergrondkleur van `.paneel`: wat is de contrastratio van de titel op het lichtste deel van de foto?
- Wat doet `background-repeat: no-repeat` met de voet, en `contain` in plaats van `cover` met de held?

## 5. Fietsatelier Noord

- Staat er in `stijl.css` nog een letterlijke kleur, letter of maat buiten `:root`? Welke, en waarom ontsnapte ze?
- Hoeveel regels telt `thema.css` zonder de `@font-face`-blokken?
- Wat betekent dat voor B7.1 en je eigen site?

## Thuis: B7.1 (met AI of zonder AI)

Welke route koos je? De twee screenshots van de tokenwissel staan in `site/review/`. Bij de AI-route: prompt en onbewerkte output staan in `site/review/`, en dit corrigeerde ik (met verwijzing naar de sectie of het foutnummer):

1. 
2. 
3. 
