# Från första prompt till trygg leverans

## Hur vi kommer igång med AI-driven utveckling — utan att tappa kvalitet, omdöme eller fart

**Format:** 45–50 minuter inklusive kort frågestund  
**Målgrupp:** Utvecklare, tech leads och ledare

## Huvudbudskap

Det viktigaste är att sänka tröskeln för att komma igång. Inte att bygga den mest sofistikerade AI-miljön. Börja använda AI i verkligt arbete, lär er vad som fungerar i det egna teamet och bygg först därefter den struktur som faktiskt behövs.

> Det är bara att börja — med en riktig uppgift, en tydlig avgränsning och en bra review. Sedan tar man det därifrån.

Alla team jobbar olika. Ett bra arbetssätt ska därför inte standardisera bort omdöme eller verktygspreferenser, utan ge en gemensam miniminivå för kvalitet, säkerhet och lärande.

## Utgångspunkt

Ett kundnära AI-tema som *The Harness* handlar om gemensam kontext, beslutshistorik, varumärkeskunskap och data som gör organisationen bättre över tid.

Den här föreläsningen är det interna komplementet:

> En utvecklingsorganisation behöver också en harness: tydliga mål, kodbas-kunskap, små förändringar, feedbackloopar och skyddsnät.

Den centrala tesen:

> AI accelererar varje steg. Människan äger riktning, risk och acceptans.

Använd bilden *Our development cycle* som öppningsbild. Den visar att agenten kan bidra vid prompt/spec, implementation, egenreview och PR-review — men att utvecklingsflödets ansvar fortfarande ligger hos människorna och teamet.

## Körschema

| Tid | Del | Kärnpoäng |
| ---: | --- | --- |
| 0–5 min | Öppning: bilden och tesen | AI är inte ett nytt steg i processen; den är en medarbetare genom hela den — och det ska vara lätt att prova. |
| Valbar, 3–5 min | Gemensamt språk och nivåer | Vad menar vi med modell, prompt, agent, skill och harness — och hur långt behöver man gå? |
| 5–12 min | Vinn skeptikern | Ta rädslorna på allvar och visa vilka arbetssätt som behåller kontroll och kompetens. |
| 12–18 min | Fyra verkliga resor | Samma principer fungerar i mycket olika förutsättningar. |
| 18–25 min | Kom igång utan verktygskult | Börja litet och verkligt; bygg inte ett skillbibliotek, agentfarm eller en plattform först. |
| 20–30 min | Rätt autonomi för rätt uppgift | Modell, effort, scope och behörigheter ska matcha risk och reviewkapacitet. |
| 30–40 min | Review är den nya kärnkompetensen | AI gör output billigare; kvalitetssäkring och beslut blir flaskhalsen. |
| 40–46 min | En praktisk 90-dagarsstart | Ett upplägg som är rimligt för en organisation med flera utvecklingsteam. |
| 46–50 min | Tre principer och frågor | Lämna publiken med en konkret första åtgärd. |

## 1. Öppning: AI genom hela leveranscykeln (0–5 min)

Visa bilden.

> Förr använde vi verktyg för att skriva kod. Nu använder vi AI för att förstå problem, formulera lösningar, skriva kod, testa och granska.
>
> Det betyder inte att utvecklaren försvinner. Det betyder att utvecklarens ansvar flyttar uppåt: från att producera varje rad till att sätta riktning, skapa goda förutsättningar och avgöra vad som är tillräckligt bra.

Lägg till direkt efter:

> Det svåra är ofta inte att använda AI. Det svåra är att våga börja innan man känner att man har den perfekta setupen. Den behöver vi inte vänta på.

Ställ sedan frågan som passet besvarar:

> Om AI kan producera förändring snabbare än vi kan förstå den — hur bygger vi då utan att öka risk och teknisk skuld i samma takt?

## Valbar modul: gemensamt språk och nivåer (3–5 min)

Använd denna om publiken har blandad förkunskap. Den kan ligga direkt efter öppningen eller tas bort om tiden behövs till case och frågor.

### Några begrepp, utan jargong

| Begrepp | En enkel förklaring |
| --- | --- |
| **Modell** | Själva AI-motorn som läser, resonerar och genererar svar eller kod. |
| **Prompt** | Uppgiften och kontexten vi ger modellen. En bra prompt är ofta bara en tydlig arbetsbeskrivning. |
| **Effort** | Hur mycket tid/beräkning modellen får lägga på att resonera. Högre effort är inte samma sak som större mandat. |
| **Agent** | En modell som också kan använda verktyg, till exempel läsa filer, ändra kod och köra tester. |
| **Skill** | En återanvändbar instruktion för ett återkommande arbete, till exempel hur ett repo testas eller hur en viss typ av ändring görs. |
| **Harness** | Miljön runt AI:n: relevant kontext, regler, verktyg, tester och feedback som gör bra beteende lättare och säkrare. |

### AI är en stege, inte ett hopp

Visa gärna detta som en horisontell skala. Budskapet är: *alla behöver inte hamna längst till höger.*

| Nivå | Exempel | Vad människan gör | Risk och krav |
| ---: | --- | --- | --- |
| 0 | Google, dokumentation, Stack Overflow | Söker och sammanställer själv | Låg risk; källkritik behövs |
| 1 | Fråga i en AI-chatt | Tänker högt, ber om förklaringar, jämför alternativ | Låg risk; kontrollera fakta och antaganden |
| 2 | Hjälp i IDE:n | Skriver själv med förslag, kodförklaring och små kompletteringar | Låg–medel; läs alltid det som accepteras |
| 3 | Prompt till kodagent | Avgränsar uppgiften, granskar diffen och kör tester | Medel; tydligt scope och bra review krävs |
| 4 | Avgränsad automation | Sätter mål, ramar, behörighet, observability och rollback | Högre; bara för repetitiva och reversibla uppgifter |

Formulering att använda i talet:

> Mognad är inte att alltid använda nivå fyra. Mognad är att välja den lägsta nivå som löser uppgiften bra.

> Högre effort betyder att AI:n får tänka längre. Högre autonomi betyder att den får göra mer. De två ska inte höjas automatiskt tillsammans.

### Slide: förhåll dig till agenten som en kollega

Många använder AI som en bättre sökmotor och missar hur mycket hjälp den kan ge. En användbar mental modell är att skilja på att **fråga**, **samarbeta** och **delegera**.

| Läget | Exempel | Vad du behöver vara tydlig med |
| --- | --- | --- |
| **Fråga** | “Kan du ge mig en text jag kan mejla?” | Målgrupp, ton och budskap. Du tar själv nästa steg. |
| **Samarbeta** | “Läs den här statusen, ställ de frågor som saknas och skriv ett mejlförslag till mina peers.” | Kontext, mottagare, vad som är osäkert och vad du vill godkänna. |
| **Delegera** | “Uppdatera mina peers om nuläget: sammanfatta X, nämn Y, och skicka bara när jag har godkänt utkastet.” | Mål, ramar, mottagare, vilken handling som får utföras och när godkännande krävs. |

Poängen är inte att alltid gå längst ned. Det är att medvetet välja vilken relation du vill ha i uppgiften.

> Behandla agenten som en kompetent ny kollega: ge den sammanhang, ett tydligt mål, mandat som matchar risken och ett sätt att visa att arbetet blev rätt.

### En enkel brief, hellre än en “magisk prompt”

När en uppgift kräver mer än ett snabbt svar räcker ofta fem delar:

1. **Mål:** Vad ska bli bättre eller klart?
2. **Kontext:** Vad behöver agenten känna till för att inte gissa?
3. **Ramar:** Vad får den göra, och vad får den inte röra?
4. **Klart när:** Hur verifierar vi att resultatet är rätt?
5. **Mandat:** Ska den föreslå, förbereda eller utföra en handling?

Exempel för utveckling:

> Fixa felet där fakturor kan skapas utan kund. Börja med att hitta orsaken och föreslå en plan. Ändra bara validering och relevanta tester; ändra inte datamodellen. Kör de relevanta testerna och visa diffen för review innan du gör något mer.

En bra slutrad för sliden:

> Du behöver inte prompta smartare. Du behöver briefa tydligare.

## 2. Vinn skeptikern (5–12 min)

Det här ska inte vara en föreläsning som säger åt människor att sluta vara oroliga. Rädslorna är rimliga. Ett dåligt AI-införande kan leda till sämre kontroll, sämre lärande och sämre arbetsmiljö. Ta dem på allvar, och visa sedan hur arbetssättet adresserar dem.

| Oro | Ärligt svar | Praktik som minskar risken |
| --- | --- | --- |
| **“Kommer jag förlora jobbet?”** | Ingen talare kan ärligt lova att AI aldrig förändrar bemanning eller roller. Däremot är värdet av utvecklarens omdöme, domänkunskap och ansvar större när kod blir billigare att producera. | Fokusera på att göra fler människor kapabla att lösa fler kundproblem; mät värde och kvalitet, inte producerade rader kod. |
| **“Tappar vi kontrollen?”** | Ja, om agenten får stort scope utan insyn. Nej, om vi begränsar uppgift, behörighet och förändringsyta och har tydliga test- och reviewgrindar. | Små PR:er, reversibla ändringar, CI, mänsklig acceptans och tydligt ägarskap. |
| **“Blir vi dumma i huvudet?”** | Det är en verklig risk om AI används för att slippa förstå. AI ska vara en sparringpartner och producent, inte en ersättning för analys och lärande. | Be om förklaringar och alternativ, gör egen designbedömning, reviewa resultatet och behåll medveten träning i grundläggande teknik. |
| **“Måste jag byta hela mitt sätt att jobba?”** | Nej. Börja i det vanliga flödet och med den typ av uppgift du redan kan äga. | En liten uppgift, en agent, en ansvarig människa och samma vanliga PR-/testflöde. |

Formulering att använda i talet:

> Målet är inte att få människor att lita blint på AI. Målet är att göra dem bättre på att använda den kritiskt.

Microsoft Researchs CHI-studie om kunskapsarbete pekar på att hög tilltro till AI kan sammanfalla med mindre självrapporterad kritisk ansträngning. Det är inte ett skäl att förbjuda AI, men ett skäl att utforma arbetssätt där utvecklaren måste förstå och verifiera resultatet. [Microsoft Research: The Impact of Generative AI on Critical Thinking](https://www.microsoft.com/en-us/research/publication/the-impact-of-generative-ai-on-critical-thinking-self-reported-reductions-in-cognitive-effort-and-confidence-effects-from-a-survey-of-knowledge-workers/)

## 3. Fyra verkliga resor (12–18 min)

Presentera casen som fyra startlägen, inte som fyra säljpitchar.

| Case | Startläge | Vad AI möjliggör | Huvudlärdom |
| --- | --- | --- | --- |
| **Greenfield-produkt** | Helt AI-drivet från start | Snabbt bygga produkt, struktur, test och iteration | En ny kodbas kan formas agentvänlig från dag ett. |
| **Rewrite i etablerad miljö** | Nyutveckling i befintlig infrastruktur med många intressenter | Hålla fart i komplexitet och navigera etablerade beroenden | AI är särskilt stark när mandat, avgränsning och kontext är tydliga. |
| **Etablerat CMS** | Traditionellt utvecklat system som skiftar arbetssätt | AI blir en naturlig del av vardagen, inte ett sidoprojekt | Förändringen är i teamets vanor, inte bara i verktyget. |
| **Affärsnära backoffice** | Intern produkt med end-to-end-domän | Snabb prototyp till fungerande intern produkt | Den som förstår verksamheten kan bygga mycket mer själv — men behöver fortfarande verifiera resultatet. |

Övergång:

> Samma arbetssätt passar inte alla fyra, men samma principer gör det.

## 4. Kom igång utan verktygskult (18–25 min)

### Börja med ett riktigt problem, inte med en AI-initiativplan

Målet här är att ta bort friktion och motstånd. En person ska kunna prova i sitt vanliga flöde, på ett arbete de redan äger, utan att först behöva lära sig ett nytt ramverk eller få godkänt för en stor satsning.

- Börja inte med ett omfattande skill-bibliotek, interna MCP:er, agentfarmer eller en egen agentplattform.
- Välj ett återkommande och avgränsat arbete: en bugg, en liten feature, en testsvit, en migration eller en intern vy.
- Ge agenten en tydlig definition av färdigt: vad ska fungera, vad får inte påverkas och hur bevisar vi det?
- Låt teamet träna på att få bra resultat i små uppgifter innan ni höjer autonomin.

### Det som ofta inte fungerar i början

| Antipattern | Varför det bromsar | Gör så här i stället |
| --- | --- | --- |
| Ett stort skillbibliotek innan teamet har återkommande behov | Dokumentation och konfiguration blir ett eget projekt | Spara en instruktion först när den har hjälpt i flera riktiga uppgifter |
| En agentfarm för varje uppgift | Koordinering, kostnad och output blir svårare att överblicka än själva arbetet | Börja med en agent och en tydlig ägare |
| Ett gemensamt “rätt” verktyg för alla | Teamens kodbaser, arbetsflöden och preferenser skiljer sig åt | Ge ett säkert basutbud och låt team välja inom ramarna |
| Stora autonoma förändringar tidigt | Review och felsökning hinner inte med | Gör små, reversibla och testbara förändringar |
| Att mäta AI-mognad i antal prompts, skills eller agenter | Det mäter aktivitet, inte leveransvärde | Mät ledtid, kvalitet, stabilitet och upplevd friktion |

Formulering att använda i talet:

> Vi ska inte bygga en AI-fabrik innan vi har lärt oss använda en bra skruvdragare.

En enklare variant om du vill undvika metaforen:

> Gör det lätt att prova, lätt att kontrollera och lätt att dela det som fungerade.

### Det du behöver första veckan

1. Godkänd tillgång till ett eller två verktyg/modeller.
2. En tydlig policy för kod, data och hemligheter.
3. Ett repo som går att starta, testa och förstå.
4. En liten uppgift med en mänsklig ägare.
5. En gemensam retro: *vad blev bättre, vad blev sämre, vad ska vi ändra i arbetssättet?*

Det räcker. Resten är sådant man förtjänar genom verklig användning — inte något man behöver gissa fram i förväg.

**Researchstöd:** DORA 2025 beskriver AI som en förstärkare av teamets befintliga system. Team med snabba feedbackloopar och goda skyddsnät får mer nytta, medan högre förändringstakt utan sådana system kan försämra stabiliteten. [DORA 2025: State of AI-Assisted Software Development](https://cloud.google.com/blog/products/ai-machine-learning/announcing-the-2025-dora-report?e=48754805)

## 5. Rätt autonomi för rätt uppgift (25–33 min)

Huvudpoängen:

> För hög agentisk nivå skapar ofta överengineering.

> Ge gärna modellen mer tid att tänka. Men ge den inte automatiskt större scope, fler behörigheter eller frihet att ändra mer.

| Typ av arbete | Modell/effort | Agentens mandat | Kontroll |
| --- | --- | --- | --- |
| Förstå kod, formulera lösning, hitta filer | Snabb modell, låg effort | Läsa och föreslå | Människa väljer väg |
| Avgränsad bugg eller feature | Stark modell, medel effort | Ändra ett tydligt område, köra tester | Diff och relevanta tester |
| Komplex felsökning eller design | Stark modell, hög effort | Undersöka, planera, prototypa | Människa godkänner plan innan bred ändring |
| Reversibelt rutinjobb | Avgränsad agent-loop | Utföra med hårda ramar | CI, policy och rollback |
| Säkerhetskänsligt eller tvärsystem | Hög effort, liten autonomi | Analys och förslag | Djup mänsklig review |

Regel att lägga på en egen slide:

> Höj inte autonomin snabbare än er förmåga att förstå, reviewa och backa förändringen.

**Researchstöd:** Zalando beskriver hur agentisk utveckling både kan öka PR-storlek och bygga upp komplexitet snabbt. När review blir flaskhals behöver team bryta ned förändringar och ändra sitt arbetssätt. [Zalando: Agentic Engineering at Zalando](https://engineering.zalando.com/posts/2026/08/agentic-engineering-at-zalando-a-snapshot.html)

## 6. Review är den nya kärnkompetensen (33–41 min)

### AI-genererad kod är ett förslag, inte ett resultat

Visa fyra kontrollnivåer:

1. **Agenten själv:** läser diffen, kör formattering, typer/lint, tester och kontrollerar krav.
2. **Automatiseringen:** CI, tester, säkerhetskontroller, deploy-preview och observability.
3. **AI som andra granskare:** hittar mönster, överträdelser av konventioner och glömda edge cases.
4. **Människan:** bedömer produktnytta, domänlogik, avvägningar, risk och om ändringen är rätt sak att göra.

En andra AI-review ersätter inte en mänsklig reviewer, men kan göra den mänskliga reviewn mer värdefull. Människan ska inte lägga sin bästa tid på formatfel eller att summera en diff.

**Researchstöd:** GitHub rekommenderar att kombinera automatiserad AI-review med mänsklig kollegial review, snarare än att ersätta den senare. [GitHub Docs: Review AI-generated code](https://docs.github.com/en/enterprise-cloud@latest/copilot/tutorials/review-ai-generated-code)

## 7. En rimlig 90-dagarsstart för en organisation (41–46 min)

### Dag 1–30: få igång goda vanor

- Tillåtna verktyg och enkel data-/säkerhetspolicy.
- En gemensam introduktion med verkliga uppgifter.
- En pilot i ett team eller på ett väl avgränsat initiativ.
- Krav: varje AI-förändring ska vara testbar och reviewbar.

### Dag 31–60: gör lärandet delat

- Veckovis 30 minuter: visa ett fungerande case och ett misslyckande.
- Spara de tre mest användbara instruktionerna, inte 100 generiska skills.
- Gör agent self-review till en normal PR-rutin.
- Mät inte rader kod; följ ledtid, PR-storlek, fel efter release och teamets upplevda friktion.

### Dag 61–90: höj bara där bevis finns

- Automatisera en återkommande lågriskuppgift.
- Förbättra repo-konteksten: startinstruktioner, testkommandon, arkitekturbeslut och lokala regler.
- Lägg till återanvändbara skills först när ett mönster bevisligen återkommer.

Målet efter 90 dagar är inte en central agentplattform eller en identisk metod för alla. Målet är att flera team har hittat ett tryggt och produktivt sätt att använda AI i sin egen vardag, och att de kan dela de få arbetssätt som verkligen fungerar.

### Kontrastfall: när en full harness är rimlig

OpenAI:s experiment med en helt agentgenererad produkt visar vad som krävs när man går mycket längre: agentvänligt repo, tydliga arkitektoniska gränser, tester, observability och feedbackloopar. Det är inte en startrekommendation för de flesta organisationer, men en bra påminnelse om att fart kräver ett system runt agenten. [OpenAI: Harness engineering](https://openai.com/index/harness-engineering/)

## 8. Avslut och frågor (46–50 min)

Avsluta med tre meningar:

> Börja inte med mer autonomi — börja med bättre feedback.
>
> Sänk tröskeln för att börja, men höj inte risknivån i samma andetag.
>
> AI ska inte göra teamet mindre ansvarigt; den ska frigöra mer ansvar till de svåra besluten.
>
> Den bästa AI-resan börjar inte med en plattform. Den börjar med ett riktigt problem, en liten förändring och en review som faktiskt håller.

Bryggan till ett kundnära AI-tema:

> En kundnära harness bygger organisationsminne och bättre beslut i produkten. Vår interna harness bygger samma sak för utvecklingsteamet: delad kontext, återkoppling och förtroende nog att öka kapaciteten utan att tappa kontrollen.

## Källor att använda sparsamt i talet

- [DORA 2025: State of AI-Assisted Software Development](https://cloud.google.com/blog/products/ai-machine-learning/announcing-the-2025-dora-report?e=48754805)
- [Zalando: Agentic Engineering at Zalando](https://engineering.zalando.com/posts/2026/08/agentic-engineering-at-zalando-a-snapshot.html)
- [OpenAI: Harness engineering](https://openai.com/index/harness-engineering/)
- [GitHub Docs: Review AI-generated code](https://docs.github.com/en/enterprise-cloud@latest/copilot/tutorials/review-ai-generated-code)
- [Pacing the Frontier](https://www.pacingthefrontier.com/)
