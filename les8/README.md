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

| Leerdoel                                                                                                                                | Toelichting                   |
| --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------- |
| 4. Ik kan uitleggen hoe AI-tools het leerproces kunnen ondersteunen en kan de kwaliteit van de gegenereerde output kritisch beoordelen. | In deze les leer je ... @TODO |

<br>

Alle leerdoelen zijn terug te vinden in de [cursushandleiding](https://brightspace.hr.nl/d2l/home/192811) @TODO: juiste
link invoeren.

<br><br><br>

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
   [les 1](../les1#opdracht-1d---eerste-project-aanmaken) hebt aangemaakt) een nieuwe map genaamd `les3` en daarin weer
   een map genaamd `foodblog-ai`. Zet hierin de
   [standaard bestandsstructuur](../les1#opdracht-1e---bestandsstructuur-html-en-css) klaar. Deze opdracht bevat 2
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

<br><br><br>

# Eindopdracht

Je gaat nu je eindproduct afronden. Dit is een website over een fictief product.

Lees hiervoor de cursushandleiding aandachtig door en zie de pagina over de [eindopdracht](../eindopdracht).
