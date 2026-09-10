# Från första prompt till trygg leverans

Code Base · Järvsö · 19 september 2026 · Christian Lizell

## Mitt första försök

- **Uppgiften:** På måndag provar vi AI för att …
- **Ägaren och reviewern:** …
- **Agentens scope:** Den får ändra …
- **Klart när:** Vi har sett eller testat …
- **Uppföljning:** Direkt efter försöket tar vi fem minuter för att …

Välj en uppgift i ert uppdrag, till exempel ett CMS-flöde, en integration eller en förvaltningsbugg, som ni äger, förstår och kan kontrollera på några timmar, högst en dag inklusive test och review. Om uppgiften växer: bryt ut en mindre del. Använd ett godkänt verktyg och den kod och data som teamets regler tillåter. Börja i en separat gren eller isolerad arbetskopia.

## Tre case att jämföra med er situation

| Startläge | Erfarenhet från passet | Något att prova |
| --- | --- | --- |
| Ossy: ny produkt | Processen växte fram från handskriven prototyp till helt AI-driven utveckling och ett återanvändbart botramverk. | Bygg återkopplingen samtidigt som första fungerande flödet. |
| Login: omskrivning med många beroenden | Planer och exempelappar gav flera team ett konkret underlag att diskutera. Produktionsstart: 9 september 2026. | Spara planen i repo och gör en liten prototyp att prova tillsammans. |
| Astrid: befintligt system i drift | Agenten behövde följa kodbasens regler och få uppgifter som växte stegvis. | Ge relevant kontext och börja med en avgränsad ändring. |

Casen är Christians projekterfarenheter. Förslagen i sista kolumnen är arbetssätt att anpassa till ert team.

Ett exempel från Ossy-ramverket är Dialora, som hjälper till med frågor om SVT:s program och tjänster. Presentationen visar en skärmbild.

## En enkel brief

```text
Mål: [observerbart beteende för användaren]
Kontext: [reproduktion, relevanta filer och befintligt exempel]
Scope: [var ändringen får ske och vad som inte ingår]
Klart när: [beteenden, gränsfall och hur de verifieras]
Mandat: [läsa/föreslå eller ändra/testa inom scope]
Leverera: diff, faktiska kontrollresultat och återstående osäkerhet.
```

### Exemplet från presentationen – fiktivt

```text
Mål: Tom eller blank sökning ska visa ”Skriv ett sökord”
och inte anropa API:t. Övriga sökord skickas oförändrade.

Läs sökflödet och relevanta tester. Ändra inget ännu.
Peka ut berörda filer och föreslå minsta ändring.
Lista antaganden och hur beteendet kan verifieras.
Scope: sökvalidering och tester; inga nya beroenden.
```

När du har bedömt planen:

```text
Implementera planen inom avgränsningen.
Visa med tester att tom/blank input inte anropar API:t,
att vanliga sökningar fungerar och att ” skog ” skickas oförändrat.
Kontrollera att felmeddelandet syns i användarflödet.
Kör relevanta kontroller enligt repots instruktioner.
Visa diff, vad du faktiskt körde och vad du inte kunde verifiera.
```

### Ge användbar feedback

```text
Förslaget missar strängar med enbart blanktecken.
Lägg till ett test som fallerar för ”   ” med nuvarande kod.
Rätta valideringen och visa att API:t inte anropas.
Verifiera även att ” skog ” skickas oförändrat.
Kör relevanta tester och redovisa resultaten.
```

## Review innan acceptans

- **Rätt sak:** matchar beteendet målet, inklusive fel- och gränsfall?
- **Rimlig ändring:** håller diffen scope och följer den befintliga mönster?
- **Bevis:** vilka tester kördes, vad upptäcker de, och vad är fortfarande okontrollerat?
- **Ansvar:** kan en människa förklara ändringen och besluta om release?
- **Efteråt:** hur upptäcker och backar ni en felaktig förändring?

AI-review kan ge fler hypoteser att undersöka. Mänsklig förståelse och acceptans behövs fortfarande. Granska också ändrade eller borttagna tester. Se [GitHubs reviewvägledning](https://docs.github.com/en/copilot/tutorials/review-ai-generated-code).

### Facit till kodövningen

`!query` fångar den tomma strängen men inte en sträng med mellanslag. Om indata enligt kontraktet alltid är en sträng kan `query.trim().length === 0` användas som vakt. Skicka sedan det ursprungliga sökordet till API:t om det inte är blankt. Testa både noll API-anrop och synligt meddelande för blank input. Om kontraktet tillåter andra typer måste de fallen beslutas och hanteras uttryckligen.

## När agenten fastnar

Stanna och kontrollera grundantagandet. Isolera ett fel, minska uppgiften och ange vilket bevis som saknas. Spara kort vad som är känt, vad som provats och nästa steg; starta ny kontext vid behov. Ta över manuellt när det hjälper. Vid större arbete: spara plan och beslut i repo och håll dem uppdaterade.

## Stäm av direkt – fem minuter

Titta på ändringen tillsammans direkt efter försöket. Vad hjälpte? Vad blev fel? Vad provar ni härnäst? Bestäm en sak att behålla och en sak att ändra till nästa lilla uppgift.

## Fortsätt lära tillsammans

Dela fungerande exempel och misslyckanden med teamet. Följ tid inklusive review och omarbete, fel efter release och hur väl ni kan förklara resultatet. Jämför liknande uppgifter och anteckna skillnader; enstaka försök bevisar inte en generell produktivitetsökning.

DORA beskriver AI som en förstärkare av organisationens befintliga styrkor och svagheter: [DORA 2025](https://dora.dev/research/2025/dora-report/).

Mer stöd finns i [begreppsguiden och tipsen](fordjupning.md), inklusive förbättring av setup, delat lärande och kunddialog.
