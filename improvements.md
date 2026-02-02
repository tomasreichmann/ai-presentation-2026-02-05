# Improvements for slide-deck.md (content)

## Narrative and structure
- Add a short agenda or 3-part roadmap early (e.g., What LLMs are, Why they fail, How to use them well). It helps audiences form a mental map and improves retention.
- Insert explicit transitions between sections (LLM basics -> limitations -> prompting -> demos) so the audience understands why the next block matters.
- Add a final 3-5 item recap slide before Q&A; repetition improves recall and gives closure.

## Accuracy and clarity
- Clarify the difference between a model and a product (LLM vs. ChatGPT/Gemini/Claude) to avoid conflating model families with apps/tools.
- Tighten the definition of RAG: emphasize that it retrieves from external sources and does not mean the model has long-term memory.
- Add a brief note that "guardrails" are policy and safety constraints, not a guarantee of truthfulness.
- When discussing time-sensitive questions (elections, presidents), show the date of the model's knowledge cutoff and the date of retrieval. This reduces confusion and models good practice.

## Examples and evidence
- Include one example where a "good" prompt clearly outperforms a "bad" prompt with side-by-side outputs. That makes the advice tangible.
- Add a short example of verification behavior (e.g., asking for sources or cross-checking) to reinforce critical evaluation.
- Consider one example where the model correctly refuses due to copyright, then show how to ask for a summary or key themes instead. This teaches a safe alternative.

## Audience engagement
- The repeated "Ruku nahoru" slides are good for engagement, but consider pacing: cluster them at the start, then reduce frequency later to keep momentum.
- Add one quick paired discussion or 30-second prompt for the audience to craft a prompt; then show 1-2 volunteers' prompts and improve them live.

## Content balance and depth
- Add a slide that distinguishes factual tasks (low temperature, citations, tools) from creative tasks (higher temperature, brainstorming). This helps tool choice.
- Consider one slide on "failure modes" (hallucination, bias, outdated info, prompt injection) with simple examples and mitigations.
- For "Vibe-Coding," briefly mention the need for testing and review to avoid over-trusting generated code.

## Slide-specific notes
- "Jak funguje LLM?" Add a simple diagram or 3-step pipeline (prompt -> model -> output) to reduce cognitive load.
- "LLM prevadi vstupni text na vystupni text" is text-heavy; reduce to 3-4 bullets and move detail into speaker notes.
- The Harry Potter example is good for copyright refusal; consider adding a non-fiction example (e.g., a current event) to show verification and browsing behavior.
- "Automatizace pomoc? AI": include a short use-case that is relevant to the audience (school admin, study planner, or part-time job workflows).

## Consistency and duplication
- "AI nastroje v prikazove radce" appears twice; replace one with a contrasting example (e.g., "AI nastroje v prohlizeci" or "AI v mobilu").
- Ensure consistent terminology for prompts (system vs. user), and reuse the same Czech terms throughout.

## Best-practice alignment (with sources)
- Keep slides focused on one key idea and reduce text density to lower extraneous cognitive load. This aligns with multimedia learning principles on coherence and redundancy.
- Use visuals and keep labels near related graphics to avoid split-attention and improve spatial contiguity.
- Use explicit signaling (headings, cue words, structure) to guide attention and reinforce organization.
- Reinforce critical evaluation and risk awareness when discussing hallucinations and bias; anchor this in general AI risk guidance.

## Sources consulted
- Cambridge Handbook of Multimedia Learning (coherence, signaling, redundancy, spatial and temporal contiguity principles): https://www.cambridge.org/core/books/cambridge-handbook-of-multimedia-learning/principles-for-reducing-extraneous-processing-in-multimedia-learning-coherence-signaling-redundancy-spatial-contiguity-and-temporal-contiguity-principles/C98AB3A6CE760DD63C048936EA0B3B44
- University of Delaware instructional design guide (multimedia learning principles table): https://www1.udel.edu/edtech/design/modules/02-learning.html
- Stanford ENGR110/210 slideshow tips (reduce text, use strong visuals): https://web.stanford.edu/class/engr110/2023/slideshow.html
- NIST AI Risk Management Framework (risk, trustworthiness, evaluation): https://www.nist.gov/itl/ai-risk-management-framework

