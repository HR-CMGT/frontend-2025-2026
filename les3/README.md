# Les 3

- [Les 3](#les-3)
  - [Leeruitkomsten](#leeruitkomsten)
- [Flexbox](#flexbox)
  - [Parent/child](#parentchild)
  - [Flexbox in een Flexbox](#flexbox-in-een-flexbox)
  - [Meest gebruikte Flexbox-opties](#meest-gebruikte-flexbox-opties)
  - [Flexbox-inspector 🔍](#flexbox-inspector-)
  - [Hulpbronnen voor Flexbox](#hulpbronnen-voor-flexbox)
- [Minipuzzels - Flexbox](#minipuzzels---flexbox)
- [Opdracht 1: Foodblog genereren met AI](#opdracht-1-foodblog-genereren-met-ai)
  - [Doel](#doel)
  - [Aanpak](#aanpak)
  - [Quiz](#quiz)
    - [HTML](#html)
    - [CSS](#css)
- [Opdracht 2: Foodblog](#opdracht-2-foodblog)
  - [Advanced opdracht](#advanced-opdracht)

<br><hr><br>

## Leeruitkomsten

In deze les werk je aan de volgende leeruitkomst:

| Leeruitkomst                                                                                                            | Toelichting                                                      |
| ----------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| 2. Ik kan uitleggen hoe een layout tot stand komt in de browser en kan een responsive webpagina bouwen met HTML en CSS. | In deze les leer je hoe je met Flexbox een layout kunt opbouwen. |

<br>

Alle leeruitkomsten zijn terug te vinden in de [cursushandleiding](https://brightspace.hr.nl/d2l/home/192811) @TODO:
juiste link invoeren.

<br><hr><br>

# Flexbox

In de afgelopen lessen heb je elementen alleen nog maar _onder elkaar_ gezet. Wil je de mogelijkheid om elementen ook
_naast elkaar_ te zetten? Dan kan je Flexbox gebruiken. Naast de mogelijkheid om elementen naast elkaar te zetten,
krijg je ook de mogelijkheid om de uitlijning van de elementen te bepalen. Kijk maar eens naar het volgende voorbeeld:

<img src="minipuzzels/flexbox/images/Minipuzzel2.png" alt="Voorbeeld Flexbox" title="Voorbeeld Flexbox" width="1012">

<br>
Met slechts 4 regels code van Flexbox krijg je het eindresultaat dat de drie elementen naast elkaar staan, dat er een ruimte tussen de elementen zit, dat ze als geheel de hele breedte vullen en dat element 1 dubbel zo groot is als element 2 en 3. Maar het volgende is bijvoorbeeld ook mogelijk:
<br><br>

<img src="minipuzzels/flexbox/images/Minipuzzel3.png" alt="Voorbeeld Flexbox" title="Voorbeeld Flexbox" width="1012">

<br>
Om dit eindresultaat te krijgen heb je zelfs maar 3 regels code van Flexbox nodig. Hopelijk krijg je hiermee al een eerste indruk wat de kracht van Flexbox is en dat je met weinig code totaal andere layouts kan maken dan je tot nu toe hebt gedaan.
<br>
Het is met Flexbox trouwens ook mogelijk om elementen weer onder elkaar te zetten met alle opties tot uitlijnen zoals je net hebt gelezen.

<br><br>

> Naast Flexbox heb je ook nog Grid. Deze techniek staat ook in de Expert-kolom in het beoordelingsmodel. Wil je hier
> meer over weten? Zie de [hulpbronnen bij de eindopdracht](../eindopdracht/).

<br>

## Parent/child

Zoals gezegd kan je met een paar regels code al veel voor elkaar krijgen met Flexbox, maar je moet wel eerst weten hoe
het werkt. Het begint met in de CSS een HTML-tag instellen als Flexbox. Al zijn directe _children_ kunnen vervolgens
naar wens worden ingesteld met de Flexbox-opties. Zie de afbeelding hieronder. Links in de afbeelding zie je de code
die we voor dit voorbeeld gebruiken: de `<main>` met daarin drie keer een `<section>`. In HTML-termen spreken we er nu
van dat de `<main>` de _parent_ is en de drie keer `<section>` die erin staan de _children_. Aan de rechterkant van
onderstaande afbeelding zie je deze parent/child relatie ook nog eens met kleuren uitgebeeld.

> De termen _parent_ en _children_ komen vaak terug bij HTML, dus onthoud ze goed!

<img src="./images/flex-parent-children.jpg" alt="Flex parent children" title="Flex parent children" width="1012">

## Flexbox in een Flexbox

Let erop dat in bovenstaand voorbeeld alleen de `<main>` een Flexbox is en dus alleen de drie children kunnen worden
vormgegeven met Flexbox. Dus stel, in de tweede `<section>` staat ook inhoud die je met Flexbox wil vormgeven, dan stel
je die `<section>` ook simpelweg in als Flexbox en dan heb je ook weer alle mogelijkheden. Zo krijg je dus een Flexbox,
in een Flexbox, in een Flexbox, etc. Dit is goed! We raden aan om zoveel mogelijk Flexbox te gebruiken om jouw layout
te bepalen.

<br>

## Meest gebruikte Flexbox-opties

De Flexbox-opties zijn in te delen in twee categorieën: _parent-opties_ en _child-opties_. Zoals de naam al verraadt
stel je de parent-opties in op de parent en heeft invloed op **alle** children. De child-opties stel je op de children
zelf in en heeft alleen invloed op de children waarop je het instelt.

<br>

**Flexbox-opties parent**

| Optie           | Omschrijving                                                                                                                               | Voorbeeld                                                                           |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------- |
| display: flex;  | Hiermee stel je een HTML-tag in als Flexbox.                                                                                               | display: flex;                                                                      |
| flex-direction  | Instellen of de children in een rij of kolom getoond moeten worden.                                                                        | flex-direction: column;<br><img src="./images/flex-direction.svg" width="300">      |
| justify-content | Bepaalt de uitlijning op de hoofdas (dus de richting die gekozen is bij `flex-direction`).                                                 | justify-content: center;<br><img src="./images/justify-content.svg" width="300">    |
| align-items     | Bepaalt de uitlijning op de dwars-as (dus het tegenovergestelde van wat gekozen is bij `flex-direction`).                                  | align-items: flex-end;<br><img src="./images/align-items.svg" width="300">          |
| flex-wrap       | Bepaalt of de Flexbox op één rij moet blijven, of zich mag verdelen over meerdere rijen.                                                   | flex-wrap: wrap;<br><img src="./images/flex-wrap.svg" width="300">                  |
| align-content   | Wanneer flex-wrap op `wrap` staat en de content valt over meerdere rijen, is met deze optie de uitlijning tussen deze rijen in te stellen. | align-content: space-between;<br><img src="./images/align-content.svg" width="300"> |
| gap             | Bepaalt de ruimte tussen de children.                                                                                                      | gap: 20px;<br><img src="./images/gap.svg" width="300">                              |

<br>

**Flexbox-opties child**

| Optie       | Omschrijving                                                                                             |                                                                          |
| ----------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| flex-grow   | Bepaalt hoeveel deze child mag groeien t.o.v. de andere children.                                        | flex-grow: 2;<br><img src="./images/flex-grow.svg" width="300">          |
| flex-shrink | Bepaalt hoeveel deze child mag krimpen t.o.v. de andere children.                                        | flex-shrink: 1;                                                          |
| flex-basis  | Bepaalt de standaardgrootte van de child voordat de resterende ruimte wordt verdeeld.                    | flex-basis: 200px;                                                       |
| flex        | Dit is de shorthand-notatie van bovenstaande drie opties. **Het wordt aangeraden om deze te gebruiken.** | flex: 1;                                                                 |
| align-self  | Deze optie werkt hetzelfde als align-items, maar wordt hier alleen toegepast op het specifieke child.    | align-self: flex-end;<br><img src="./images/align-self.svg" width="300"> |

Voor het volledige overzicht,
[zie deze documentatie](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flexbox-properties).

<br>

## Flexbox-inspector 🔍

Om erachter te komen wat er allemaal mogelijk is met Flexbox gebruik je de `inspector`. Hierin kun je namelijk met
simpelweg drukken op knopjes veel parent-opties uitproberen. Inspecteer een HTML-tag die staat ingesteld als Flexbox en
klik rechts van `display: flex` op het Flexbox-knopje. Voor meer info, bekijk de volgende video:
[https://developer.chrome.com/docs/devtools/css/flexbox/](https://developer.chrome.com/docs/devtools/css/flexbox/)

<img src="./images/flex-inspector.png" alt="Flexbox inspector" title="Flexbox inspector" width="300">

<br>

> Reminder: je opent de inspector door met de rechter muistoets op een specifiek HTML-element te klikken en vervolgens
> op **Inspecteren**, óf met de sneltoets ⌥⌘i op Mac en F12 op Windows.

<br>

## Hulpbronnen voor Flexbox

- [Flexbox basics cheatsheet](./images/flex-cheatsheet.pdf)<br>![Flexbox cheatsheet](./images/flex-cheatsheet.png)
- [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Video: CSS Flexbox in 100 Seconds](https://www.youtube.com/watch?v=K74l26pE4YA)
- [Video waarin flex-grow, flex-shrink en flex-basis wordt uitgelegd met voorbeelden](https://www.youtube.com/watch?v=CFgeJq4l1YM)

<br><br> **Klaar met het hoofdstuk over Flexbox?** <br>
[Klik dan hier om naar de minipuzzels over Flexbox te gaan.](minipuzzels/flexbox/)

<br><hr><br>

# Minipuzzels - Flexbox

[Klik hier om naar de minipuzzels over Flexbox te gaan.](minipuzzels/flexbox/)

<br><hr><br>

# Opdracht 1: Foodblog genereren met AI

In deze opdracht ga je GitHub Copilot (of een vergelijkbare AI-assistent) in Visual Studio Code gebruiken om de
Foodblog opdracht te maken. Dit is een kans om te ervaren hoe AI-tools kunnen helpen bij het ontwikkelen van
webpagina's.

## Doel

- Kennismaken met code-generatie via AI
- Leren effectieve prompts te schrijven
- Kritisch beoordelen van AI-gegenereerde code

## Aanpak

1. **Voorbereiding**: Maak in het project `frontend-development` (die je in
   [les 1](../les1#opdracht-1c---eerste-project-aanmaken) hebt aangemaakt) een nieuwe map genaamd `les3` en daarin weer
   een map genaamd `foodblog-ai`. Zet hierin de
   [standaard bestandsstructuur](../les1#opdracht-1d---bestandsstructuur-html-en-css) klaar. Deze opdracht bevat 2
   pagina's, dus maak ook het bestand `details.html` aan, deze dient als losse pagina.

2. **Doel**: Het ontwerp van [opdracht 2](#opdracht-2-foodblog) zoveel mogelijk nabouwen met AI.
3. **Agent openen**: In Visual Studio Code zit Copilot; een AI-tool die jou op meerdere manieren kan helpen. Open
   copilot en stel hem in op `Agent`. Op die manier zal copilot met je "meedenken" over wat de beste oplossing is.

4. **Experimenteer met prompts**: Beschrijf wat je wilt bereiken en kijk wat de AI genereert. Probeer verschillende
   benaderingen om te zien wat het beste werkt. Niet het gewenste resultaat? Schrijf meerdere prompts om het bij te
   sturen of begin simpelweg helemaal opnieuw met een andere benadering. Experimenteer er vooral op los!

## Quiz

Wanneer je tevreden bent met het gegenereerde resultaat is het tijd om te achterhalen in hoeverre je de code ook
begrijpt. AI kan je zien als hulpje die je helpt met code sneller schrijven, maar jij, als expert, moet altijd weten
wat er zich onder de motorkap afspeelt.

Je gaat twee quizzen over de HTML en over CSS. Open in copilot een nieuwe chat, stel deze in op `Ask` en voer de
volgende prompt uit en maak de quiz.

### HTML

```
Creëer een interactieve quiz over HTML voor beginners met 10 vragen op basis van de code. De quiz moet uitsluitend gaan over HTML-semantiek (zoals gebruik van semantische tags zoals header, section, nav, article, etc.) van de homepage en detailpagina van de foodblog. Geen vragen over toegankelijkheid (aria-attributen), CSS of JavaScript. Wissel de volgende type vragen evenredig af:

- Jij stelt een vraag en ik moet het juiste stukje code selecteren, waarna ik het woord "check" stuur en jij moet checken of ik het juiste stukje code heb geselecteerd (laat hierbij nooit een code snippet zien).
- Open vragen over semantische HTML-elementen en hun doel (laat hierbij altijd de code snippet zien waar de vraag over gaat)
- Multiple choice (a, b, c, d) over correct gebruik van semantische HTML (laat hierbij altijd de code snippet zien waar de vraag over gaat)

Na elk antwoord van mij:

- Geef aan of het antwoord juist of onjuist is.
- Is het juist? Geef positieve feedback en ga automatisch door naar de volgende vraag.
- Is het onjuist? Geef géén goed antwoord. Geef wél een nuttige hint, en vraag me opnieuw te antwoorden. Blijf wachten op mijn verbeterde antwoord.

Belangrijke regels:

- Stel steeds slechts één vraag tegelijk.
- Stel steeds slechts één vraag tegelijk.
- Je bent in deze chat geen code expert, maar een quiz master, gedraag je daar dus ook naar
- Geef nooit het juiste antwoord bij een fout antwoord.
- Wacht altijd op mijn input na een onjuist antwoord.
- Herhaal de oorspronkelijke vraag als dat helpt.
- Geef bij elke vraag aan welk nummer het is (bijv. "Vraag 3/10").
- De quiz moet in het Nederlands zijn.
- Toon aan het einde mijn totaalscore.

Stel nu de eerste vraag.
```

### CSS

```
...
```

<br><hr><br>

# Opdracht 2: Foodblog

In de vorige opdracht heb je de foodblog gegenereert en geleerd waar AI toe in staat is, maar ook dat het belangrijk is
dat je zelf weet wat er zich onder de motorkap afspeelt. Daarom ga je de foodblog nogmaals maken, maar dan volledig met
de hand, zodat je goed leert hoe je o.a. Flexbox moet toepassen.

Download de startcode als je dat nog niet had gedaan
([zie Brightspace](https://brightspace.hr.nl/d2l/le/lessons/110777/lessons/442865)) en bouw vervolgens het volgende
ontwerp na _(klik op de afbeelding om te vergroten)_.

Let op, het gaat om twee pagina's: de homepage met recepten en de detailpagina van een recept. Wanneer er op de
homepage wordt geklikt op **Bekijk recept** moet er dus naar de detailpagina worden genavigeerd. <br> De
receptomschrijving op de detailpagina moet een échte lijst zijn. Gebruik hiervoor de tag `<ol>`.

Ook hierbij geldt weer: wanneer er een handje op een linkje wordt getoond, dan wordt de hover-state getoond.

Voor deze opdracht heb je de volgende kleurcodes nodig:

| Hex       | RGB                  |
| --------- | -------------------- |
| `#000000` | `rgb(0,0,0)`         |
| `#FFFFFF` | `rgb(255,255,255)`   |
| `#457B9D` | `rgb(69,123,157)`    |
| `#A0ABC0` | `rgb(160, 171, 192)` |

<br>

**Homepage** <br> <img src="./images/Opdracht1-home.png" alt="Opdracht 1" title="Opdracht 1" width="1012">

<br>

**Detailpagina recept** <br> <img src="./images/Opdracht1-detail.png" alt="Opdracht 1" title="Opdracht 1" width="1012">

<br>

## Advanced opdracht

Als je wat extra uitdaging wilt, dan kan je ook onderstaande wireframe nabouwen. Hierin zitten extra elementen die je
door zelfstudie moet zien te achterhalen. De afbeeldingen zijn te vinden in de startcode
([zie Brightspace](https://brightspace.hr.nl/d2l/le/lessons/110777/lessons/442865)). Je mag de startcode gebruiken,
maar je mag ook alles zelf maken.

Let op, ook bij deze opdracht gaat het om twee pagina's: de homepage met recepten en de detailpagina van een recept. De
detailpagina is dezelfde als bij de reguliere opdracht, maar hij staat ook hieronder nog weergegeven. Wanneer er op de
homepage wordt geklikt op **Bekijk recept** moet er dus naar de detailpagina worden genavigeerd

Zorg er tot slot ook voor dat de knoppen **Bekijk recept** netjes tegen de onderkant uitlijnen, zoals ook in het
ontwerp te zien is.

<br>

**Homepage advanced** <br> <img src="./images/Opdracht1-advanced.png" alt="Opdracht 1" title="Opdracht 1" width="1012">

**Detailpagina recept** <br> <img src="./images/Opdracht1-detail.png" alt="Opdracht 1" title="Opdracht 1" width="1012">
