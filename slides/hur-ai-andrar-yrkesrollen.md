<!-- .slide: data-background-gradient="radial-gradient(circle at 30% 50%, #1a1a4a 0%, #0a0a1a 70%)" -->
# Hur AI ändrar yrkesrollen
## (på riktigt)

Christian Lizell (Athega @ SVT Nyheter & Sport)  
Öppet hus · Chas Academy · 20–25 min

Note:
Syfte: nyansera bilden. Visa vad som faktiskt förändrats i vardagen.
Jag använder Ossy som ett konkret exempel, men fokus är arbetssättet och vad som blir viktigare i rollen.

---

# Vad detta handlar om
## (och inte)

--

## Detta handlar om
- Praktiska förändringar i hur vi bygger mjukvara idag
- Ett konkret case: Ossy (SVT)
- Vad vi tittar efter vid rekrytering 2026

--

## Det är inte
- En AI-demo eller verktygsreklam
- Ett "AI tar jobben"-snack
- En teknisk deep dive i modeller

Note:
Sätt förväntningar. Jag pratar om arbetsmetod, kvalitet, risk och ansvar.

---

## Upplägg (20–25 min)

1) Vad som faktiskt förändrats (5 min)  
2) Case: Ossy och hur vi jobbar (10–12 min)  
3) Vad Chas tränar er för (3–4 min)
4) Rekryteringsperspektiv 2026 (3–5 min)

Note:
Håll tempot. Om tiden blir tight: korta demo/case-delen men behåll Chas-kopplingen och rekryteringsdelen.

---

<!-- .slide: data-background-gradient="linear-gradient(135deg, #1a1a4a 0%, #2a1a3a 100%)" -->
# Vad som faktiskt förändrats i yrkesrollen
## Del 1

Note:
Övergång: från abstrakt AI-prat till konkreta förändringar i vardagen.

--

## 💸 Förändring 1: Implementation blev "billig"

- Det som tog månader kan nu ske på timmar eller dagar
- Det kostar lite att prova en idé — normalt att kasta och börja om
- Kod blir kommunikationsmediet: man bygger istället för att diskutera diagram

Note:
Förr: mycket "sunk cost", försiktighet och abstrakta planeringsmöten.
Nu: bygg en fungerande prototyp, låt alla interagera med den, iterera därifrån.
Designers kan uppleva flödet istället för att föreställa sig det.

--

## 🎯 Förändring 2: Kvalitetsarbete flyttade framåt

- Mer tid på intention, avgränsningar, edge cases
- Mindre "hero debugging" i slutet
- Kvalitet byggs som ett system, inte ett granskningssteg

Note:
AI kan producera output snabbt. Värdet ligger i att definiera "rätt", "säkert" och "klart".
Därför blir krav, teststrategi och riskhantering viktigare.

--

## 🧠 Förändring 3: Omdöme blev mer värdefullt

- Kan du bedöma output du inte skrivit?
- Kan du resonera om risk, säkerhet och konsekvenser?
- Kan du förklara varför något är korrekt?

Note:
AI tar inte bort ansvar. Den koncentrerar ansvar i omdöme och verifiering.
Därför blir grundläggande systemförståelse ännu viktigare.

--

### Varför du fortfarande behöver kunna koda

- Du kan inte bedöma det du inte förstår
- Systemförståelse är grunden för omdöme
- Utan den vet du inte när AI har fel — eller varför
- "Koda" handlar mindre om att skriva, mer om att tänka i system

Note:
Poängen: AI gör att du skriver mindre kod, inte att du behöver förstå mindre.
Den som förstår arkitektur, beroenden och felhantering kan styra AI.
Den som inte gör det blir beroende av att AI alltid har rätt — och det har den inte.

---

<!-- .slide: data-background-gradient="linear-gradient(135deg, #0a2a3a 0%, #1a1a4a 100%)" -->
# Case: Ossy
## (SVT Nyheter & Sport)
## Del 2

![Ossy](assets/images/ossy.png) <!-- .element: style="height: 300px; border: none; box-shadow: none; background: transparent;" -->

Note:
Nu gör vi det konkret: hur jobbar man i ett AI-first-projekt i produktion?

--

## Vad är Ossy?

- SVT:s första publika AI-tjänst: en chatbot i SVT-kontext
- Användes flitigt och framgångsrikt under OS
- Plus: ett ramverk för att snabbt skapa nya expertbotar

Note:
Max 30 sek. Inga features.
Poängen: produkt + återanvändbar kapacitet.

--

<iframe src="https://australis.svt.se/quickshot/kross/widgets/fUBlY/webframe.html?darkMode=true" width="900" height="100%" style="border: 1px solid #2a2a4a; border-radius: 16px; background: #0a0a1a; height: 620px;"></iframe>

Note:
Visa snabbt — ställ en fråga som funkar, t.ex. "Vilka matcher visas ikväll?" eller "Vad hände i allsvenskan senast?"
Lägg inte för lång tid här, max 30 sek.

--

## Teamet (och varför det är intressant)

- 3 utvecklare + 1 redaktionell person
- Ingen dedikerad UX, testare, AD eller DevOps
- Väldigt litet team, ändå production-grade
- Vi löste det inte med fler roller — utan med en annan arbetsmetod

Note:
Teamet är litet med flit, inte av brist.
Alla kan interagera med fungerande kod — redaktören ser beteendet direkt, inte via mockups.
Arbetsmetoden är det som gör det möjligt.

--

## 🔄 Vår standard-loop

<div class="fragment semi-fade-out" data-fragment-index="1">

Idé → Promptjam → Generera → Verifiera → Test → PR → Release

</div>

<div class="fragment" data-fragment-index="1">

<span style="color: #a78bfa">🧑🤖 Idé</span> → <span style="color: #a78bfa">🧑🤖 Promptjam</span> → <span style="color: #f59e0b">🤖 Generera</span> → <span style="color: #a78bfa">🧑🤖 Verifiera</span> → <span style="color: #a78bfa">🧑🤖 Test</span> → <span style="color: #a78bfa">🧑🤖 PR</span> → <span style="color: #6ea8fe">🧑 Release</span>

<small>🧑 = människa &nbsp; 🤖 = AI-agent &nbsp; 🧑🤖 = tillsammans</small>

</div>

Note:
Promptjam = vi formar beställningen tillsammans:
mål, avgränsningar, risker, acceptanskriterier.
Vi synkar ofta, ibland sitter vi i samma möte och jobbar parallellt.

--

## Radikalt (?): ingen kod skrivs för hand

- AI är inte ett sidoverktyg — det är vårt primära sätt att bygga
- All kod genereras av AI (t.ex. Claude/Codex)
- Även "akutfixar" går ofta snabbare och med färre misstag via AI

Note:
Motintuitivt: "jag fixar bara snabbt" är en klassisk källa till slarv och regressioner.
AI kan ge mer konsekvent output om kontext + tester finns i loopen.
Men det kräver att man förstår vad som byggs och varför det fungerar.

--

## Varför det går fort utan att bli vårdslöst

- Implementering + test är billigt
- Lätt att prova, kasta, prova igen
- "Klart" = good enough for now → release → iterera

Note:
Vi har skrivit om större delar flera gånger.
Det är inte slöseri när kostnaden för iteration är låg och lärandet är högt.

--

## ⚠️ När det blir svårt

<table>
<tr><th>Problem</th><th class="fragment" data-fragment-index="1">Motdrag</th></tr>
<tr><td>AI kan missförstå kontext</td><td class="fragment" data-fragment-index="1">Tydligare kontext + krav + källor</td></tr>
<tr><td>AI kan utgå från gammal dokumentation</td><td class="fragment" data-fragment-index="2">Peka den till rätt kunskap och dokumentation</td></tr>
<tr><td>Man kan hamna i frustrerande fel-loopar</td><td class="fragment" data-fragment-index="3">Byt modell/verktyg när det inte passar</td></tr>
</table>

Note:
Det här är en yrkesskicklighet — att veta när man ska byta approach.

--

## 🧪 Test av chatbot: du kan inte testa exakta strängar

Vi använder:
- enhetstester
- integrationstester
- en LLM-judge som bedömer "rimlighet" i svaren

Note:
Chatbotar är inte deterministiska UI-texter.
Därför testar vi scenarion och acceptans.
Det blir inte 100% hallucinationsfritt, men vi bygger system för att upptäcka och begränsa fel.

--

## 🔒 Säkerhet och förtroende (icke-förhandlingsbart)

- flera lager av guardrails
- modeller/verktyg reviewar varandra
- manuell koll där det behövs

Note:
Guardrails skyddar både boten och användaren.
Exempel på vardagsfriktion: ibland blockar den fel (t.ex. "visa klipp på Elvira" kan feltolkas).
Det kräver finjustering, inte bara "släppa fri".

--

## 📊 Drift och kostnadskontroll

- övervakning (dashboards/alerts)
- cost dashboards och trösklar
- vi byter modell/leverantör när förutsättningarna ändras

Note:
Det här är en del av produkten, inte en eftertanke.
Modeller förändras; att kunna byta är en plan, inte en incident.

---

## Det här är också en utbildningsfråga

- AI är nu en naturlig del av utvecklingsprocessen
- Men det räcker inte att kunna "få fram kod"
- Du måste kunna resonera, granska och förbättra
- Det liknar verkligheten mer än gamla skoluppgifter gjorde

Note:
Koppla till publiken: det här är varför utbildningen inte bara kan handla om syntax och tutorials.
Det viktiga är arbetsloopen: förstå problemet, använda verktyg klokt, verifiera och kommunicera.

---

<!-- .slide: data-background-gradient="linear-gradient(135deg, #1a243a 0%, #113a2d 100%)" -->
# Vad Chas verkar träna er för
## Del 3

Note:
Här visar jag att jag faktiskt läst på. Knyt till deras sajt utan att låta som reklamfilm.

--

## Det jag tycker de verkar fatta

- AI beskrivs som en del av arbetsprocessen, inte som magi
- De betonar branschnärhet tidigt: talks, meetups, studiebesök
- De verkar värdera resonemang och kommunikation, inte bara rätt svar
- Tvärfunktionellt arbete dyker upp flera gånger

Note:
Det här matchar ganska väl hur jobbet faktiskt ser ut 2026.
Särskilt bra: fokus på granskning, bedömning och samarbete runt AI-genererad output.

--

## Om jag ska översätta det till arbetslivet

Chas verkar träna fyra saker som faktiskt spelar roll:

1. bygga något som fungerar
2. resonera om varför det fungerar
3. samarbeta med andra roller
4. anpassa sig när verktygen ändras

Note:
Det här är ett bra ställe att vara generös men konkret.
Inte "ni lär er allt", utan "det här är relevanta träningsytor för dagens arbetsliv".

--

## Det jag själv hade maxat ännu mer

- mer systemförståelse: integrationer, drift, beroenden
- mer verifiering: tester, utvärdering, felsökning
- mer risk/snack om säkerhet, integritet och policy
- mer träning i att presentera tekniska avvägningar tydligt

Note:
Säg detta vänligt. Det blir ett värdefullt inspel till studenterna: vad de själva bör jaga utöver kursplanen.

---

<!-- .slide: data-background-gradient="linear-gradient(135deg, #2a1a3a 0%, #1a2a1a 100%)" -->
# Rekryteringsperspektiv 2026
## Del 4

Note:
Nu: vad betyder allt detta för er som studenter och för oss som anställande?

--

## Det som blivit viktigare

- systemtänk (beroenden, felscenarier, drift)
- verifiering (test, utvärdering, felsökning)
- kommunikation (krav, avgränsningar, "definition of done")
- ansvar och riskmedvetenhet (säkerhet, integritet, policy)

Note:
AI gör output billigare.
Det som särskiljer proffs är verifiering och ansvar.

--

## Det vi gärna ser hos juniora kandidater

- du kan bygga något som kör end-to-end
- du kan läsa och förbättra kod du inte skrev
- du kan skriva/förbättra tester
- du kan iterera med feedback och förklara dina val
- du kan visa hur du tänkte, inte bara vad du byggde

Note:
Du behöver inte vara "AI-magiker".
Du behöver grunder + bra arbetsloopar + vilja att lära snabbt.
Videomoment, demos och muntliga resonemang blir därför mer relevanta än många tror.

--

## ⚡ Vanliga fallgropar

- "vibekodning" utan systemförståelse
- hoppa över verifiering för att output ser rimlig ut
- tro att AI ersätter omdöme
- nöja sig med att vara bra på prompts, men svag på grunderna

Note:
En minnesrad:
"Plausibelt är inte samma som korrekt. Snabbt är inte samma som säkert."

---

<!-- .slide: data-background-gradient="radial-gradient(circle at 50% 50%, #1a2a4a 0%, #0a0a1a 70%)" -->
## så…

AI kommer inte ta bort behovet av utvecklare.  
Den flyttar *var* arbetet sker.

Note:
Det som ger edge:
- bättre lärloopar
- bättre verifiering
- bättre omdöme

Avsluta med:
"Implementation blev billigare. Omdöme blev mer värdefullt."
Tacka och hänvisa till panelen/kvällen.

---

<!-- .slide: data-background-gradient="radial-gradient(circle at 50% 50%, #1a1a4a 0%, #0a0a1a 60%)" -->
# Tack!
