# Recurs Educatiu: La Unió Europea (Cicle Superior de Primària)

**Recurs web educatiu d'una sola pàgina (Single-Page Application)** desenvolupat amb criteri pedagògic per a l'àrea de **Llengua Catalana** (Comprensió Lectora) amb contingut transversal de Ciències Socials sobre la **Unió Europea**, dissenyat per a l'alumnat de **5è i 6è de primària**.

---

## 🎯 Objectius pedagògics i curriculars

- **Nivell educatiu:** Cicle Superior d'Educació Primària (10 - 12 anys).
- **Matèria principal:** Llengua Catalana i Literatura (Competència en Comunicació Lingüística).
- **Matèria transversal:** Coneixement del Medi Natural, Social i Cultural (Ciències Socials i Educació per a la Ciutadania).
- **Marc normatiu:** Decret 175/2022 d'ordenació dels ensenyaments de l'educació bàsica (Catalunya).
- **Competències clau:**
  - **CCL (Comunicació lingüística):** Desenvolupament de la comprensió lectora mitjançant la localització d'informació explícita (preguntes literals) i la deducció de significats, intencions i relacions de causa-efecte (preguntes inferencials).
  - **CC (Competència ciutadana):** Comprensió dels valors de convivència pacífica, democràcia, drets humans, solidaritat i diversitat lingüística i cultural a Europa.
  - **CD (Competència digital):** Ús autònom d'un recurs tecnològic interactiu respectuós amb la privadesa.
  - **CPSAA (Aprendre a aprendre):** Regulació de l'aprenentatge a través del tractament constructiu de l'error mitjançant pistes pedagògiques.

---

## 🚀 Com provar el recurs en local

Aquest projecte ha estat creat com una aplicació estàtica **100% autònoma**, sense necessitat de compilar ni instal·lar paquets `npm`.

### Opció A: Doble clic directe
1. Obre la carpeta del projecte: `C:\Users\pberrozp\.gemini\antigravity\scratch\recurs-ue-llengua-primaria`.
2. Fes doble clic sobre el fitxer `index.html`.
3. S'obrirà immediatament al teu navegador preferit (Chrome, Firefox, Safari, Edge) i funcionarà perfectament, fins i tot sense connexió a Internet.

### Opció B: Amb un servidor web local
Pots utilitzar qualsevol servidor web lleuger des del terminal:
```bash
# Amb Python 3:
cd C:\Users\pberrozp\.gemini\antigravity\scratch\recurs-ue-llengua-primaria
python -m http.server 8000
# Després obre al navegador: http://localhost:8000
```
O utilitzar l'extensió *Live Server* de Visual Studio Code.

---

## 🌐 Com publicar a GitHub Pages (en 3 passos)

El projecte disposa de l'`index.html` a l'arrel, de manera que està preparat per a desplegament immediat:

1. **Crear el repositori a GitHub:**
   - Ves a [GitHub](https://github.com) i crea un nou repositori (ex: `recurs-ue-primaria`).
2. **Pujar el codi:**
   ```bash
   cd C:\Users\pberrozp\.gemini\antigravity\scratch\recurs-ue-llengua-primaria
   git init
   git add .
   git commit -m "Versió inicial: recurs educatiu accessible UE per a primària"
   git branch -M main
   git remote add origin https://github.com/EL-TEU-USUARI/recurs-ue-primaria.git
   git push -u origin main
   ```
3. **Activar GitHub Pages:**
   - Dins del teu repositori a GitHub, ves a **Settings** > **Pages**.
   - A l'apartat **Build and deployment**, a **Branch**, selecciona la branca `main` i la carpeta `/ (root)`.
   - Fes clic a **Save**. En un parell de minuts tindràs l'enllaç públic llest per compartir a l'aula (per exemple: `https://el-teu-usuari.github.io/recurs-ue-primaria/`).

---

## 📋 Justificació del compliment dels requisits

### 1. Protecció de dades (RGPD / Menors d'edat) i Exportació PDF
- **Identificació respectuosa:** Es demana només el nom de pila o un àlies/pseudònim escolar i el grup-classe.
- **Sobirania de les dades:** Totes les dades es processen i s'emmagatzemen exclusivament a la memòria local del navegador (`sessionStorage`). **No s'envia cap dada a servidors externs, bases de dades remotes o eines analítiques de tercers.**
- **Exportació autònoma en .PDF:** S'incorpora un botó d'exportació directa a PDF (`jspdf.umd.min.js` emmagatzemat localment al projecte). La generació del document A4 es realitza íntegrament a la màquina de l'alumne, sense pujar cap dada a serveis de tercers.
- **Botó de reinici i esborrament:** L'alumnat pot buidar les seves dades en qualsevol moment amb un sol clic.

### 2. Accessibilitat web (WCAG 2.1 Nivell AA)
- **Estructura semàntica:** Ús estricte d'elements HTML5 (`<header>`, `<main>`, `<nav>`, `<aside>`, `<fieldset>`, `<legend>`, `<label>`).
- **Navegació per teclat:** Tots els botons, controls i opcions tenen focus visible destacat (`:focus-visible` amb vora d'alt contrast).
- **Independència del color:** Els estats d'encert, pista i error es transmeten mitjançant canvi d'icona (✓, 💡, ✗), text explícit i canvis d'estil geomètric de les targetes, mai únicament per color.
- **Ràtios de contrast:** Tots els colors principals compleixen sobradament el ràtio 4.5:1 exigit per la pauta WCAG AA. S'inclou a més un mode d'**Alt Contrast** accessible des de la capçalera.
- **Lectors de pantalla:** S'incorporen regions actives `aria-live="polite"` que informen automàticament a les persones que utilitzen lectors de pantalla de la retroacció i canvis de pregunta.

### 3. Disseny Universal per a l'Aprenentatge (DUA)
- **Múltiples formes de representació:**
  - Text estructurat amb iconografia clara per seccions.
  - **Lectura en veu alta (Text-to-Speech):** Síntesi de veu integrada per a cada paràgraf i pregunta en llengua catalana.
  - **Glossari de vocabulari clau:** Termes destacats al text que obren finestres explicatives de conceptes com *Schengen*, *solidaritat*, *Parlament*, etc.
  - **Selector de tipografia per a dislèxia / alta llegibilitat:** Augment d'interlineat i espaiat de caràcters.
  - **Visualitzador dividit (Split-Screen):** El text de lectura es manté accessible al costat del qüestionari per reduir la sobrecàrrega de la memòria de treball de l'alumnat.
- **Múltiples formes d'acció i expressió:** Progrés visualitzable pas a pas mitjançant un mapa interactiu de 10 nodes.
- **Múltiples formes de compromís:** Retroacció formativa i no punitiva que fomenta la mentalitat de creixement.

### 4. Rigor pedagògic, retroacció i combinació de formats (Test + Escriptura)
- **Combinació de formats (Reconeixement vs. Evocació activa):**
  - **6 Preguntes tipus test (Selecció múltiple amb 4 opcions):** Treballen la discriminació visual, la lectura selectiva i l'anàlisi d'opcions distractores plausibles.
  - **4 Preguntes d'escriure (Resposta curta / construïda):** L'alumnat ha de redactar directament paraules clau, sintagmes o frases del text (*«Units en la diversitat»*, *«l'euro»*, *«el carbó i l'acer»*, *«solidaritat»*). Treballen l'evocació activa, la precisió lèxica i l'ortografia.
- **Validació intel·ligent i flexible de les respostes escrites:**
  - El motor d'autocorrecció normalitza la resposta eliminant puntuació innecessària, espais sobrers i aplicant tolerància als accents diacrítics (per evitar que un error d'accentuació frustri l'alumne en una tasca de comprensió conceptual).
  - Alhora, la retroacció mostra sempre la **«Resposta model»** amb l'ortografia i accentuació normatives correctes com a referent d'aprenentatge.
- **Bateria de 10 preguntes curriculars equilibrades:**
  - **5 Preguntes literals:** Localització directa de dades al text (lema de la UE, data del Dia d'Europa, membres del Parlament, moneda euro, simbolisme de les 12 estrelles).
  - **5 Preguntes inferencials:** Deducció de motius històrics (carbó i acer com a prevenció de guerres), interpretació de valors en context (què implica la solidaritat en cas de catàstrofes), aplicació a situacions reals (beneficis per a una estudiant), lliure circulació Schengen i pensament crític democràtic (importància del sufragi universal).
- **Mecànica formativa de dos intents:**
  - *Primer error:* No revela la resposta correcta. Mostra una pista pedagògica reflexiva que guia l'alumnat cap al paràgraf clau i permet un segon intent.
  - *Segon error:* Es comptabilitza com a fallada definitiva, mostra la resposta correcta esperada en contrast amb el que ha escrit/triat l'alumne i ofereix una explicació didàctica detallada.
  - *Encert al 1r intent:* Atorga 10 punts i reforça el motiu de l'encert.
  - *Encert al 2n intent:* Atorga 5 punts i felicita l'aprofitament de la pista.

### 5. Recursos i dependències
- **Zero dependències externes:** No s'utilitzen frameworks feixucs (com Bootstrap, Tailwind o React) ni biblioteques de tercers mitjançant CDN que puguin fallar si s'aplica una política de xarxa escolar restrictiva o si no hi ha connexió a Internet.
- Les icones s'han incorporat mitjançant caràcters universals Unicode i emojis estandarditzats.

### 6. Codi i transparència sobre l'ús d'IA
- Codi modular i netament comentat en català (`index.html`, `css/styles.css`, `js/quiz-data.js`, `js/app.js`).
- **Nota de transparència sobre la IA:** Accessible a la pròpia aplicació (botó "Docent / IA") i detallada en aquest document. La IA s'ha utilitzat com a eina d'assistència per a l'estructuració tecnològica del codi i la proposta de preguntes inicials, amb una **revisió docent estricta** per garantir l'adequació del llenguatge a 5è-6è de primària, el rigor històric i la idoneïtat de les pistes pedagògiques.

---

## 🗂️ Estructura del projecte

```text
recurs-ue-llengua-primaria/
│
├── index.html            # Pàgina principal del recurs (aplicació autònoma)
├── README.md             # Documentació tècnica i pedagògica
├── css/
│   └── styles.css        # Estils accessibles, variables DUA, alt contrast i impressió
└── js/
    ├── quiz-data.js      # Text de lectura, glossari i preguntes amb pistes i explicacions
    └── app.js            # Lògica interactiva, gestió d'intents, accessibilitat i TTS
```

---

## 📄 Llicència

Aquest recurs es distribueix sota una llicència **Creative Commons Reconeixement-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)** per afavorir el seu ús lliure i compartit en l'àmbit escolar.
