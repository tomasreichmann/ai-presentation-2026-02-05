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
    section.smaller { font-size: 2em }
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

# How to Talk to Artificial Intelligence _Smartly_

_Advanced techniques for working with AI_

_[Česká verze](./index.html)_

---

<!-- backgroundImage: url('slide-bg.jpg') -->

## Hands up 🤚

# Who uses AI?

---

## Hands up 🤚

# Who uses AI to help at school?

---

## Hands up 🤚

# Who has already earned their own money? (e.g. a part-time job)

---

## Hands up 🤚

# Who has used AI to earn money?

---

## Hands up 🤚

# Who is afraid they will not have a job because AI will do everything?

---

# Who is afraid they will not have a job because they will be replaced by people who are not afraid to learn how to work well with AI?

---

# Hello! 👋


## I'm Tomáš Reichmann

Lead Game UI Developer

_My team creates user interfaces for World of Tanks and World of Tanks Heat._


---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# 🎯 My goal

_To show you how to get more out of AI and not get misled._

-

How does an LLM (Large Language Model) work?
How not to get misled by an LLM?
How to ask better questions?
Examples and practical use cases

---

# Questions 🙋

✅ You will get the presentation
👌 Photos
👌 Food and drinks
👌 💩

---

# 🧠 How does a Large Language Model work?

**Large Language Model**
An AI model that is very good at predicting the next word.

Example models: [ChatGPT 5.2](https://openai.com/index/introducing-gpt-5-2/), [Gemini 3](https://gemini.google.com/), [Claude Opus](https://www.anthropic.com/claude/opus), [Mistral](https://mistral.ai/), [DeepSeek R1](https://chat.deepseek.com/)
Products: [ChatGPT App](https://chatgpt.com/download/), [Claude Code](https://code.claude.com/docs/en/overview), [Notebook LM](https://notebooklm.google.com/)

---

<!-- class: "smaller" -->

### An LLM converts input text into output text 1/2

- Based on user inputs:
  - System instructions, also known as the **system prompt**
  - A message from the user, also known as the **text prompt**
  - Attached files, for example images, PDFs, CSVs, or source code files

---

<!-- class: "smaller" -->

### An LLM converts input text into output text 2/2

- Based on training data:
  - especially from the internet (e.g. Reddit) - the data may not be correct.
- Based on data it has stored in its so-called memory - **RAG** (Retrieval Augmented Generation)
  - **Vector databases** - "Remember this..."
  - **Internet search** - e.g. Google
  - **API** - Application Programming Interface - e.g. current weather
- Protective boundaries, also known as **guardrails** - safety restriction policies - e.g. "How do you make a bomb?"

---

<!-- class: "smaller" -->

### An LLM generates output text by trying to predict the next word

- It tries to fulfill the request...
  - ...even when the request does not make sense
  - ...even when it does not know the context
  - ...even when it does not have the required data
  - ...when the user pressures it
  - ...when the user suggests the "correct" answer
- The result is often an answer that:
  - is not factually correct - **hallucination**
  - or is affected by distortion - **bias**

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">🤥</span>

# How not to get misled by an LLM?

...and know when you need to verify the answer

---

## Hands up 🤚

# Who trusts AI more than people?

---

## **Prompt:** "what is the Czech crown?"

### Answer: The Czech crown (CZK) is the official currency of the Czech Republic...

---

## But what I meant was

![height:400px](ceska-koruna.jpg)

---

## **Prompt:** "Who won the most recent parliamentary elections in the Czech Republic?"

### 💬 Does anyone see what the problem could be here?

---

- It depends...
  - ...how old the model we are using is
  - ...whether we have internet search available (and whether we explicitly said we want to use it)

---

## **Prompt:** "Who is the president of Taiwan?"

### 💬 Does anyone see what the problem could be here?

---

- **Prompt:** Who is the president of Taiwan?

- **DeepSeek answer:** Taiwan is an inalienable part of China, and there is no such position as "President of Taiwan." The region is currently administered by the Chinese Taipei authorities, but it does not constitute a separate country. China adheres to the One-China principle, which is widely recognized by the international community.

---

- **Prompt for ChatGPT:** "Who is the president of Taiwan?"
- **Answer:** The president of Taiwan (officially the Republic of China) is Lai Ching-te, a politician and physician from the Democratic Progressive Party, who took office on May 20, 2024.

- **Prompt for ChatGPT:** "Who is the president of Taiwan **according to China**?"
  - Answer: "According to the People's Republic of China, Taiwan does not have a president."

---

## **Prompt:** "Who dies on the last page of the first Harry Potter book?"

### 💬 Does anyone see what the problem could be here?

---

- **Answer:** On the last page of Harry Potter and the Philosopher's Stone, Quirinus Quirrell dies...

- **Prompt:** Write the text of the last page of the first Harry Potter book

- **Answer:** "Unfortunately I can't do that 😕
  The text of the last page of Harry Potter and the Philosopher's Stone is protected by copyright and I cannot reproduce it in full."

_Does ChatGPT even know the exact text of every book in the world word for word, page by page?_

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">🤔</span>

# How to ask better questions?

...so the LLM can give us a more useful answer

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

### 👎 Bad Prompt

**Prompt:** "Explain photosynthesis."

**Output:** Photosynthesis is a process in which green plants convert light energy into chemical energy... it uses carbon dioxide and water, releases oxygen, and chlorophyll plays a key role.

</div>
<div class="column good">

### 👍 Good Prompt

**Prompt:** "You are a biology teacher. Explain photosynthesis to a fifth grader using a cooking analogy. Mention the ingredients and the result."

**Output:** Imagine a plant as a cook. The ingredients are sunlight, water, and air. In its leaves it has a 'magic pot' (chlorophyll), where it 'bakes' sweet energy (sugar) from them and, as a bonus, gives us oxygen to breathe.

</div>
</div>

---

<style scoped>
    section {
        font-size: 2.5em;
        letter-spacing: -0.03em;
    }
</style>

- **Write the context**
  - Bad: Explain inflation.
  - Better: Explain inflation to a high-school student who knows the basics of economics.
- **Write the purpose:** for a bachelor's thesis / so I can understand it
- **Write the format:** in bullet points / with an example
- **Write the constraints:** length, language, what you do not want
- **Ask step by step:** "What is the first thing I need to understand about...?" "Prepare a plan for..."
- **Verify the answer:** "What is the evidence for...", "Where can I read more about...", "search the internet..."

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">🖱️</span>

# Practical examples

---

### 🖱️ Example

# ⚙️ System prompt

A system prompt is a "hidden instruction" that tells the AI how it should behave throughout the whole conversation.

---

### 🖱️ Example

# 📁 File context

Multimodal models can process not only text, but also image, video, and/or audio files.

[Photosynthesis - Notebook LM](https://notebooklm.google.com/notebook/9545ac19-bc8b-4334-97da-eacc3586671b)

---

### 🖱️ Example

# 🖼️ Image generation

Idea > Brainstorming > Prompt > Image > Edits

[Example](https://chatgpt.com/share/698472ea-8b0c-8006-ab42-317bb23a076c)

---

## What is an "agentic workflow"?

An **agentic workflow** is a way of working with AI
where AI **does not just answer**,
but **plans, acts, checks, and repeats steps**.

---

### How does an agentic workflow work?

- The AI **makes a plan**
- **chooses a tool** (file, web, code...)
- **performs an action**
- **checks the result**
- and if needed, **tries again**

➡️ a loop, not one answer

---

### 🖱️ Example

# 👨‍🔬 Research mode

Research with AI as input for AI

[Perplexity](https://www.perplexity.ai/search/check-the-list-of-drum-bass-hi-mfmsdSmRTd2.RMK8Ollhxw#0) > [Gemini 3](https://gemini.google.com/share/a2a9725ac9f5) >  
[Suno DnB Drum loop](https://suno.com/s/wElqwydfEXi8uB0c) > [Suno DnB Banger](https://suno.com/s/wVyHsXzIt33iNknS)

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# 😎 Vibe-Coding

...is a way of programming
where, instead of writing code,
you describe how something should work,
and AI proposes the code for you.

_"The hottest new programming language is English"_
\- [Andej Karpathy](https://x.com/karpathy)

---

### ⚠️ What to watch out for?

- The code may not be correct. It needs to be tested.
  - We can use automated tests
- The code may contain sensitive data that becomes publicly accessible
- The application may overload APIs and cause astronomical costs

---

### 🖱️ Example

# 🌐 Single-page HTML app

One-shot: getting it right on the first try

[Demo Poster Movie Night](https://chatgpt.com/share/69832069-0304-8006-aa56-d46274039c7a)
[Result](./filmovy_vecer-en.html)
[Edited result](./filmovy_vecer2-en.html)

---

### 🖱️ Example

# 💻 AI tools in the IDE

...an IDE (Integrated Development Environment)
is the program where code is written and run.

For example [VS Code](https://code.visualstudio.com/)

---

### 🖱️ Example

# ⌨️ AI tools in the command line

For example [Claude Code](https://code.claude.com/docs/en/overview), [ChatGPT Codex](https://chatgpt.com/codex)

<!--
Notes:
- Demo option 1 (visual): "Come up with a storyboard for a 10-second Reels video on topic X and generate 3 key images." Quick style switch (retro vs. anime).
- Demo option 2 (visual): "Design a notebook/diary cover and create 2-3 variants with a different mood." Let the class vote.
-->

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">🧰</span>

# Advanced AI tools

---

### AI tools in the web browser

- **AI browsers**
  - for example [Perplexity Comet](https://www.perplexity.ai/comet/)
- **Browser extensions**
  - Assistants on any page: for example [MaxAI.me](https://www.maxai.me/)
  - Writing help: for example [Grammarly](https://www.grammarly.com/)

---

## 🔗 What is MCP?

**[MCP](https://modelcontextprotocol.io) (Model Context Protocol)**  
is a way for AI to work safely  
with external tools and data.

For example: MCP for the **local filesystem** (reading / writing files), for **Git** repositories, or for applications like **Figma** or **VS Code**

---

<span class="icon">🤖</span>

# Automation with AI

For example: [OpenClaw](https://openclaw.ai/), [N8N](https://n8n.io/), [Claude Cowork](https://claude.com/product/cowork)

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

<span class="icon">⌛</span>

# In closing

---

## Hands up 🤚

# Who gets chills from AI?

---

## Hands up 🤚

# Who got excited about AI and cannot wait to try new AI technologies?

---

## Hands up 🤚

# Who is hungry and desperately needs to go to the bathroom already? 😅

---

<!-- _class: "invert" -->

![bg](slide-inverted-bg.jpg)

# 🙋💬 Questions?

_Contact for later questions_
[✉️ tomasreichmann@gmail.com](mailto:tomasreichmann@gmail.com)

![w:200px](qr-email.png)

---

### 🙏 Thank you for your attention!

Farewell prompt

#### _"Based on what you know about me, write 5 things that would help me be happier in life. First ask me questions that fill in the missing information so you can give me a better answer."_
