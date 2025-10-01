# Les 8

**Inhoudsopgave**

- [Les 8](#les-8)
  - [Leerdoelen](#leerdoelen)
- [Opdracht 1: Foodblog genereren met AI](#opdracht-1-foodblog-genereren-met-ai)
  - [Doel](#doel)
  - [Aanpak](#aanpak)
  - [Quiz](#quiz)
    - [HTML](#html)
    - [CSS](#css)
- [Eindopdracht](#eindopdracht)

<br><br><br>

## Leerdoelen

In deze les ligt de focus op het volgende leerdoel:

| Leerdoel                                                                                                                                | Toelichting                                                           |
| --------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| 4. Ik kan uitleggen hoe AI-tools het leerproces kunnen ondersteunen en kan de kwaliteit van de gegenereerde output kritisch beoordelen. | In deze les leer je hoe je gegenereerde code kritisch kan beoordelen. |

<br>

Alle leerdoelen zijn terug te vinden in de
[cursushandleiding op Brightspace](https://brightspace.hr.nl/d2l/le/lessons/192811/units/824025) <br><br><br>

# Opdracht 1: Foodblog genereren met AI

In deze opdracht ga je GitHub Copilot (of een vergelijkbare AI-assistent) in Visual Studio Code gebruiken om de
Foodblog opdracht te maken. Dit is een kans om te ervaren hoe AI-tools kunnen helpen bij het ontwikkelen van
webpagina's.

## Doel

- Kennismaken met code-generatie via AI
- Leren effectieve prompts te schrijven
- Kritisch beoordelen van AI-gegenereerde code

## Aanpak

1. **Voorbereiding**: Open een nieuw project in Visual Studio Code. Zet hierin eventueel de
   [standaard bestandsstructuur](../les1#opdracht-1f---bestandsstructuur-html-en-css) klaar, maar Copilot kan dit ook
   voor je doen (alleen dan is het waarschijnlijk niet naar wens).

2. **Doel**: Het ontwerp van de homepage van [opdracht 2 van les 3](../les3/README.md#opdracht-2-foodblog) zoveel
   mogelijk nabouwen met AI.
3. **Agent openen**: Tot nu toe heb je Copilot in Visual Studio Code gebruikt in de `ask` modus (oftewel, de
   vraag-modus). Je kan echter ook voor `edit` of `agent` kiezen. Met `edit` kun je code selecteren en vragen om
   wijzigingen, waarna Copilot de code direct aanpast. De `agent` modus is de meest geavanceerde. Deze probeert zelf te
   beredeneren wat de beste stappen zijn om te nemen, evalueert dit ook en kan vervolgvragen aan jou stellen. Op die
   manier zal copilot met je "meedenken" over wat de beste oplossing is. 🤯 Een `agent` kan ook rechtstreeks in je code
   typen! Stel Copilot voor deze opdracht in op `agent`.

4. **Experimenteer met prompts**: Beschrijf wat je wilt bereiken en kijk wat de AI genereert. Probeer verschillende
   benaderingen om te zien wat het beste werkt. Niet het gewenste resultaat? Schrijf meerdere prompts om het bij te
   sturen of begin simpelweg helemaal opnieuw met een andere benadering. Open als je opnieuw begint wel een nieuwe chat
   door bovenin op het plusje te klikken, zodat Copilot ook met een frisse start begint. Experimenteer er vooral op
   los!

## Quiz

Wanneer je tevreden bent met het gegenereerde resultaat is het tijd om te achterhalen in hoeverre je de code ook
begrijpt. AI kan je zien als hulpje die je helpt met code sneller schrijven, maar jij, als expert, moet altijd weten
wat er zich onder de motorkap afspeelt.

Je gaat twee quizzen over de HTML en over CSS. Open in copilot een nieuwe chat, stel deze in op `Ask` en voer de
volgende prompt uit en maak de quiz. Copilot gedraagt zich dan als quizmaster en zal jou vragen stellen over de code
die is gegenereert.

🏴‍☠️ Fun tip: wil je dat de quiz master een piraat is? Voeg dan de volgende regel toe aan de belangrijke regels:
`Spreek altijd met een piraten-accent.`, of ga voor `gollum`, `yoda` of `shakespeare`

> ⚠️ Disclaimer: Onderstaande prompt geeft geen zekerheid op een correctie quiz. Iedere AI-tool en ieder model wat
> daarin gebruikt wordt zal hier weer anders mee omgaan. Mocht je iets geks zien, geef dit dan aan bij jouw docent,
> zodat deze prompt verfijnd kan worden.

### HTML

```
Creëer een interactieve quiz over HTML voor beginners met 10 vragen op basis van de code. De quiz moet uitsluitend over HTML-semantiek gaan (zoals gebruik van semantische tags zoals header, section, nav, article, etc.). Geen vragen over toegankelijkheid (aria-attributen), CSS of JavaScript. Wissel de volgende type vragen evenredig af:

- Jij stelt een vraag en ik moet het juiste stukje code selecteren, waarna ik het woord "check" stuur en jij moet checken of ik het juiste stukje code heb geselecteerd (laat hierbij nooit een code snippet zien).
- Open vragen over semantische HTML-elementen en hun doel (laat hierbij altijd de code snippet zien waar de vraag over gaat)
- Multiple choice (a, b, c, d) over correct gebruik van semantische HTML (laat hierbij altijd de code snippet zien waar de vraag over gaat)

Na elk antwoord van mij:

- Geef aan of het antwoord juist of onjuist is.
- Is het juist? Geef positieve feedback en ga automatisch door naar de volgende vraag.
- Is het onjuist? Geef géén goed antwoord. Geef wél een nuttige hint, en vraag me opnieuw te antwoorden. Blijf wachten op mijn verbeterde antwoord.

Belangrijke regels:

- Stel steeds slechts één vraag tegelijk.
- Stel in een vraag nooit meerdere subvragen.
- Check bij een multiple choice vraag of er slechts 1 antwoord is gegeven (bijvoorbeeld: de gebruiker mag niet a, b, c, d invoeren, keur dit af)
- Je bent in deze chat geen code expert, maar een quiz master, gedraag je daar dus ook naar
- Geef nooit uitleg of code buiten de quiz-context.
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
Creëer een interactieve quiz over CSS voor beginners met 10 vragen op basis van de code. De quiz moet uitsluitend over de volgende CSS onderwerpen gaan: selector, Flexbox, responsiveness, transitions en animations. Andere onderwerpen, zoals Grid, mogen niet worden gebruikt. Wissel de volgende type vragen evenredig af:

- Jij stelt een vraag en ik moet het juiste stukje code selecteren, waarna ik het woord "check" stuur en jij moet checken of ik het juiste stukje code heb geselecteerd (laat hierbij nooit een code snippet zien).
- Open vragen (laat hierbij altijd de code snippet zien waar de vraag over gaat)
- Multiple choice (a, b, c, d) over correct gebruik van CSS (laat hierbij altijd de code snippet zien waar de vraag over gaat)

Na elk antwoord van mij:

- Geef aan of het antwoord juist of onjuist is.
- Is het juist? Geef positieve feedback en ga automatisch door naar de volgende vraag.
- Is het onjuist? Geef géén goed antwoord. Geef wél een nuttige hint, en vraag me opnieuw te antwoorden. Blijf wachten op mijn verbeterde antwoord.

Belangrijke regels:

- Stel steeds slechts één vraag tegelijk.
- Stel in een vraag nooit meerdere subvragen.
- Check bij een multiple choice vraag of er slechts 1 antwoord is gegeven (bijvoorbeeld: de gebruiker mag niet a, b, c, d invoeren, keur dit af)- Je bent in deze chat geen code expert, maar een quiz master, gedraag je daar dus ook naar
- Geef nooit uitleg of code buiten de quiz-context.
- Geef nooit het juiste antwoord bij een fout antwoord.
- Wacht altijd op mijn input na een onjuist antwoord.
- Herhaal de oorspronkelijke vraag als dat helpt.
- Geef bij elke vraag aan welk nummer het is (bijv. "Vraag 3/10").
- De quiz moet in het Nederlands zijn.
- Toon aan het einde mijn totaalscore.

Stel nu de eerste vraag.
```

<br><br><br>

# Eindopdracht

Je gaat nu je eindproduct afronden. Dit is een website over een fictief product.

Lees hiervoor de cursushandleiding aandachtig door en zie de pagina over de [eindopdracht](../eindopdracht).
