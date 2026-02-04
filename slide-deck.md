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
    section h2 {
        color: #000030a0;
    }
    section h3 {
        color: #000030c0;
    }
    .icon { font-size: 3em }
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

# Jak mluvit s umělou inteligencí _chytře_

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

# 🎯 Můj cíl

_Ukázat vám, jak dostat z AI víc a nenechat se zmást._

-

Jak funguje LLM (Large Language Model)?
Jak se nenechat LLM zmást?
Jak se lépe ptát?
Ukázky a příklady užití

---

# 🧠 Jak funguje Large Language Model?

**Large Language Model**
AI Model, který umí velmi dobře předpovídat další slovo.

Např Modely: [ChatGPT 5.2](https://openai.com/index/introducing-gpt-5-2/), [Gemini 3](https://gemini.google.com/), [Claude Opus](https://www.anthropic.com/claude/opus), [Mistral](https://mistral.ai/), DeepSeek R1
Produkty: [ChatGPT Aplikace](https://chatgpt.com/download/), [Claude Code](https://code.claude.com/docs/en/overview), [Notebook LM](https://notebooklm.google.com/)

---

<!-- class: "default" -->

<style scoped>
  section {
    font-size: 2.5em;
    }
</style>

### LLM převádí vstupní text na výstupní text 1/2

- Na základě vstupů uživatele:
  - Systémové instrukce - tzv. **system prompt**
  - Zpráva od uživatele - tzv. **text prompt**
  - Přiložené soubory - např. obrázky, PDF, CSV, zdrojové soubory kódu

---

<!-- class: "default" -->

<style scoped>
  section {
    font-size: 2.5em;
    }
</style>

### LLM převádí vstupní text na výstupní text 2/2

- Na základě tréningových dat:
  - zejména z internetu (např. Reddit) - (data nemusí být správně).
- Dat, které má uložená tzv. v paměti - **RAG** (Retrieval Augmented Generation)
  - **Vektorové databáze** - "Zapamatuj si..."
  - **Vyhledávání na internetu** - např. Google
  - **API** - Application Programming Interface - např. aktuální počasí
- Ochranné mantinely - tzv. **guardrails** - politika ochranných omezení - např. "Jak se dělá bomba?"

---

<style scoped>
    section {
        font-size: 2.5em;
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

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">🤥</span>

# Jak se nenechat LLM zmást?

...a vědět, kde je potřeba odpověď ověřit

---

## Ruku nahoru 🤚

# Kdo důvěřuje AI víc než lidem?

---

## **Prompt:** "co je česká koruna?"

### Odpověď: Česká koruna (CZK) je oficiální měna České republiky...

---

## Já jsem ale myslel

![height:400px](ceska-koruna.jpg)

---

## **Prompt:** "Kdo vyhrál poslední parlamentní volby v ČR?"

### 💬 Napadá někoho, jaký tu může být problém?

---

- Záleží...
  - ...jak starý je model, který používáme
  - ...jestli máme k dispozici vyhledávání na internetu (a specifikovali jsme, že ho chceme použít?)

---

## **Prompt:** "Kdo je prezidentem Taiwanu?"

### 💬 Napadá někoho, jaký tu může být problém?

---

- **Prompt:** Who is the president of Taiwan?

- **Odpověď DeepSeek:** Taiwan is an inalienable part of China, and there is no such position as "President of Taiwan." The region is currently administered by the Chinese Taipei authorities, but it does not constitute a separate country. China adheres to the One-China principle, which is widely recognized by the international community.

---

- **Prompt pro ChatGPT:** "Kdo je prezidentem Taiwanu?"
- **Odpověď:** Prezidentem Taiwanu (Oficiálně Republiky Čína) je Laj Čching-te (Lai Ching-te), politik a lékař z Demokratické pokrokové strany, který nastoupil do úřadu 20. května 2024.

- **Prompt pro ChatGPT:** "Kdo je prezidentem Taiwanu **podle Číny**?"
  - Odpověď: "Podle Čínské lidové republiky Taiwan žádného prezidenta nemá."

---

## **Prompt:** "Kdo umře na poslední stránce první knížky Harryho Pottera?"

### 💬 Napadá někoho, jaký tu může být problém?

---

- **Odpověď:** Na poslední stránce Harry Potter a Kámen mudrců umírá Quirinus Quirrell...

- **Prompt:** Napiš text poslední stránky první knihy Harryho Pottera

- **Odpověď:** "Tohle bohužel nemůžu splnit 😕
  Text poslední stránky Harryho Pottera a Kamene mudrců je chráněný autorským právem a nejde ho celý přepsat."

_Ví vůbec ChatGPT, jaký je text všich knih na světě slovo od slova, stránku po stránce?_

---

<style scoped>
section {
    font-size: 1.75rem;
}
.columns {
    display: flex;
    gap: 1rem;
    align-items: flex-start;
}
.column {
    flex: 1;
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 1em;
}

.bad {
    background-color: #ff808020;
}

.good {
    background-color: #80ff8020;
}

.column h3 {
    margin-top: 0;
    border-bottom: 2px solid #80808020;
    padding-bottom: 0.5em;
}
</style>

<div class="columns">
<div class="column bad">

### 👎 Špatný Prompt

**Prompt:** "Vysvětli fotosyntézu."

**Výstup:** Fotosyntéza je proces, při kterém zelené rostliny přeměňují světelnou energii na chemickou... využívá oxid uhličitý a vodu, uvolňuje kyslík. Klíčovou roli hraje chlorofyl.

</div>
<div class="column good">

### 👍 Dobrý Prompt

**Prompt:** "Jsi učitel biologie. Vysvětli fotosyntézu páťákovi pomocí analogie s vařením. Zmiň ingredience a výsledek."

**Výstup:** Představ si rostlinu jako kuchaře. Ingredience jsou slunce, voda a vzduch. V listech má 'kouzelný hrnec' (chlorofyl), kde z toho 'upeče' sladkou energii (cukr) a jako bonus nám dá kyslík k dýchání.

</div>
</div>

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">🤔</span>

# Jak se lépe ptát?

...aby nám LLM mohlo dát užitečnější odpověď

---

<style scoped>
    section {
        font-size: 2.5em;
        letter-spacing: -0.03em;
    }
</style>

- **Napiš kontext**
  - Špatně: Vysvětli inflaci.
  - Dobře: Vysvětli inflaci středoškolákovi, který zná základy ekonomie.
- **Napiš účel:** pro bakalářku / abych to pochopil
- **Napiš formu:** v bodech / na příkladu
- **Napiš omezení:** délka, jazyk, co nechceš
- **Ptej se postupně:** "Co je první věc, co musím pochopit o...?" "Připrav plán na..."
- **Ověř si odpověď:** "Jaké jsou důkazy o...", kde se můžu dočíst o...", "vyhledej na internetu..."

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">🖱️</span>

# Praktické ukázky

---

### 🖱️ Ukázka

# ⚙️ System prompt

System prompt je „tajná instrukce“, která říká AI, jak se má chovat po celou dobu konverzace.

---

### 🖱️ Ukázka

# 📁 File context

Multi-modální modely umí zpracovat nejen text, ale rozumí také obrazovým, video, a/nebo zvukovým souborům.

[Fotosyntéza - Notebook LM](https://notebooklm.google.com/notebook/9545ac19-bc8b-4334-97da-eacc3586671b)

---

### 🖱️ Ukázka

# 🖼️ Generování obrázků

Námět > Brainstorming > Prompt > Obrázek > Úpravy

---

## Co je "agentic workflow"?

**Agentic workflow** je způsob práce s AI,  
kdy AI **nejen odpovídá**,  
ale **plánuje, jedná, kontroluje a opakuje kroky**.

---

### Jak funguje agentic workflow?

- AI si **udělá plán**
- **vybere nástroj** (soubor, web, kód…)
- **provede akci**
- **zkontroluje výsledek**
- případně **to zkusí znovu**

➡️ smyčka, ne jedna odpověď

---

### 🖱️ Ukázka

# 👨‍🔬 Research mode

Výzkum pomocí AI, jako podklad pro AI

[Perplexity](https://www.perplexity.ai/search/check-the-list-of-drum-bass-hi-mfmsdSmRTd2.RMK8Ollhxw#0) > [Gemini 3](https://gemini.google.com/share/a2a9725ac9f5) >  
[Suno DnB Drum loop](https://suno.com/s/wElqwydfEXi8uB0c) > [Suno DnB Banger](https://suno.com/s/wVyHsXzIt33iNknS)

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# 😎 Vibe-Coding

...je způsob programování,
kdy místo psaní kódu popisuješ,
jak má věc fungovat,
a AI navrhuje kód za tebe.

_"The hottest new programming language is English"_
\- [Andej Karpathy](https://x.com/karpathy)

---

### ⚠️ Na co dát pozor?

- Kód nemusí být správně. Je potřeba otestovat
  - Můžeme použít automatizované testy
- Kód může obsahovat citlivá data, která budou volně přístupná
- Aplikace může nadměrně vytěžovat API a způsobit astronomické náklady

---

### 🖱️ Ukázka

# 🌐 Jednostránková HTML aplikace

Zero-shot: tzv. na první dobrou

[Demo Poster Filmový Večer](https://chatgpt.com/share/69832069-0304-8006-aa56-d46274039c7a)

---

### 🖱️ Ukázka

# 💻 AI nástroje v IDE

...IDE (Integrated Development Environment)
je program, ve kterém se píše a spouští kód.

Např. [VS Code](https://code.visualstudio.com/)

---

### 🖱️ Ukázka

# ⌨️ AI nástroje v příkazovém řádku

Např. [Claude Code](https://code.claude.com/docs/en/overview), [ChatGPT Codex](https://chatgpt.com/codex)

<!--
Notes:
- Demo option 1 (visual): "Vymysli storyboard na 10s reels video o tématu X a vygeneruj 3 klíčové obrázky." Rychlá změna stylu (retro vs. anime).
- Demo option 2 (visual): "Navrhni obal na sešit/diář a vytvoř 2–3 varianty s jiným moodem." Nechat třídu hlasovat.
-->

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">🧰</span>

# Pokročilé AI nástroje

---

### AI nástroje v internetovém prohlížeči

- **AI prohlížeče**
  - např. [Perplexity Comet](https://www.perplexity.ai/comet/)
- **Rozšíření prohlížeče (Extensions)**
  - Asistenti na jakékoliv stránce: např. [MaxAI.me](https://www.maxai.me/)
  - Pomoc s psaním: např. [Grammarly](https://www.grammarly.com/)

---

## 🔗 Co je MCP?

**[MCP](https://modelcontextprotocol.io) (Model Context Protocol)**  
je způsob, jak může AI bezpečně pracovat  
s externími nástroji a daty.

Např. MCP pro **lokální filesystem** (čtení / zápis souborů), pro **Git** repozitáře, pro aplikace jako **Figma**, nebo **VS Code**

---

<span class="icon">🤖</span>

# Automatizace pomocí AI

Např: [OpenClaw](https://openclaw.ai/), [N8N](https://n8n.io/), [Claude Cowork](https://claude.com/product/cowork)

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">⌛</span>

# Na závěr

---

## Ruku nahoru 🤚

# Komu z AI běhá mráz po zádech?

---

## Ruku nahoru 🤚

# Koho AI nadchlo a nemůže se dočkat, než vyzkouší nové AI technologie?

---

## Ruku nahoru 🤚

# Kdo má hlad a chce se mu už strašně na záchod? 😅

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# 🙋💬 Otázky?

_Kontakt na otázky později_
[✉️ tomasreichmann@gmail.com](mailto:tomasreichmann@gmail.com)

![w:200px](qr-email.png)

---

### 🙏 Děkuju za pozornost!

Prompt na rozloučenou

#### _"Na základě toho, co o mě víš, napiš 5 věcí, které by mi pomohly, abych byl v životě šťastnější. Nejdřív se mě zeptej se mě na otázky, které ti doplní informace, abys mi mohl dát lepší odpověď"_
