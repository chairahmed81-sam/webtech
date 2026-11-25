# Labo 8 - reflecties

Naam: Chair Ahmed

Wat ik in 8.1 noteerde over de hover- en focusfeedback op mijn eigen site: Ik heb nog geen eigen site, dus ik kon dit niet testen.

## 1. Maaklab Linkeroever: kaarten die reageren

- De transition verplaatst van `.kaart` naar `.kaart:hover`: wat zie je als de muis de kaart verlaat, en hoe heet dat?

  transition op .kaart:hover → als ik met de muis op de kaart ga, komt ze rustig omhoog. Als ik de muis weghaal, springt ze ineens terug, want zonder hover is er geen transition meer. Dat heet "de halve overgang" (F8.1). De transition moet dus op .kaart staan, niet op :hover.

- `translateY(-0.25rem)` vervangen door `margin-top: -0.25rem`: wat gebeurt er met de buren en met de voet?

  De eerste kaart gaat omhoog en krijgt een schaduw. De andere kaarten en de footer blijven op hun plaats. De kaart springt omhoog omdat margin-top niet in de transition staat. De schaduw verandert wel geleidelijk (F8.3).
  transform: translateY(-0.25rem) → schuift alleen de kaart zelf, de rest van de pagina blijft gewoon staan.

- Hoeveel transitions vuren er af in het Animations-paneel als je over één kaart gaat?

  Animations-paneel → als ik over één kaart ga, vuren er 2 transitions af: één voor transform en één voor box-shadow.

## 2. Buurthuis Stuivenberg: prikbord

- `transform-origin: top left` ook op het eerste briefje: wat verandert er, en waarom?

  transform-origin: top left → het briefje draait dan rond zijn linkerbovenhoek in plaats van rond zijn midden. Die hoek blijft op zijn plaats staan en de rest draait eromheen, zoals een deur rond een scharnier. Daardoor schuift het briefje een klein beetje naar rechts en naar boven.

- De volgorde omgekeerd bij de stempel (`rotate(12deg) translate(25%, -50%)`): waar staat hij nu?

  rotate(12deg) translate(25%, -50%) → nu draait de stempel eerst en schuift hij pas daarna. Hij schuift dan in de schuine richting, dus hij staat een klein beetje lager en meer naar rechts dan eerst. De volgorde in transform is dus belangrijk.

- Een briefje wordt bij hover 5% groter: waarom schuiven de buren niet op?

  transform: scale(1.05) → een transform verandert alleen hoe het briefje eruitziet, niet de layout. Het briefje houdt zijn plaats in het raster, dus de buren merken niets en schuiven niet op.


## 3. Scheldeveer: vertrekbord

- Waarom is de stip een animation en de kaart-lift van oefening 1 een transition?

  animation → de stip pulseert vanzelf en blijft altijd doorgaan, zonder dat iemand iets doet. Daar heb je een animation met @keyframes voor nodig.
  transition → de kaart-lift gebeurt alleen als ik met de muis op de kaart ga (of met Tab). Een transition beweegt alleen van A naar B als er iets verandert.

- Welke curve heeft de stip en welke de ring, en waarom is `linear` hier juist en bij de kaart niet?

  ease-in-out → de stip begint traag, gaat sneller en eindigt weer traag. Zo pulseert ze zacht, zoals ademen.
  linear → de ring draait de hele tijd even snel. Bij iets dat rond en rond draait is dat juist, anders zou hij bij elke toer vertragen en weer versnellen en lijkt hij te haperen.
  bij de kaart → daar is linear niet goed, want de kaart moet zacht landen op haar plaats. Met linear voelt het stijf en zoals een machine.

- Met de emulatie *prefers-reduced-motion* aan: wat staat er stil, en is er iets onleesbaar of onbereikbaar geworden?

  prefers-reduced-motion: reduce → de stip pulseert niet meer en blijft gewoon zichtbaar, de ring draait niet meer en de nieuwe afvaart staat meteen op haar plaats.
  leesbaarheid → niets is onleesbaar of onbereikbaar geworden. Alle tekst en alle afvaarten zijn nog gewoon te zien, alleen de beweging is weg.


## 4. Rondje

- De curve op `linear`: wat verandert er in de hoeken, en op welk stuk van de animatie werkt een curve dus?

  Bij linear beweegt het blok met een constante snelheid. In de hoeken verandert het plots van richting, zonder te vertragen.
  curve → een curve werkt dus op elk stuk tussen twee keyframes apart (van 0% naar 25%, van 25% naar 50%, ...), niet één keer op de hele animatie.

- Met de emulatie *prefers-reduced-motion* aan: waar staat het blok, en in welke kleur?

  prefers-reduced-motion: reduce → het blok staat stil linksboven en is geel, net zoals het begin van de animatie.


## 5. Estafette

- Zonder `alternate`: wat doet een loper aan de rechterrand?

  zonder alternate → de loper komt aan de rechterrand en springt dan ineens terug naar links om opnieuw te beginnen. Met alternate loopt hij netjes terug.

- Waarom verplaats je de loper met `transform` en niet met `margin-left`?

  transform: translateX(...) → schuift alleen de loper zelf, de layout blijft hetzelfde. Het loopt vloeiend.
  margin-left → dan verandert de layout bij elke stap en moet de browser alles opnieuw uitrekenen. Dat is zwaarder en kan haperen (F8.3).


## 6. Pijlen

- `100% 50%` en `0 50%` geschrapt uit `--vierkant`: wat gebeurt er met de overgang, en waarom?

  --vierkant met vier punten → de tegel verandert niet meer zacht van vorm. Ze blijft eerst een pijl en springt dan halverwege ineens naar een vierkant (en weer terug).
  waarom → de browser kan een polygon alleen geleidelijk laten veranderen als beide vormen evenveel punten hebben. Hij schuift dan elk punt naar zijn nieuwe plaats. Bij 6 en 4 punten weet hij niet welk punt waarheen moet, dus springt hij.


## Thuis: B8.1 (met AI of zonder AI)

Welke route koos je? Welke ene animatie heeft een aanleiding, en welke? Bij de AI-route: prompt en onbewerkte output staan in `site/review/`, en dit corrigeerde ik (met verwijzing naar de sectie of het foutnummer):

1. Ik heb nog geen eigen website. Daarom heb ik B8.1 nog niet uitgevoerd.
2. 
3. 
