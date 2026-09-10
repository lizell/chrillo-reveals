# Källor och redaktionella avgränsningar

Kontrollerat 10 september 2026. Presentationens råd är en syntes av Christians tidigare material, generella arbetssätt och nedanstående primärkällor. De är inte en utvärderad införandemetod eller ett löfte om viss effekt.

## Erfarenheter från SVT

Huvudkälla för de tre casen är Christians egen transkriberade berättelse från 10 september 2026, tillhandahållen särskilt för denna presentation. Källfilen heter `transcript.txt`; råmaterialet kopieras inte till det här repot. Plauds PDF-sammanfattning har lästs som stöd, men transkriptionen och Christians uttryckliga beskrivning i uppdraget har företräde.

| Case | Tidsstämplar i inspelningen | Uppgifter som används |
| --- | --- | --- |
| Ossy | 00:00:03–00:02:05 | Idé från sporten under en tekniksprint; handskrivet första försök; nytt försök cirka ett halvår senare; AI-kodning, fredagsarbete, tre omskrivningar och en månad på heltid inför OS; använd chatbot och AI genom utveckling och utvärdering. |
| Login | 00:02:05–00:05:44 | Befintliga implementationer, en gemensam lösning över plattformar och team; Markdown-planer med arkitektur och nätverksflöden; frågor till planerna; tidiga exempelappar för att låta UX och produktägare prova; produktion vid inspelningstillfället. |
| Astrid CMS | 00:05:44–00:07:13 | Flera års handskriven kod; övergång till helt AI-driven vidareutveckling; anpassning till regler och struktur genom dokumentation, agentfiler och skills; små uppgifter följda av större. System i drift framgår också av Christians beskrivning i uppdraget. |

Stavningarna Ossy och Astrid följer Christians instruktion och det befintliga presentationsmaterialet, inte taligenkänningens namnvariationer. Relativa datum omvandlas inte till kalenderår eller ett visst OS. ”100 procent AI” återges som AI-driven utveckling och kodgenerering med mänskligt ansvar; det avser inte en autonom organisation. Login gick i produktion **9 september 2026**, enligt Christians senare uttryckliga komplettering i samtalet. Inget påstående görs om att samtliga klienter är migrerade. Astrid beskrivs som vidareutveckling, inte en total omskrivning.

Sammanfattningens formuleringar om arbete ”i smyg”, en ”digital tvilling” och att casen ”bevisar” metodens effekt har inte förts vidare. Resultaten återges som Christians erfarenheter. Det finns inga uppmätta produktivitetsvinster, jämförande studier eller specifika incidenter i underlaget. De gemensamma lärdomarna är en redaktionell syntes.

[Hur AI ändrar yrkesrollen](../../slides/hur-ai-andrar-yrkesrollen.md) kompletterar Ossys arbetsloop och talaranteckningar med teamstorlek, promptjam, test- och reviewarbete samt uppföljning i drift.

[AI-driven utveckling](../../slides/ai-driven-utveckling.md) och [workshopens tidigare outline](../ai-driven-development/outline.md) bidrar med scope, feedback, autonomi, review och gradvis införande. Övriga uppdragsmaterial används endast för generella arbetssätt. Kund- och systemuppgifter från andra uppdrag återges inte. De tre uttryckligen beställda SVT-casen hålls åtskilda från dessa underlag.

Bildnummer nedan avser huvudbildernas horisontella positioner; PDF-sidnumren inkluderar även vertikala fördjupningar.

Christians senare komplettering i samtalet är källa för att Ossy också blev ett ramverk för att skapa bottar enkelt och säkert med specifik kunskap. Uppgiften stöds även av ramverksbeskrivningen i den tidigare Ossy-presentationen. Inga detaljer om kunskapshämtning, datalagring eller en viss säkerhetsarkitektur läggs till.

Dialora är exemplet Christian delade från Ossy-ramverket. Presentationen använder en lokal skärmbild av gränssnittet, tagen 10 september 2026. Introduktionen beskriver en bot för frågor om SVT:s program och tjänster. Inga frågor skickades vid fotograferingen. Skärmbilden är en illustration, inte en utvärdering av svarskvalitet eller säkerhet.

## Externa primärkällor

| Källa | Användning | Begränsning |
| --- | --- | --- |
| [DORA: State of AI-assisted Software Development 2025](https://dora.dev/research/2025/dora-report/) | Bild 21: AI förstärker befintliga organisatoriska styrkor och svagheter. | Resultat på organisationsnivå ger inte en garanterad effekt för ett visst team eller verktyg. Upplägget för första försöket är vårt förslag. |
| [GitHub Docs: Review AI-generated code](https://docs.github.com/en/copilot/tutorials/review-ai-generated-code) | Bild 17 och deltagarblad: funktionella kontroller, intention, kontext, beroenden och mänsklig review. | Leverantörens praktiska vägledning; inte en kontrollerad effektstudie. |
| [METR: Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/) | Bakgrund till talaranteckning på bild 21 och källbilden. | 16 erfarna utvecklare, 246 uppgifter i välkända öppna projekt och tidiga 2025-verktyg. Inte en generell skattning för dagens verktyg. |
| [METR: We are Changing our Developer Productivity Experiment Design](https://metr.org/blog/2026-02-24-uplift-update/) | Nyanserar den tidigare studien. | METR beskriver att senare data ger en opålitlig signal om aktuell effekt, bland annat på grund av urval och svårigheter att mäta tid vid parallellt agentarbete. |

## Pedagogiska exempel

Sökfältet, koden med `!query`, testfallen och feedbackpromptarna är skapade för presentationen. De återger inget riktigt system, ingen kundincident och ingen faktiskt genomförd agentkörning. Kodförslaget är avsiktligt felaktigt så att publiken kan öva på review. Promptar, upplägget för första försöket och mätfrågor är rekommendationer att anpassa lokalt.


## Begrepp och tips

Begreppsguiden förklarar terminologin i passet. Tipsen utgår främst från de generella arbetssätten i tidigare workshopmaterial: avgränsade steg, uppdaterade planer, fokuserad kontext, korta instruktioner och delade lärdomar. Råden är förslag att pröva, inte uppmätta effekter från kundprojekt.

Kompletterande primärkällor, kontrollerade 10 september 2026:

- [Anthropic: Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents): relevant kontext, sammanfattning och avgränsade deluppgifter.
- [Claude Code: Best practices](https://code.claude.com/docs/en/best-practices): verifierbara mål och fokuserat arbete. De produktspecifika detaljerna återges inte som generella regler.
- [Model Context Protocol: Tools](https://modelcontextprotocol.io/specification/2024-11-05/server/tools): MCP kan exponera anropbara verktyg; protokollet innebär inte automatiskt att alla handlingar är tillåtna.

En agent kan föreslå hur arbetet ska läggas upp, men har ingen säker självkännedom om det mest effektiva valet. En ny kontext, en subagent och parallellt arbete är olika saker. Skills och instruktioner behöver prövas för relevans; fler är inte automatiskt bättre.

## Anpassning till Precio Fishbone

[Precio Fishbones systemutveckling](https://www.preciofishbone.se/vad-vi-gor/tjanster/systemutveckling/) beskriver Microsoft/Azure, integration, modernisering och förvaltning. [Webbutvecklingserbjudandet](https://www.preciofishbone.se/vad-vi-gor/tjanster/webutveckling/) beskriver Optimizely och redaktörsarbete. Detta motiverar kopplingen mellan de tre SVT-casen och deltagarnas möjliga arbetsområden. Inga enskilda kundcase eller påståenden om deras aktuella AI-mognad används.

Niklas delade den 19 augusti tre presentationsbilder i den privata Slack-konversation som Christian bad oss läsa. De bidrar med teman: AI-utveckling som färdighet, kollektivt lärande, gemensamma arbetssätt och ett trovärdigt svar på kundens frågor om AI i leveransen. De nya bilderna är vår praktiska tolkning, inte ett påstående om Precio Fishbones beslutade policy. Privat konversation, originalbilder och annan orelaterad information har inte kopierats in i repot. Källmeddelanden: [temat för passet](https://app.slack.com/archives/D09AD02HYKF/p1787147361552039) och [kompletterande bilder](https://app.slack.com/archives/D09AD02HYKF/p1787147492842999), åtkomst krävs.

De delade bildernas numeriska produktivitetspåstående och påståenden om konkurrenter eller framtida marknadsutveckling används inte som fakta i presentationen. Hänvisningen till Jonas pass bygger på arrangörens programtext i uppdraget.


## Bilder, video och diagram

Christian tillhandahöll skärmbilderna av Astrid CMS och SVT Konto samt klippet `ossy-curlar-2026-03-04 10_31.mp4` från Downloads för användning i presentationen. Bilder och video har kopierats utan innehållsändring. Astrid-bilden visar stage-miljön, inte en skärmbild som påstås vara från produktion. Videon är 19,13 sekunder utan ljudspår och visar hur Ossy presenteras i en curlingsändning. Stillbilden är en oförändrad bildruta vid 15 sekunder.

Diagrammen är pedagogiska scheman utifrån de redan beskrivna arbetssätten. Login-diagrammet är en målbild över klienter och ett gemensamt flöde, inte en nätverks- eller säkerhetsarkitektur. Astrid-diagrammets block är generiska och återger inte kodbasens verkliga moduler. Uppspelningskontroller och länkar ingår i HTML-versionen; PDF innehåller stillbilder.


### Valbar introduktion och utvecklingsloop

- Christian Lizells egna presentationsbilder, delade i samtalet 10 september 2026: bakgrundsbilden används oförändrad; utvecklingsloopen har ritats om i presentationens formspråk.
- Athegas företagspresentation, läst 10 september 2026: grundat 1997, systemutveckling, AI/maskininlärning, teknisk granskning och branscher. Logotyp hämtad från samma webbplats.

- Underlaget ”Om Athega”: teknikintresset, aktivt ägande, långa kundrelationer och AI-satsningen sedan 2016. Underlag till omarbetad introduktion.
