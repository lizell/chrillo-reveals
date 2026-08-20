<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=DM+Sans:opsz,wght@9..40,400;9..40,500;9..40,600;9..40,700&display=swap');

:root {
  --ink: #1a2332;
  --muted: #60707b;
  --paper: #f1faee;
  --mist: #deebe7;
  --teal: #2d8b8b;
  --deep-teal: #17696d;
  --seafoam: #a8dadc;
  --coral: #e86f51;
  --line: rgba(26, 35, 50, .16);
}

.reveal { background: var(--paper); color: var(--ink); }
.reveal .slides { text-align: left; }
.reveal h1, .reveal h2, .reveal h3, .reveal p, .reveal li, .reveal blockquote { font-family: 'DM Sans', sans-serif; }
.reveal h1 { -webkit-text-fill-color: var(--ink) !important; background: none !important; color: var(--ink) !important; font-size: 1.6em; font-weight: 700; letter-spacing: -.055em; line-height: 1.08; margin: .08em 0 .34em; max-width: 1080px; padding-top: .05em; text-transform: none !important; }
.reveal h2 { color: var(--ink); font-size: 1.5em; font-weight: 700; letter-spacing: -.045em; line-height: 1.05; margin: 0 0 .48em; }
.reveal h3, .eyebrow { color: var(--teal); font-family: 'DM Mono', monospace; font-size: .41em; font-weight: 500; letter-spacing: .12em; text-transform: uppercase; }
.reveal p, .reveal li { color: var(--ink); font-size: .7em; line-height: 1.45; }
.reveal strong { color: var(--deep-teal); font-weight: 700; }
.reveal small { color: var(--muted); font-size: .45em; }
.reveal .slides > section { box-sizing: border-box; padding: 5.5vh 7vw; height: 100%; }
.reveal .slide-number { background: transparent; color: var(--muted); font-family: 'DM Mono', monospace; font-size: 12px; left: 1.4vw !important; right: auto !important; top: 1.2vw !important; bottom: auto !important; }
.reveal .progress { color: var(--teal); height: 5px; }
.reveal .controls { color: var(--teal); }
.reveal .headline { max-width: 900px; }
.reveal .lead { color: var(--muted); font-size: .9em; max-width: 900px; }
.reveal .quote { border-left: 5px solid var(--teal); color: var(--ink); font-family: 'DM Sans', sans-serif; font-size: .82em; font-weight: 600; letter-spacing: -.035em; line-height: 1.25; margin: .72em 0; max-width: 880px; overflow-wrap: anywhere; padding: .18em 0 .18em .65em; }
.reveal .micro { color: var(--muted); font-family: 'DM Mono', monospace; font-size: .37em; letter-spacing: .02em; }
.reveal .marker { color: var(--coral); }

/* Cover */
.reveal .cover { background: var(--ink); color: var(--paper); overflow: hidden; }
.reveal .cover:before { background: radial-gradient(circle at 84% 18%, rgba(168, 218, 220, .32) 0 2%, transparent 2.2%), radial-gradient(circle at 76% 38%, rgba(45, 139, 139, .82) 0 10%, transparent 10.3%), radial-gradient(circle at 88% 70%, rgba(232, 111, 81, .86) 0 3%, transparent 3.3%); content: ''; inset: 0; opacity: .95; position: absolute; }
.reveal .cover > * { position: relative; z-index: 1; }
.reveal .cover h1 { -webkit-text-fill-color: var(--paper) !important; background: none !important; color: var(--paper) !important; font-size: 2.35em; line-height: 1.08; max-width: 920px; padding-top: .1em; }
.reveal .cover .eyebrow { color: var(--seafoam); margin-bottom: 1.1em; }
.reveal .cover .subtitle { color: var(--seafoam); font-size: .85em; max-width: 700px; }
.reveal .cover .footer { bottom: 5vh; color: rgba(241, 250, 238, .7); font-family: 'DM Mono', monospace; font-size: .38em; left: 7vw; position: absolute; }

/* Layout primitives */
.grid-2 { align-items: start; display: grid; gap: 2.2vw; grid-template-columns: repeat(2, minmax(0, 1fr)); width: 90%; }
.grid-3 { display: grid; gap: 1.3vw; grid-template-columns: repeat(3, minmax(0, 1fr)); align-items: stretch; width: 90%; }
.grid-4 { display: grid; gap: 1vw; grid-template-columns: repeat(4, minmax(0, 1fr)); align-items: stretch; width: 90%; }
.case-overview { display: grid; gap: .55em 1.1vw; grid-template-columns: repeat(2, minmax(0, 1fr)); margin-top: .75em; max-width: 92%; }
.case-overview .card { min-height: 2.15em; padding: .48em .62em; }
.case-overview .card h3 { font-size: .57em; margin-bottom: .24em; }
.case-overview .card p { font-size: .46em; line-height: 1.3; }
.autonomy-grid .card h3 { font-size: .46em; letter-spacing: .01em; }
.skeptic-grid .card { min-height: 1.55em; padding: .3em .55em; }
.skeptic-grid .number { font-size: 1.65em; margin-bottom: .05em; }
.skeptic-grid .card h3 { margin-bottom: .15em; }
.skeptic-grid .card p { font-size: .42em; }
.card { background: rgba(255,255,255,.48); border: 1px solid var(--line); border-radius: 15px; box-sizing: border-box; padding: .72em .78em; }
.card h3 { margin: 0 0 .45em; }
.card p { font-size: .56em; margin: 0; }
.number { color: var(--teal); display: block; font-family: 'Fraunces', serif; font-size: 2.3em; font-weight: 700; letter-spacing: -.06em; line-height: .9; margin-bottom: .2em; }
.step { border-top: 4px solid var(--seafoam); padding: .7em .62em; }
.step.active { background: var(--ink); border-color: var(--coral); color: var(--paper); }
.step.active h3, .step.active p { color: var(--paper); }
.step.active h3 { color: var(--seafoam); }

/* Diagrams */
.cycle { align-items: center; display: flex; gap: .08em; margin-top: 1.25em; width: 90%; }
.cycle .node { background: #fff; border: 1px solid var(--line); border-radius: 100px; color: var(--ink); flex: 1 1 0; font-size: .37em; min-width: 0; padding: 1.1em .3em; text-align: center; white-space: nowrap; }
.cycle .node.agent { background: var(--teal); border-color: var(--teal); color: white; }
.cycle .arrow { color: var(--teal); font-size: .72em; margin: 0 -.05em; }
.cycle-legend { display: flex; gap: 1.6em; margin-top: 1em; width: 90%; }
.cycle-legend span { color: var(--muted); font-family: 'DM Mono', monospace; font-size: .34em; }
.dot { border-radius: 99px; display: inline-block; height: .72em; margin-right: .4em; width: .72em; }
.dot-human { background: var(--ink); }.dot-agent { background: var(--teal); }.dot-together { background: linear-gradient(90deg, var(--ink) 50%, var(--teal) 50%); }
.ladder { display: grid; gap: .35em; grid-template-columns: repeat(5, 1fr); margin-top: .85em; width: 90%; }
.ladder .rung { border-bottom: 6px solid var(--mist); min-height: 5.15em; padding: .45em .48em; position: relative; }
.ladder .rung:nth-child(2) { border-color: #c2e0df; }.ladder .rung:nth-child(3) { border-color: var(--seafoam); }.ladder .rung:nth-child(4) { border-color: var(--teal); }.ladder .rung:nth-child(5) { border-color: var(--coral); }
.ladder b { color: var(--teal); display: block; font-family: 'DM Mono', monospace; font-size: .35em; margin-bottom: .65em; }
.ladder span { display: block; font-size: .54em; font-weight: 700; line-height: 1.08; }
.ladder small { display: block; font-size: .34em; line-height: 1.25; margin-top: .7em; }
.relation { display: grid; gap: 1.3vw; grid-template-columns: repeat(3, 1fr); margin-top: 1em; width: 90%; }
.relation .mode { border-bottom: 5px solid var(--mist); padding: .25em .35em .9em; }
.relation .mode:nth-child(2) { border-color: var(--seafoam); }.relation .mode:nth-child(3) { border-color: var(--coral); }
.relation .mode h3 { margin: 0 0 .45em; }.relation .mode p { font-size: .52em; }
.relation .example { color: var(--muted); font-family: 'DM Mono', monospace; font-size: .37em; line-height: 1.35; }
.brief { display: grid; gap: .65vw; grid-template-columns: repeat(5, 1fr); margin-top: .95em; width: 90%; }
.brief div { background: #fff; border-top: 4px solid var(--teal); padding: .55em; }.brief div:nth-child(2) { border-color: var(--seafoam); }.brief div:nth-child(3) { border-color: var(--coral); }.brief div:nth-child(4) { border-color: var(--teal); }.brief div:nth-child(5) { border-color: var(--ink); }
.brief strong { color: var(--ink); display: block; font-size: .52em; margin-bottom: .28em; }.brief span { color: var(--muted); display: block; font-size: .39em; line-height: 1.2; }
.review { align-items: center; display: grid; gap: .12em; grid-template-columns: 1fr .09fr 1fr .09fr 1fr .09fr 1fr; margin: 1em 0 .7em; width: 90%; }.review .gate { background: #fff; border: 1px solid var(--line); border-radius: 14px; min-height: 6.1em; padding: .52em; }.review .gate strong { color: var(--ink); display: block; font-size: .48em; margin-bottom: .4em; }.review .gate span { color: var(--muted); display: block; font-size: .33em; line-height: 1.3; }.review .gate.final { background: var(--ink); border-color: var(--ink); }.review .gate.final strong, .review .gate.final span { color: var(--paper); }.review .chevron { color: var(--teal); font-size: .6em; text-align: center; }
.timeline { border-top: 2px solid var(--line); display: grid; grid-template-columns: repeat(3, 1fr); margin-top: 1.2em; width: 90%; }.timeline .phase { padding: 1em .8em 0 0; position: relative; }.timeline .phase:before { background: var(--teal); border: 5px solid var(--paper); border-radius: 99px; content: ''; height: 12px; left: 0; position: absolute; top: -8px; width: 12px; }.timeline .phase:nth-child(2):before { background: var(--seafoam); }.timeline .phase:nth-child(3):before { background: var(--coral); }.timeline h3 { color: var(--ink); font-family: 'DM Sans', sans-serif; font-size: .55em; font-weight: 700; letter-spacing: -.02em; margin: 0 0 .45em; text-transform: none; }.timeline p { color: var(--muted); font-size: .43em; max-width: 230px; }
.source-list { display: grid; gap: .55em; grid-template-columns: repeat(2, 1fr); margin-top: .8em; width: 90%; }.source-list a { border-bottom: 1px solid var(--line); color: var(--ink); display: block; font-size: .52em; padding: .5em 0; text-decoration: none; }.source-list a span { color: var(--teal); font-family: 'DM Mono', monospace; font-size: .75em; }
.process { align-items: stretch; display: grid; gap: .48em; grid-template-columns: repeat(3, 1fr); margin-top: .8em; width: 90%; }.process .phase { background: #fff; border: 1px solid var(--line); border-radius: 12px; min-height: 4.8em; padding: .52em .6em; position: relative; }.process .phase.agent { border-top: 5px solid var(--teal); }.process .phase.human { border-top: 5px solid var(--ink); }.process .phase.together { border-top: 5px solid var(--seafoam); }.process .phase b { color: var(--teal); display: block; font-family: 'DM Mono', monospace; font-size: .33em; margin-bottom: .5em; }.process .phase strong { color: var(--ink); display: block; font-size: .52em; line-height: 1.1; }.process .phase span { color: var(--muted); display: block; font-size: .36em; line-height: 1.3; margin-top: .35em; }
.glossary { display: grid; gap: .48em .9em; grid-template-columns: repeat(2, 1fr); margin-top: .65em; width: 90%; }.glossary .term { background: rgba(255,255,255,.45); border-top: 4px solid var(--teal); padding: .42em .55em; }.glossary .term:nth-child(2), .glossary .term:nth-child(5) { border-color: var(--seafoam); }.glossary .term:nth-child(3), .glossary .term:nth-child(6) { border-color: var(--coral); }.glossary strong { color: var(--ink); display: block; font-size: .54em; margin-bottom: .2em; }.glossary span { color: var(--muted); display: block; font-size: .38em; line-height: 1.25; }
.case-lens { display: grid; gap: 1.7vw; grid-template-columns: 1.1fr 1fr 1fr; margin-top: 1em; width: 90%; }.case-lens .lens { border-top: 5px solid var(--teal); padding: .65em .08em; }.case-lens .lens:nth-child(2) { border-color: var(--seafoam); }.case-lens .lens:nth-child(3) { border-color: var(--coral); }.case-lens h3 { color: var(--ink); font-family: 'DM Sans', sans-serif; font-size: .54em; font-weight: 700; letter-spacing: -.02em; margin: 0 0 .5em; text-transform: none; }.case-lens p { color: var(--muted); font-size: .46em; line-height: 1.35; margin: 0; }
.reflection { background: var(--ink); border-radius: 18px; color: var(--paper); margin-top: .7em; padding: .95em 1.05em; width: 90%; }.reflection h3 { color: var(--seafoam); margin: 0 0 .7em; }.reflection ol { display: grid; gap: .7em; grid-template-columns: repeat(3, 1fr); list-style: none; margin: 0; padding: 0; }.reflection li { color: var(--paper); font-size: .52em; line-height: 1.25; }.reflection li b { color: var(--coral); display: block; font-family: 'DM Mono', monospace; font-size: .8em; margin-bottom: .35em; }
</style>

<!-- .slide: class="cover" data-transition="fade" -->
<div class="eyebrow">Workshop · AI-driven utveckling</div>

# Från första prompt<br>till trygg leverans

<p class="subtitle">Hur man kommer igång med AI i utvecklingsarbetet — utan att bygga en agentfarm först.</p>

<div class="footer">Tydligt mål · litet scope · bra feedback</div>

Note:
Öppna lugnt. Det här är inte en verktygsdemo och inte ett “AI tar jobben”-pass.

Det handlar om att sänka tröskeln för att börja använda AI väl i det vanliga utvecklingsarbetet. Jag vill ge ett språk, några konkreta arbetssätt och erfarenheter från flera olika typer av projekt.

Lova inte en perfekt metod. Säg i stället: “Alla team jobbar olika. Jag vill visa hur man tar ett tryggt första steg och låter arbetssättet växa fram ur verkliga behov.”

---

<div class="eyebrow">Tesen</div>

# Det svåra är sällan<br>att använda AI.

<div class="quote">Det svåra är att våga börja innan man har en perfekt setup.</div>

<p class="lead">Den behöver vi inte vänta på.</p>

Note:
Säg att många blockerar sig själva: “vi måste först ha skills, modellpolicy, intern plattform och rätt verktyg.” De sakerna kan behövas senare, men de är sällan första steget.

Fråga gärna publiken: “Vilken liten uppgift gjorde du senast som du skulle kunna låta AI hjälpa dig att förstå, formulera eller kontrollera?” Det flyttar tanken från transformation till vardag.

Landning: börja i ett verkligt flöde med en tydlig ägare, inte i ett styrgruppsprojekt.

---

<div class="eyebrow">En utvecklingscykel</div>

# AI är inte ett nytt steg.<br>Den finns genom hela flödet.

<div class="cycle">
  <div class="node">Idé</div><div class="arrow">→</div>
  <div class="node agent">Förstå &amp; formulera</div><div class="arrow">→</div>
  <div class="node agent">Bygga</div><div class="arrow">→</div>
  <div class="node agent">Granska</div><div class="arrow">→</div>
  <div class="node">Acceptera &amp; släppa</div>
</div>
<div class="cycle-legend">
  <span><i class="dot dot-human"></i>människan äger riktning</span>
  <span><i class="dot dot-agent"></i>AI accelererar arbete</span>
  <span><i class="dot dot-together"></i>det mesta sker tillsammans</span>
</div>

<div class="quote">AI accelererar varje steg. Människan äger riktning, risk och acceptans.</div>

Note:
Det här är den uppdaterade versionen av development-cycle-bilden.
Poängen är inte att agenten tar över; den avlastar repetitivt och hjälper oss tänka, kontrollera och prova snabbare.

Ta 60–90 sekunder här. Peka på att agenten är aktiv i mitten av flödet, men att idé och acceptans fortfarande måste ha en mänsklig ägare.
Det här är också övergången till din egen erfarenhet: “så här ser min loop ut när jag faktiskt bygger.”

--

<div class="eyebrow">Valbar fördjupning · min loop</div>

# Min utvecklingsloop

<div class="process">
  <div class="phase human"><b>01 · människa</b><strong>Problem &amp; utfall</strong><span>Vad ska bli sant för användaren?</span></div>
  <div class="phase together"><b>02 · tillsammans</b><strong>Formulera</strong><span>Kontext, avgränsning och klart när.</span></div>
  <div class="phase agent"><b>03 · agent</b><strong>Första loop</strong><span>Läser, föreslår, bygger och testar.</span></div>
  <div class="phase together"><b>04 · tillsammans</b><strong>Review</strong><span>Diff, edge cases, produkt och risk.</span></div>
  <div class="phase agent"><b>05 · agent</b><strong>Åtgärda</strong><span>Fångar feedback och kör om kontroller.</span></div>
  <div class="phase human"><b>06 · människa</b><strong>Acceptera</strong><span>PR, release och lärande efteråt.</span></div>
</div>

<div class="quote">Det viktiga är inte att agenten skriver koden. Det viktiga är att loopen gör det lättare att få rätt sak byggd.</div>

Note:
Valbar slide: använd den när publiken vill förstå hur arbetet faktiskt känns i vardagen.

Gå igenom i ett konkret case. Börja med ett problem som “kunden kan inte skapa en faktura utan kund”. Förklara att du inte säger “fixa det”; du beskriver önskat utfall, var den får ändra och vilka tester som ska visas.

Agenten gör en första loop, men den är inte klar för att den har genererat kod. Du tittar på diffen och frågar: löser den rätt problem, är ändringen rimligt liten, saknas något edge case? Sedan får agenten ta hand om feedbacken och köra samma kontroller igen.

Om tiden är knapp: tryck höger från föregående slide och hoppa den här fördjupningen.

---

<div class="eyebrow">Välj nivå med avsikt</div>

# AI är en stege,<br>inte ett hopp.

<div class="ladder">
  <div class="rung"><b>01</b><span>Sök</span><small>Google, docs, forum</small></div>
  <div class="rung"><b>02</b><span>Fråga</span><small>AI-chatt för att förstå och jämföra</small></div>
  <div class="rung"><b>03</b><span>Få hjälp</span><small>IDE-förslag, förklaring och små ändringar</small></div>
  <div class="rung"><b>04</b><span>Delegera</span><small>En kodagent löser en avgränsad uppgift</small></div>
  <div class="rung"><b>05</b><span>Automatisera</span><small>Reversibelt, mätbart och med skyddsnät</small></div>
</div>

<div class="quote">Mognad är inte att alltid välja nivå fem. Mognad är att välja den lägsta nivå som löser uppgiften bra.</div>

Note:
Det finns inget pris för att vara mest agentisk. Ofta är AI-chatten eller IDE-hjälp exakt rätt.
Automation är toppen när den är repetitiv, reversibel och går att övervaka.

Om publiken är ovan vid ämnet: säg att steg fyra och fem inte är målet. De är bara ytterligare alternativ när uppgiften och skyddsnäten motiverar dem.

--

<div class="eyebrow">Valbar fördjupning · gemensamt språk</div>

# Sex ord som räcker<br>för att komma igång.

<div class="glossary">
  <div class="term"><strong>Modell</strong><span>AI-motorn som läser, resonerar och genererar svar eller kod.</span></div>
  <div class="term"><strong>Prompt</strong><span>Uppgiften och den kontext vi ger modellen.</span></div>
  <div class="term"><strong>Effort</strong><span>Hur mycket tid modellen får lägga på att resonera.</span></div>
  <div class="term"><strong>Agent</strong><span>En modell som också kan använda verktyg: läsa, ändra och testa.</span></div>
  <div class="term"><strong>Skill</strong><span>En återanvändbar instruktion för ett arbete som faktiskt återkommer.</span></div>
  <div class="term"><strong>Harness</strong><span>Kontext, regler, verktyg och feedback runt AI:n.</span></div>
</div>

<div class="quote">Högre effort betyder att AI:n får tänka längre. Högre autonomi betyder att den får göra mer.</div>

Note:
Valbar slide för blandade målgrupper. Håll den kort: det här är ingen definitionsövning utan ett sätt att avdramatisera orden.

Den viktigaste distinktionen är effort kontra autonomi. En modell kan få tänka länge på ett svårt problem och ändå bara få lämna ett förslag. Den kan också få utföra ett rutinjobb snabbt, men då bara inom hårda ramar.

Knyt “harness” till ett mänskligt team: samma saker som gör en ny kollega effektiv — dokumentation, verktyg, feedback och tydliga förväntningar — gör agenten effektiv.

---

<div class="eyebrow">Relationen till agenten</div>

# Fråga, samarbeta<br>eller delegera?

<div class="relation">
  <div class="mode"><h3>Fråga</h3><p>Du vill ha ett svar eller ett utkast.</p><div class="example">“Skriv ett mejl som jag kan skicka.”</div></div>
  <div class="mode"><h3>Samarbeta</h3><p>Ni formar lösningen tillsammans; du godkänner nästa steg.</p><div class="example">“Ställ frågorna som saknas och skriv ett mejlförslag.”</div></div>
  <div class="mode"><h3>Delegera</h3><p>Agenten får utföra en tydligt avgränsad handling.</p><div class="example">“Förbered uppdateringen, men skicka först efter mitt godkännande.”</div></div>
</div>

<div class="quote">Behandla agenten som en kompetent ny kollega.</div>

Note:
En bra ny kollega behöver mål, sammanhang, mandat och feedback.

Påpeka skillnaden: att be om ett mejl och att be någon kommunicera externt är olika risknivåer. Var alltid tydlig med vilket mandat som ges. Den normala starten är “förbered, visa mig, sedan beslutar jag” — inte “gör allt själv”.

I kod ser samma mönster ut som: “analysera och föreslå” → “gör en avgränsad ändring” → “öppna en PR när kontrollerna är gröna.”

---

<div class="eyebrow">En bra brief</div>

# Du behöver inte prompta smartare.<br>Du behöver briefa tydligare.

<div class="brief">
  <div><strong>1. Mål</strong><span>Vad ska bli bättre eller klart?</span></div>
  <div><strong>2. Kontext</strong><span>Vad måste agenten veta för att inte gissa?</span></div>
  <div><strong>3. Ramar</strong><span>Vad får den göra — och inte röra?</span></div>
  <div><strong>4. Klart när</strong><span>Hur bevisar vi att resultatet är rätt?</span></div>
  <div><strong>5. Mandat</strong><span>Ska den föreslå, förbereda eller utföra?</span></div>
</div>

<p class="lead" style="margin-top:1.2em">Det är en arbetsbeskrivning, inte magi.</p>

Note:
Exempel från vardagen: “Fixa felet där en faktura kan skapas utan kund. Hitta orsaken och föreslå en plan. Ändra bara validering och relevanta tester. Kör testerna och visa diffen innan du gör något mer.”

Peka på att detta inte är en magisk prompt. Det är samma saker som gör en ticket, en brief till en konsult eller en uppgift till en ny kollega bra.

Om agenten missar: börja med att fråga vilken del som saknades — mål, kontext, ram, acceptanskriterium eller mandat — i stället för att bara prompta om hårdare.

---

<div class="eyebrow">Skepticism är sunt</div>

# Rädslorna är rimliga.<br>Så låt oss designa för dem.

<div class="case-overview skeptic-grid">
  <div class="card"><span class="number">01</span><h3>Jobbet</h3><p>Roller förändras. Omdöme, domänkunskap och ansvar blir mer värdefulla.</p></div>
  <div class="card"><span class="number">02</span><h3>Kontrollen</h3><p>Gör scope, behörighet och godkännanden tydliga — inte implicita.</p></div>
  <div class="card"><span class="number">03</span><h3>Kompetensen</h3><p>AI får inte bli ett sätt att slippa förstå. Review är aktivt lärande.</p></div>
  <div class="card"><span class="number">04</span><h3>Förändringen</h3><p>Börja i befintligt flöde med arbete som du redan äger.</p></div>
</div>

<div class="quote">Målet är inte att lita blint på AI. Målet är att använda den kritiskt.</div>

Note:
Var tydlig med att ingen kan lova att AI aldrig påverkar roller. Det vore oärligt.
Men utvecklares förmåga att förstå system, värdera risk och skapa värde blir inte irrelevant för att kod blir billigare.

Microsoft Research pekar på risk för mindre kritisk ansträngning vid hög tilltro till AI. Det är därför review, förklaringar och medveten träning är viktiga — inte bara snabb output.

Rama in skepticism som en tillgång: den gör att vi ställer bättre krav på arbetssättet.

---

<div class="eyebrow">Fyra resor, samma princip</div>

# Det ser olika ut<br>i olika verkligheter.

<div class="case-overview">
  <div class="card step"><h3>Greenfield</h3><p>Ny produkt från start: forma struktur, test och kontext agentvänligt direkt.</p></div>
  <div class="card step"><h3>Rewrite</h3><p>Nyutveckling i befintlig infrastruktur: AI navigerar bäst med tydligt mandat.</p></div>
  <div class="card step"><h3>Etablerat system</h3><p>Det stora skiftet är i teamets vanor, inte bara i verktyget.</p></div>
  <div class="card step"><h3>Backoffice</h3><p>Domänkunskap + snabb prototyp kan bli en fungerande intern produkt.</p></div>
</div>

<div class="quote">Samma arbetssätt passar inte alla. Samma principer gör det.</div>

Note:
Berätta kort om dina fyra egna case här. Håll dem anonymiserade i grundversionen.

Greenfield: vad händer när man formar kontext, test och struktur agentvänligt från början? Rewrite: hur använder man AI när infrastrukturen, beroendena och intressenterna redan finns? Etablerat system: hur får ett team ett nytt vardagsbeteende? Backoffice: hur mycket längre kommer någon med stark domänkunskap?

Poängen är inte att jämföra projekten. Poängen är att ingen av dem behöver samma setup för att få nytta.

--

<div class="eyebrow">Case 1 · greenfield</div>

# När allt är nytt<br>är kontexten produkten.

<div class="case-lens">
  <div class="lens"><h3>Utgångspunkt</h3><p>Tomt repo, högt tempo och få tidigare beslut att luta sig mot.</p></div>
  <div class="lens"><h3>AI möjliggjorde</h3><p>Snabba vertikala skivor: struktur, UI, test och iteration i samma loop.</p></div>
  <div class="lens"><h3>Det som krävdes</h3><p>Tydliga regler, testbarhet och beslut som går att hitta igen.</p></div>
</div>

<div class="quote">I ett greenfield-projekt är det lätt att bygga fort. Därför måste du tidigt göra det lätt att förstå vad som redan finns.</div>

Note:
Använd ditt greenfield-case här. Berätta i tre akter på ungefär tre minuter:

1. Vad var målet och varför behövde ni röra er snabbt?
2. Vad gjorde AI konkret snabbare — till exempel första fungerande flödet, test, UI eller förändring efter feedback?
3. Vad lärde ni er om kontext? När det inte finns gammal dokumentation måste ni skapa en tydlig kodstruktur, enkla startkommandon och några få levande regler från början.

Viktigt: låt inte detta låta som “AI skrev allt åt oss”. Berätta vad du fortfarande gjorde: valde problem, satte riktning, testade och bestämde när något var klart.

--

<div class="eyebrow">Case 2 · rewrite i etablerad miljö</div>

# AI kan röra sig snabbt<br>i en gammal värld.

<div class="case-lens">
  <div class="lens"><h3>Utgångspunkt</h3><p>Befintlig infrastruktur, beroenden och många människor med legitim input.</p></div>
  <div class="lens"><h3>AI möjliggjorde</h3><p>Snabbare förståelse av kod, tydligare alternativ och kortare loopar i nyutveckling.</p></div>
  <div class="lens"><h3>Det som krävdes</h3><p>Tydligt mandat: vad ändras, vad är skyddat och vem accepterar?</p></div>
</div>

<div class="quote">AI tar inte bort komplexitet i organisationen. Den gör det billigare att utforska den.</div>

Note:
Använd rewrite-caset. Börja med kontrasten mot greenfield: här är koden bara en del av systemet. Infrastruktur, historik, beroenden, säkerhet och människor måste alla få plats i briefen.

Berätta om ett läge där AI hjälpte dig att snabbt skapa en karta: hitta relaterad kod, jämföra gamla och nya flöden eller formulera en plan. Berätta sedan om motdraget: du gjorde inte en bred ändring förrän mandat, scope och acceptanskriterier var tydliga.

Poängen för publiken är att AI inte kräver ett nytt och rent system. Men den belönar god avgränsning extra mycket i äldre miljöer.

--

<div class="eyebrow">Case 3 · etablerat system</div>

# Det största skiftet<br>är inte i koden.

<div class="case-lens">
  <div class="lens"><h3>Utgångspunkt</h3><p>Ett system och ett team med invanda sätt att analysera, bygga och diskutera.</p></div>
  <div class="lens"><h3>AI möjliggjorde</h3><p>Fler iterationer, mindre friktion och mer fokus på produktbeslut än tangenttryckningar.</p></div>
  <div class="lens"><h3>Det som krävdes</h3><p>Nya vanor: visa diff, testa, dela lärdomar och involvera fler.</p></div>
</div>

<div class="quote">Ett nytt verktyg förändrar inte ett team. Nya vanor gör det.</div>

Note:
Använd CMS-/förändringscaset. Det viktiga här är inte en specifik modell utan en vardagsförflyttning.

Beskriv före/efter med ett konkret beteende: kanske att någon tidigare satt länge själv med implementation, medan teamet nu snabbare kan prova, se ett fungerande resultat och diskutera det verkliga beteendet.

Var också ärlig med friktionen: en del behöver stöd för att komma igång, andra går för fort, och teamet måste skapa ett sätt att dela goda exempel utan att standardisera allt för tidigt.

--

<div class="eyebrow">Case 4 · affärsnära backoffice</div>

# Domänkunskap blir<br>byggkapacitet.

<div class="case-lens">
  <div class="lens"><h3>Utgångspunkt</h3><p>Ett konkret internt problem, många små detaljer och hög kunskap om verksamheten.</p></div>
  <div class="lens"><h3>AI möjliggjorde</h3><p>Snabb väg från arbetsflöde och behov till en fungerande intern produkt.</p></div>
  <div class="lens"><h3>Det som krävdes</h3><p>Affärsregler och undantag behöver verifieras.</p></div>
</div>

<div class="quote">Lägre byggkostnad gör domänkunskap mer värdefull.</div>

Note:
Använd backoffice-caset. Här får du visa den kanske mest konkreta affärseffekten: någon som verkligen förstår processen kan komma ovanligt långt, snabbt.

Berätta om ett riktigt arbetsflöde, inte en teknikdetalj. Vad var den manuella friktionen? Vad blev bättre när det fanns en fungerande vy eller process? Vilka regler behövde fortfarande en människa kontrollera?

Landning: AI demokratiserar en del av byggandet, men den demokratiserar inte automatiskt omdöme. Domänkunskap och kvalitetssäkring blir därför centrala.

---

<div class="eyebrow">Första veckan</div>

# Gör första steget<br>löjligt litet.

<div class="grid-2" style="margin-top:.75em">
  <div class="card"><span class="number">01</span><h3>Välj ett riktigt jobb</h3><p>En bugg, liten feature, testsvit, migration eller intern vy. Något som redan har en ägare.</p></div>
  <div class="card"><span class="number">02</span><h3>Gör “klart” konkret</h3><p>Vad ska fungera? Vad får inte påverkas? Vilka tester visar att det blev rätt?</p></div>
  <div class="card"><span class="number">03</span><h3>Gör det tryggt att prova</h3><p>Tydliga ramar för kod, data och hemligheter. Samma vanliga PR- och testflöde.</p></div>
  <div class="card"><span class="number">04</span><h3>Prata om resultatet</h3><p>Vad hjälpte? Vad blev fel? Vad gör vi annorlunda nästa gång?</p></div>
</div>

Note:
DORA pekar på just detta: AI förstärker det teamet redan har. Snabba feedbackloopar och välfungerande skyddsnät ger nytta; annars blir högre förändringstakt instabilitet.

Gör detta handfast: välj en person, ett repo och en uppgift. Bestäm hur “klart” ska bevisas. Prova. Prata om resultatet innan ni skalar något.

Det är viktigt att första försöket inte blir en hemlig individuell genväg. Dela gärna både det som fungerade och det som blev fel.

--

<div class="eyebrow">Publikreflektion · 3 minuter</div>

# Vilket är ert<br>första riktiga jobb?

<div class="reflection">
  <h3>Ta två minuter själv eller två och två.</h3>
  <ol>
    <li><b>01</b>Vilken återkommande uppgift skaver mest i ert vanliga flöde?</li>
    <li><b>02</b>Vad är minsta säkra scope där ni skulle kunna prova AI?</li>
    <li><b>03</b>Vad måste ni se eller testa för att våga säga “klart”?</li>
  </ol>
</div>

<div class="quote">Målet är inte en stor idé. Målet är en uppgift ni kan prova nästa vecka.</div>

Note:
Säg: “Ta två minuter. Skriv gärna ned en uppgift — inte ett AI-initiativ — som ni redan äger och som återkommer.”

Ge publiken ungefär 90 sekunder i tystnad eller parvis samtal. Fråga sedan två personer eller två bord om vad de kom fram till. Hjälp dem att göra scope mindre om de väljer något stort som “modernisera systemet”.

Om tiden är knapp: gör detta som en retorisk fråga från huvudsliden i stället för en övning.

---

<div class="eyebrow">Spara energin</div>

# Du behöver inte detta<br>första veckan.

<div class="grid-3 autonomy-grid" style="margin-top:.9em">
  <div class="card"><span class="number">×</span><h3>Ett stort skillbibliotek</h3><p>Spara först sådant som faktiskt har hjälpt i flera riktiga uppgifter.</p></div>
  <div class="card"><span class="number">×</span><h3>En agentfarm</h3><p>Flera agenter skapar lätt mer koordinering och review än arbete.</p></div>
  <div class="card"><span class="number">×</span><h3>En egen plattform</h3><p>Bygg gemensam infrastruktur när den löser ett bevisat återkommande problem.</p></div>
</div>

<div class="quote">Vi ska inte bygga en AI-fabrik innan vi har lärt oss använda en bra skruvdragare.</div>

Note:
Var lite lätt här. Folk känner igen sig i överambitiösa transformationsprogram.
Säg att skills och plattformar kan vara fantastiska — när de växer fram ur verkliga mönster.

En skill är rimlig när samma instruktion redan har hjälpt flera gånger. En intern plattform är rimlig när flera team fastnar i exakt samma friktion. Före det är de ofta bara en avancerad gissning.

---

<div class="eyebrow">Autonomi är inte effort</div>

# Låt AI:n tänka längre.<br>Inte nödvändigtvis göra mer.

<div class="grid-3" style="margin-top:.9em">
  <div class="card"><h3>Hög effort</h3><p>Passar svår felsökning, design och komplex analys.</p><p class="micro">Mer resonemang</p></div>
  <div class="card"><h3>Litet scope</h3><p>Håll ändringen begriplig, testbar och möjlig att reviewa.</p><p class="micro">Mindre blast radius</p></div>
  <div class="card"><h3>Tydligt mandat</h3><p>Matcha behörighet och nästa handling med den faktiska risken.</p><p class="micro">Kontroll där den behövs</p></div>
</div>

<div class="quote">Höj inte autonomin snabbare än er förmåga att förstå, reviewa och backa förändringen.</div>

Note:
Det här är centralt. En starkare modell med mer reasoning är inte samma sak som att låta den ändra fler system eller skicka saker utan kontroll.

Ett bra exempel är en svår produktionsbugg: ge agenten mer tid att undersöka loggar, kod och hypoteser, men låt den först föreslå en plan. Ge den inte automatiskt mandat att ändra fem tjänster.

Zalando har sett stora PR:er och ökande komplexitet som följd av agentiskt arbete utan tillräcklig anpassning av review. Autonomi behöver därför växa med teamets kontrollsystem.

---

<div class="eyebrow">Kvalitet som system</div>

# Review är inte sista steget.<br>Den är det som gör att vi kan gå fort.

<div class="review">
  <div class="gate"><strong>Agenten</strong><span>Läser diffen<br>kör tester<br>kontrollerar krav</span></div><div class="chevron">→</div>
  <div class="gate"><strong>Automatik</strong><span>CI<br>typer &amp; lint<br>säkerhetskontroll</span></div><div class="chevron">→</div>
  <div class="gate"><strong>Andra ögon</strong><span>AI-review<br>konventioner<br>edge cases</span></div><div class="chevron">→</div>
  <div class="gate final"><strong>Människan</strong><span>Produktnytta<br>domänlogik<br>risk &amp; acceptans</span></div>
</div>

<div class="quote">AI-genererad kod är ett förslag, inte ett resultat.</div>

Note:
AI review är inte en ersättning för ansvar. Den gör mänsklig review mer värdefull genom att avlasta summering, enkla konventionsbrott och repetitiva kontroller.

Människan lägger då sin tid där den betyder mest: är detta rätt problem, fungerar det i kundens verklighet, vad är den svåra edge casen och är risken rimlig?

GitHub rekommenderar kombinationen av AI-review och mänsklig review. Gör gärna detta till er miniminivå i stället för att försöka ersätta review.

---

<div class="eyebrow">En realistisk start</div>

# 90 dagar.<br>Inte en transformation.

<div class="timeline">
  <div class="phase"><h3>Dag 1–30<br>Bygg vana</h3><p>Trygga verktyg, enkla ramar, verkliga pilotuppgifter och en gemensam retro.</p></div>
  <div class="phase"><h3>Dag 31–60<br>Dela lärande</h3><p>Visa ett bra case och ett misslyckande. Spara de få instruktioner som faktiskt återkommer.</p></div>
  <div class="phase"><h3>Dag 61–90<br>Höj där det bevisats</h3><p>Automatisera ett lågriskmönster. Förbättra repo-kontekst och testbarhet där det hjälper.</p></div>
</div>

<div class="quote">Målet är inte ett identiskt arbetssätt för alla. Målet är fler team som tryggt kan använda AI i sin vardag.</div>

Note:
Understryk “varje team är olika”. Den delade basnivån är kvalitet och lärande, inte exakt verktyg eller promptformat.

Efter 30 dagar vill vi veta om folk vågar använda verktygen. Efter 60 dagar vill vi veta vilka uppgifter som återkommer och vilka instruktioner som har hjälpt. Efter 90 dagar kan vi automatisera en liten, lågriskuppgift där vi faktiskt har bevis.

Det är en resa som bygger förtroende, inte ett program som försöker tvinga fram entusiasm.

---

<!-- .slide: class="cover" -->
<div class="eyebrow">Ta med dig detta</div>

# Sänk tröskeln<br>för att börja.

<div class="quote" style="color:var(--paper);border-color:var(--coral)">Men höj inte risknivån i samma andetag.</div>

<p class="subtitle"><strong style="color:var(--seafoam)">1.</strong> Börja med verkligt arbete.<br><strong style="color:var(--seafoam)">2.</strong> Matcha autonomi med risk.<br><strong style="color:var(--seafoam)">3.</strong> Gör lärandet delat.</p>

<div class="footer">Frågor</div>

Note:
Låt denna ligga kvar för frågor.
Summera i en mening: AI ska inte göra teamet mindre ansvarigt, den ska frigöra mer av vår uppmärksamhet till de svåra besluten.

Om du vill öppna frågor: “Vilken del av ert vanliga flöde skulle ni vilja göra lättare att prova AI i — utan att höja risken?”

---

<div class="eyebrow">Research och vidare läsning</div>

# Underlag bakom<br>rekommendationerna

<div class="source-list">
  <a href="https://cloud.google.com/blog/products/ai-machine-learning/announcing-the-2025-dora-report?e=48754805"><span>DORA 2025</span><br>AI förstärker teamets befintliga system och feedbackloopar.</a>
  <a href="https://engineering.zalando.com/posts/2026/08/agentic-engineering-at-zalando-a-snapshot.html"><span>Zalando</span><br>Verktygsfrihet, delat lärande och lärdomar om PR-storlek/review.</a>
  <a href="https://openai.com/index/harness-engineering/"><span>OpenAI</span><br>Agent-first kräver kontext, tester och arkitektoniska gränser.</a>
  <a href="https://docs.github.com/en/enterprise-cloud@latest/copilot/tutorials/review-ai-generated-code"><span>GitHub</span><br>AI-review kompletterar mänsklig review.</a>
  <a href="https://www.microsoft.com/en-us/research/publication/the-impact-of-generative-ai-on-critical-thinking-self-reported-reductions-in-cognitive-effort-and-confidence-effects-from-a-survey-of-knowledge-workers/"><span>Microsoft Research</span><br>Kritisk användning är viktig för att motverka överberoende.</a>
  <a href="https://www.pacingthefrontier.com/"><span>Pacing the Frontier</span><br>Kapacitet behöver följas av förmåga att förstå och styra konsekvenser.</a>
</div>

Note:
Den här sliden är främst för distribution efter workshopen. Hoppa över den i talet om tiden är knapp.
