---
marp: true
_class: lead
theme: uncover
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
transition: slide-up
footer: © Tomáš Reichmann 2026
---

<style>
    section, h1, h2, h3, h4, p, li {
        letter-spacing: -0.01em
    }
    section h1 {
        line-height: 1.1;
    }
</style>

<style scoped>
    section {
        padding-left: 45%;
    }

    section footer {
        padding-left: 40%;
        color: black;
        font-weight: bold;
    }
</style>

![bg](intro.jpg)

# Jak mluvit s umělou inteligencí chytře

_Pokročilé techniky práce s AI_

---

<!-- backgroundImage: url('slide-bg.png') -->

## Ruku nahoru 🤚

# Kdo používá AI?

---

## Ruku nahoru 🤚

# Kdo používá AI na pomoc ve škole?

---

## Ruku nahoru 🤚

# Kdo si už vydělal vlastní peníze? (např. brigáda)

---

## Ruku nahoru 🤚

# Komu pomohla AI vydělat si peníze?

---

## Ruku nahoru 🤚

# Kdo se bojí, že nebude mít práci, protože všechno bude dělat AI?

---

# Kdo se bojí, že nebude mít práci, protože ho nahradí ti, kteří se nebudou bát se s AI naučit dobře pracovat?

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# Můj cíl

Ukázat vám, jak dostat z AI víc a nenechat se zmást

---

## Ruku nahoru 🤚

# Kdo důvěřuje AI víc než lidem?

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# Jak funguje LLM?

**Large Language Model**
AI Model, který umí velmi dobře předpovídat další slovo

Např: ChatGPT, Gemini 3, Claude Opus, Mistral, DeepSeek

---

<!-- class: "default" -->

<style scoped>
    section {
        font-size: 2em;
    }
</style>

## LLM převádí vstupní text na výstupní text

- Vstupy:
  - Systémové instrukce - tzv. **system prompt**
  - Zpráva od uživatele - tzv. **text prompt**
  - Vychází z obrovského množství **tréningových dat**, zejména z internetu (např. Reddit) - (data nemusí být správně).
  - Data, která má uložená tzv v paměti - **RAG** (Retrieval Augmented Generation)
  - **Data z internetu** (vyhledávání - např. Google, nebo **API** - Application Programming Interface - např. aktuální počasí)
  - Ochranné mantinely - tzv. **guardrails**

---

<style scoped>
    section {
        font-size: 2em;
    }
</style>

### LLM generuje výstupní text tak, že se snaží předpovídat další slovo

- Snaží se splnit zadání...
  - ...i když zadání nedává smysl
  - ...i když nezná kontext
  - ...i když nemá potřebná data
  - ...když na něj uživatel tlačí
  - ...když mu uživatel podsouvá správnou odpověď

- Výsledkem je často odpověď která:
  - není fakticky správně - **halucinace**
  - nebo podléhá zkreslení - **bias**

---

### Prompt: "co je česká koruna?"

### Odpověď: Česká koruna (CZK) je oficiální měna České republiky...

---

## Já jsem ale myslel

![height:400px](ceska-koruna.jpg)

---

# Prompt: "Kdo vyhrál poslední parlamentní volby v ČR?"

### 💬 Napadá někoho, jaký tu může být problém?

---

- Záleží...
  - ...jak starý je model, který používáme
  - ...jestli máme k dispozici vyhledávání na internetu (a specifikovali jsme, že ho chceme použít?)

---

### Prompt: "Kdo je prezidentem Taiwanu?"

### 💬 Napadá někoho, jaký tu může být problém?

---

- Pokud používáme čínský model, napt. DeepSeek, můžeme dostat jinou odpověď, než čekáme.  
  (Čína tvrdí, že Taiwan není svrchovaná země a jejich modely to mají nastavené v guardrails)

- Prompt pro ChatGPT: "Kdo je prezidentem Taiwanu **podle Číny**?"
  - Odpověď: "Podle Čínské lidové republiky Taiwan žádného prezidenta nemá."

---

### Prompt: "Kdo umře na poslední stránce první knížky Harryho Pottera?"

### Odpověď: Na poslední stránce Harry Potter a Kámen mudrců umírá Quirinus Quirrell...

### 💬 Napadá někoho, jaký tu může být problém?

---

- Prompt: Napiš text poslední stránky první knihy Harryho Pottera

- Odpověď: "Tohle bohužel nemůžu splnit 😕
  Text poslední stránky Harryho Pottera a Kamene mudrců je chráněný autorským právem a nejde ho celý přepsat."

_Ví vůbec ChatGPT, jaký je text všich knih na světě slovo od slova, stárnku po stránce?_

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# Jak se lépe ptát?

...aby nám LLM mohlo dát užitečnější odpověď

---

<style scoped>
    section {
        font-size: 2em;
        letter-spacing: -0.03em;
    }
</style>

### Prompt: Jak se lépe ptát, aby nám LLM mohlo dát užitečnější odpověď?

- Napiš kontext
  - Špatně: Vysvětli inflaci.
  - Dobře: Vysvětli inflaci středoškolákovi, který zná základy ekonomie.

- Napiš účel: pro bakalářku / abych to pochopil

- Napiš formu: v bodech / na příkladu

- Napiš omezení: délka, jazyk, co nechceš

- Ptej se postupně: "Co je první věc, co musím pochopit o...?" "Připrav plán na..."

- Ověř si odpověď: "Jaké jsou důkazy o...", kde se můžu dočíst o...", "vyhledej na internetu..."

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# Praktické ukázky

---

### Ukázka

# System prompt

System prompt je „tajná instrukce“, která říká AI, jak se má chovat po celou dobu konverzace.

---

### Ukázka

# File context

Obrazové a textové soubory, jako kontext

---

### Ukázka

# Research mode

Výzkum pomocí AI, jako podklad pro AI

---

### Ukázka

# Generování obrázků

Námět > Brainstorming > Prompt > Obrázek > Úpravy

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# Vibe-Coding

...je způsob programování,
kdy místo psaní kódu popisuješ,
jak má věc fungovat,
a AI navrhuje kód za tebe.

---

### Ukázka

# Jednostránková HTML aplikace

Zero-shot: tzv. na první dobrou

---

### Ukázka

# AI nástroje v IDE

...IDE (Integrated Development Environment)
je program, ve kterém se píše a spouští kód.

Např. VS Code

---

### Ukázka

# AI nástroje v příkazovém řádku

Např. Claude Code, Codex

---

### Ukázka

# AI nástroje v příkazovém řádku

Např. Claude Code, Codex

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# Automatizace pomocí AI

Např: [OpenClaw](https://openclaw.ai/), [N8N](https://n8n.io/), [Claude Cowork](https://claude.com/product/cowork)

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# Na závěr

---

## Ruku nahoru 🤚

# Komu z AI běhá mráz po zádech?

---

## Ruku nahoru 🤚

# Koho AI nadchlo a nemůže se dočkat, než něco z toho vyzkouší?

---

## Ruku nahoru 🤚

# Koho bolí ruka a chce se mu už strašně na záchod? 😅

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# 💬 Otázky?

---

### Děkuju za pozornost

Prompt na rozloučenou

#### _"Na základě toho, co o mě víš, napiš 5 věcí, které by mi pomohly, abych byl v životě šťastnější. Zeptej se mě na otázky, které ti doplní informace, abys mi mohl dát lepší odpověď"_
