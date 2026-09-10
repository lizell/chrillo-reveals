# Begrepp och tips

Code Base · fördjupning

Begreppen beskriver funktioner; namn och beteenden kan variera mellan verktyg. Tipsen är förslag att pröva i den egna miljön.

## Modellen föreslår. Agenten kan också agera.

- **Modell / LLM:** En språkmodell som genererar text, kod och förslag utifrån sin indata.

- **Agent:** En modell i en arbetsloop med verktyg: läsa, agera, se resultat och fortsätta.

- **Verktyg / tool:** En funktion agenten kan anropa, till exempel filsökning eller testkörning.

- **Autocomplete:** Kodförslag medan du skriver. Du driver själv arbetet steg för steg.



## Vad ber vi om – och när är det klart?

- **Prompt:** Instruktionen eller frågan du ger modellen vid ett tillfälle.

- **Brief / promptjam:** Briefen beskriver uppgiften. Promptjam är att forma den tillsammans.

- **Scope:** Avgränsningen: vilket beteende och vilka delar får ändras?

- **Acceptanskriterier:** Observerbara villkor för att godkänna resultatet. ”Klart när …”



## Vad finns med i samtalet?

- **Kontext:** Instruktioner, meddelanden, kod och verktygsresultat som modellen får se.

- **Token / kontextfönster:** Token är textbitar. Kontextfönstret begränsar hur mycket modellen kan hantera åt gången.

- **Kompaktering / minne:** Historik sammanfattas eller sparas för senare bruk. Detaljer kan gå förlorade.

- **Hallucination:** Ett trovärdigt men felaktigt eller påhittat påstående, API eller kodförslag.



## Instruktion, plan eller skill?

- **Repoinstruktioner:** Lokala arbetsregler och kommandon, exempelvis i AGENTS.md där verktyget stöder det.

- **Skill:** Återanvändbara instruktioner och ibland skript för en viss typ av uppgift.

- **Plan:** Uppgiftens steg, status och öppna frågor. Uppdateras när vi lär oss något.

- **ADR:** Architectural Decision Record: ett beslut, alternativen och varför vi valde så.



## Vad ingår i en setup?

- **MCP:** Model Context Protocol: ett standardiserat sätt att koppla AI-appar till verktyg och information.

- **Harness:** Miljön som driver agenten: arbetsloop, verktyg, kontext, kontroller och återkoppling.

- **Sandbox:** En tekniskt begränsad körmiljö, exempelvis för filåtkomst och nätverk.

- **Behörigheter:** Vad verktygen faktiskt får läsa, ändra eller publicera. Separat från promptens önskemål.



## Mer tankearbete eller mer frihet?

- **Effort / reasoning:** En inställning för modellens resonemangsinsats, där verktyget erbjuder den.

- **Autonomi / mandat:** Vilka steg agenten får driva själv innan en människa behöver ta ställning.

- **Subagent:** En delegerad agent för en deluppgift, ofta med egen kontext. Kan också köras sekventiellt.

- **Worktree:** En separat arbetskatalog för en Git-gren. Isolerar filer, men inte all miljö eller alla tjänster.



## Vad granskar och levererar vi?

- **Repo / branch:** Repot innehåller kod och versionshistorik. En branch är en gren för förändringar.

- **Diff / PR:** Diffen visar ändringarna. En pull request samlar dem för granskning och eventuell merge.

- **CI / CD:** Automatiska kontroller och leveranssteg. CD kan avse delivery eller deployment.

- **Release / rollback:** Sätta en ändring i bruk respektive återgå till en tidigare fungerande version.



## Test, utvärdering och uppföljning.

- **Enhets- / integrationstest:** Kontrollerar en avgränsad del respektive samspelet mellan flera delar.

- **End-to-end / gränsfall:** Ett helt användarflöde respektive indata eller situationer nära beteendets gränser.

- **Eval / LLM-judge:** En eval utvärderar scenarier. En LLM-judge använder en modell som bedömare och kan själv ha fel.

- **Observability / guardrails:** Insyn via loggar, mätvärden och spårning; kontroller som begränsar oönskat beteende.



## Tre startlägen – och en mindre del.

- **Greenfield:** Ny produkt med stor frihet att forma lösningen. Ossy började som en ny idé.

- **Brownfield / rewrite:** Arbete i en befintlig miljö; rewrite är en omskrivning. Login behövde passa in bland många beroenden.

- **Legacy / vidareutveckling:** Ett ärvt eller etablerat system. Astrid har historik, användare och beslut att bygga vidare på.

- **Vertikal skiva:** En liten fungerande del genom de lager som behövs för ett användarbeteende.



## Förkortningarna runt arbetet.

- **API:** Application Programming Interface: gränssnittet som andra program eller komponenter anropar.

- **UX / CMS:** User Experience: användarupplevelsen. Content Management System: ett system för att hantera innehåll.

- **Markdown / README:** Ett enkelt textformat; repots introduktion med bland annat start- och testinstruktioner.

- **DORA:** Googles forskningsprogram om utveckling och leverans. Rapporten 2025 handlar om AI-stödd utveckling.



## Hur får agenten rätt kunskap?

- **Retrieval:** Hämta relevant information från en källa för den aktuella frågan.

- **RAG:** Retrieval-Augmented Generation: låt modellen använda hämtat underlag när den formulerar svaret.

- **Strukturerat innehåll:** Innehåll med tydliga fält, typer och relationer som både kod och människor kan tolka.

- **AI-readiness:** Hur redo kod, data och arbetssätt är för AI-användning. Ett samlingsbegrepp, ingen garanti.



## Börja med ett jobb som går att avsluta.

- **Det som hjälper:** En uppgift för några timmar. Ett synligt mål och en reviewer. Ett repo som går att köra och testa.

- **Det som stjälper:** ”Bygg om systemet.” Oklart vad som ska fungera. En hel setup innan första försöket.


Första varvet: välj → bygg → kontrollera → stäm av.



## Styr nästa steg med tydlig feedback.

- **Det som hjälper:** Be om en kort plan när vägen är oklar. Ge ett fel som går att återskapa. Begär diff och faktiska testresultat.

- **Det som stjälper:** ”Försök igen” utan ny information. Nya sidospår före en klar del. Att tro att en grön summering räcker.


”Det här beteendet saknas. Visa ett test som fångar det.”



## Spara en regel när den löser ett problem.

- **Det som hjälper:** Korta start- och testkommandon. Ett bra lokalt exempel. Ta bort instruktioner som krockar.

- **Det som stjälper:** Långa generiska regelverk. Samma instruktion på flera ställen. Skills som laddas utan att behövas.


En återkommande miss → en tydlig regel → prova igen.



## Låt planen överleva sessionen.

- **Det som hjälper:** Checklistor med verklig status. Beslut med motiv och alternativ. Uppdatera efter en ny insikt.

- **Det som stjälper:** Alla beslut kvar i chatten. En plan som beskriver gårdagen. ”Klart” utan körbara bevis.


Spara läget: klart, öppet, blockerat och nästa steg.



## Börja om med rätt sammanfattning.

- **Det som hjälper:** En avgränsad fråga. Aktuella filer och beslut. En kontrollerad överlämning.

- **Det som stjälper:** Hela historiken inklistrad igen. Upprepade fixar på samma antagande. ”Fortsätt” efter att målet ändrats.


”Sammanfatta målet, fynden, filerna och nästa kontroll.”



## Byt modell för en konkret anledning.

- **Det som hjälper:** Pröva på samma avgränsade uppgift. Mer resonemang för svåra avvägningar. Jämför kvalitet, tid och kostnad.

- **Det som stjälper:** Högsta effort på alla uppgifter. Byte utan att förstå felet. Mer autonomi för att modellen är stark.


Ändra en sak i taget och se om resultatet förbättras.



## Lägg till det som tar bort friktion.

- **Det som hjälper:** Snabbare tester och startmiljö. Ett skript för ett återkommande steg. En koppling till kunskap som saknas.

- **Det som stjälper:** MCP-servrar utan tydligt behov. Mer åtkomst än uppgiften kräver. Automation av ett oklart arbetssätt.


Behov först: miljö → instruktion → skill eller verktyg.



## Dela upp arbete som kan göras separat.

- **Det som hjälper:** En tydlig deluppgift per agent. Separata arbetskopior vid behov. En ägare för helhet och integration.

- **Det som stjälper:** Flera agenter i samma filer. Överlämningar utan sammanhang. Fler förslag än någon hinner granska.


Prova först en avgränsad undersökning eller extra review.



## Behåll bara det som hjälper.

- **Det som hjälper:** Skriv ned vad som gick fel. Förbättra en sak i setupen. Prova på nästa liknande uppgift.

- **Det som stjälper:** Fler regler efter varje enstaka miss. Mäta antal prompts eller agenter. Behålla verktyg som skapar merarbete.


Varje försök ska ge ett bättre resultat eller en användbar lärdom.



## Vad finns kvar efter nästa modellbyte?

- **Gemensam grund:** Prövade instruktioner och teststöd. Beslut och lärdomar. En miljö som går att köra.

- **Lokalt i uppdraget:** Kundens kod och data. Behörigheter och integrationer. Domänregler och acceptans.


Dela metoden. Håll kundens information i rätt sammanhang.



## ”Hur använder ni AI i vår leverans?”

- **Vad hjälper AI till med?:** Beskriv den konkreta uppgiften och dess avgränsning.

- **Hur kontrolleras det?:** Visa testresultat, review och vem som accepterar.

- **Vad gäller för materialet?:** Förklara verktygsval, åtkomst och hantering enligt uppdragets ramar.



Underlag och vidare läsning finns i [källkartan](kallor.md).
