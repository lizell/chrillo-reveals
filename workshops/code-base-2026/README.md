# Code Base · Järvsö · 19 september 2026

**Kom igång med AI i utvecklingsarbetet – så här gjorde vi på SVT**  
Christian Lizell · Athega / SVT Nyheter & Sport

Färdig presentation i [slides/code-base-2026.md](../../slides/code-base-2026.md). PDF kan exporteras lokalt för visning utan webbläsarserver; den versionshanteras inte. 25 huvudbilder, 2 valbara introduktionsbilder om Christian och Athega, 7 vertikala casefördjupningar, 1 valbart botexempel, 11 begreppsbilder, 11 tipsbilder och 3 reservbilder (60 bilder totalt). Alla bilder har talarstöd med muntliga formuleringar, korta hållpunkter, övergångar och tidsangivelser. Källor och redaktionella avgränsningar finns i källdokumentet. Tid och rum är ännu inte fastställda enligt arrangörens underlag.

## Körschema

| Tid | Bilder | Innehåll |
| --- | --- | --- |
| 00–03 | 1–3 | Introduktion, handuppräckning och dagens löfte |
| 03–07 | 4 + tre bilder nedåt, därefter valbar demo | Ossy: från handskriven prototyp till produkt och botramverk |
| 07–11 | 5 + två bilder nedåt | Login: planer, exempelappar och samverkan mellan team |
| 11–15 | 6 + två bilder nedåt | Astrid: nytt arbetssätt i en etablerad kodbas i drift |
| 15–16 | 7 | Gemensamma lärdomar och brygga till första uppgiften |
| 16–22 | 8–13 | Uppgift, prompt, kontext och mandat |
| 22–25 | 14 | Parövning: granska ett kodförslag |
| 25–32 | 15–18 | Facit, feedback, review och när agenten fastnar |
| 32–34 | 19–21 | Första försöket på några timmar och direkt återkoppling |
| 34–37 | 22 | Parövning: formulera ert första försök |
| 37–40 | 23–24 | Fortsatt lärande och avslutning |
| 40–45 | 25 | Frågor |
| Vid behov | 26–28 | Reserv: äldre kod, genvägar till fördjupningar och källor |

Bildnummer i tabellen avser **horisontella positioner**. Räknaren i presentationen och sidnumren i PDF räknar även de 32 vertikala bilderna. Caseöversikterna ligger på PDF-sidorna 6 (Ossy), 11 (Login) och 14 (Astrid).

45 minuter är normalversionen. Frågorna ingår. 50 minuter är arrangörens absoluta max, inte planerad speltid.

## Två fördjupningar att välja ur

- **Begrepp:** under huvudbild 8, ”Ge agenten ett jobb som går att avsluta”, `#/7/1`. Elva bilder: modell/agent, beställning, kontext, instruktioner/skills, setup/MCP, effort/autonomi, Git/leverans, kvalitet, startlägen, förkortningar samt retrieval/RAG och innehåll.
- **Tips och tricks:** under huvudbild 23, ”Gör lärandet gemensamt”, `#/22/1`. Elva bilder: första försöket, feedback, regler, beständiga planer, ny kontext, modellval, verktyg, parallellt arbete, förbättring av setup, delat lärande och kunddialog.
- [Skriftlig fördjupning](fordjupning.md) för läsning efter passet.

Dessa 22 bilder är uppslagsmaterial, inte ett nytt obligatoriskt block. I 45-minuterspasset: välj vid behov en eller två under frågetiden eller byt ut motsvarande talartid. Kör inte hela vertikalspåren utöver körschemat. Högerpil hoppar över ett spår; mellanslag går igenom alla dess bilder. Reservbilden ”Begrepp eller praktiska tips?” har klickbara genvägar. `O` visar alla bilder.

Precio Fishbone-kopplingen finns i huvudspåret genom nyutveckling, integration, CMS och förvaltning. Övningen utgår från en liten uppgift i deltagarnas uppdrag. Tipsdelen tar också upp delat lärande och hur arbetssättet kan förklaras för en kund.

## Anpassa under passet

Frågor under tiden är välkomna. Ta korta frågor direkt och parkera längre deep dives till frågebilden. Normalversionens tolv minuter för casen inkluderar de sju fördjupningarna. Ossy: 45 sekunders översikt, en minut om resan, en minut om arbetsloopen och 1 min 15 sek om ramverket. Login och Astrid: en minut per översikt och 1,5 minut per fördjupning. Dialora-exemplet är valbar: ta då 45 sekunder från ramverksbilden, så att Ossy-blocket fortfarande slutar vid minut 7. Teamets första försök och uppföljningen är ett kort block på två minuter – läs inte all forskningsbakgrund i anteckningarna högt.

Om frågor tar fem minuter extra: korta varje case till två minuter genom att stanna på översikten och berätta dess viktigaste händelse och lärdom muntligt. Det sparar sex minuter och behåller alla tre berättelserna. Tryck högerpil för att hoppa till nästa case. Behåll övningarnas facit och fem minuter till frågor. Stanna på frågebilden; reservbilderna är inte ett extra block.

Övningarna fungerar utan datorer, konton och nät. Vid stort rum: samtala med grannen och ta två svar, utan att skicka runt mikrofon länge. Vid litet rum: samla två muntliga exempel. Inget behöver lämnas in.

## Starta och visa

```bash
npm run dev
```

Välj `code-base-2026.md` på indexsidan. Använd **högerpil** för nästa huvudbild. På casebilderna, huvudbild 8 och huvudbild 23 går **nedåtpil** till fördjupningarna och **uppåtpil** tillbaka. Högerpil från en fördjupning går till nästa huvudbild. Mellanslag följer hela ordningen inklusive fördjupningarna. `O` visar översikten, `F` ger helskärm och `S` öppnar talarvyn med anteckningar och timer.

För lokal statisk visning:

```bash
npm run build
python3 -m http.server 8000 --directory docs
```

Öppna http://localhost:8000/code-base-2026.html. Kör via HTTP även utan nät; talarvyn använder ett separat fönster. Tillåt popup-fönstret och öppna det före passet. Casebilderna innehåller lokala skärmbilder från Login och Astrid samt ett 19 sekunder långt Ossy-klipp utan ljud. Klippet startar automatiskt utan ljud när Ossy-bilden visas och pausas när du går vidare. Det är inräknat i Ossy-introduktionens 45 sekunder. Om webbläsaren blockerar automatisk start finns playknappen kvar. Klicka på skärmbilderna för att öppna dem i full storlek. PDF visar en stillbild från klippet. Fem diagram förklarar resan, arbetsloopen, det gemensamma inloggningsflödet, en liten ändring i befintlig kod och förbättringen av setupen.

Det valbara Dialora-exemplet under Ossy är en lokal skärmbild som visas även i PDF. Alla casebilder och Ossy-klippet fungerar utan nät via den lokala servern. Behåll hela `docs/assets/` vid kopiering av den statiska presentationen. Källänkarna kräver nät om de ska öppnas. Det gemensamma temat försöker ladda ett externt typsnitt, men detta deck använder lokala reservtypsnitt och fungerar utan det.

PDF kan exporteras från Chromium/Chrome: öppna samma adress med `?print-pdf`, skriv ut till PDF i liggande format utan sidhuvud/sidfot och med bakgrundsgrafik. PDF är publikens bilder; talaranteckningarna finns i Markdown och talarvyn.

## Material att använda

[Deltagarbladet](deltagarblad.md) innehåller en kopierbar uppgift, promptar och reviewfrågor. Det kan delas som Markdown eller skrivas ut från en Markdown-läsare. [Källkartan](kallor.md) skiljer personlig erfarenhet från forskning och generella råd.

De tre SVT-casen bygger på Christians inspelade berättelse från den 10 september och tidigare material i repot. Källkartan anger tidsstämplar för respektive case. Berättelsen beskriver erfarenheter från projekten, utan påhittade mätningar eller effekter. Den genomgående sökuppgiften är fiktiv och märks som sådan. Inget kundnamn, systemnamn eller systemdetalj från andra uppdrag finns i det nya materialet.

## Verifiering

Statisk build genomförd. Casebilderna och de fem diagrammen har även granskats visuellt i skärmbilder från Chrome, inklusive radbrytningar, textavstånd och videons utskriftsbild. Samtliga 60 bilder kontrollerade i Chrome utan innehåll utanför bildytan och utan JavaScript-fel. Lokal videouppspelning, bilder, horisontell och vertikal pilnavigering, översiktsläge och talarvyns visning av rätt anteckningar kontrollerade. PDF exporterad från samma statiska presentation. Uppdatera PDF-filen efter framtida innehållsändringar; den ingår inte i `npm run build`.
