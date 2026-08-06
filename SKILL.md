---
name: source-grounded-content-writing
description: Create source-grounded, personally voiced Chinese content from papers, reports, news, books, interviews, or supplied materials. Use for WeChat articles, blogs, explanatory essays, reflective commentary, and content repurposing when factual fidelity, a coherent outline, non-repetitive prose, tone calibration, and separate publishable and fact-brief files are required.
---

# Source-Grounded Content Writing

Create readable Chinese content that translates interesting information into lived experience without overstating the source. Treat the supplied sources as the factual boundary and preserve a distinct, curious human voice.

## Scope and defaults

- Trigger for source-based long-form or short-form content creation, not ordinary chat, simple proofreading, email, code comments, or literal translation.
- Treat source material as the authority for factual claims. Search only when the user authorizes source expansion or the supplied material is insufficient.
- Default to Chinese unless the user requests another language.
- When the user has not asked for a direct draft, present the core proposition and outline before drafting. When asked to draft directly, build the outline internally and proceed.
- For every completed creation, write **two Markdown files** in the user-specified output directory. If none is specified, use the current workspace:
  1. `<slug>-publish.md`: the publishable external draft.
  2. `<slug>-fact-brief.md`: the internal fact brief described in [references/deliverables.md](references/deliverables.md).

## Workflow

### 1. Register the source

Read the provided source before drafting. Build an internal source ledger containing the source title/date, relevant page/section/link, and each usable claim.

Classify every substantive statement internally as one of:

- **Fact**: directly supported by a supplied source.
- **Explanation**: a faithful plain-language rendering of source facts.
- **Extension**: a clearly signposted inference, application, or personal observation.
- **Unverified**: omit from the publishable draft until verified.

Return to the original source before stating numbers, samples, methods, dates, comparisons, causal claims, named entities, or study conclusions. Do not turn correlation, self-report, or a limited sample into causal or universal claims.

### 2. Find the article's real question

State the central tension in one sentence. Prefer a human-scale question over a technology headline. Distinguish what the source studies from the larger question the article wants to discuss.

For research writing, explain the research question, method, key findings, and limitations only to the level needed for the narrative; do not simulate academic expertise by adding irrelevant technical detail.

### 3. Build an outline with paragraph jobs

Before prose, assign every section a unique job: scene, question, concept, method, evidence, interpretation, extension, or ending. For each section, specify its one new idea and its source basis.

Move from a concrete experience to the source material, then back to the reader's world. Do not write a sequence of disconnected observations.

### 4. Draft with evidence and voice

- Bind factual claims to the source ledger. Attribute studies precisely (e.g., “the survey reports”, not “research proves”).
- Signal extensions with phrasing such as “这让我想到”, “放到软件测试里看”, or “论文没有直接回答，但…”.
- Match tone to the material: reflective and vivid for personal work; calm, curious, and lightly playful for research explanation; never sterile or sensational.
- Use concrete scenes, specific verbs, varied sentence length, and selective first-person observation where appropriate.
- Let uncertainty remain when the source does not settle a question.

### 5. Edit for structure, repetition, and readability

Perform three passes before delivery:

1. **Structure**: confirm each paragraph advances the argument and bridges to the next.
2. **Redundancy**: keep each core claim's full explanation in one primary location. Delete or compress later restatements unless they add evidence, contrast, or a new consequence.
3. **Voice**: remove formulaic AI prose, inflated declarations, empty transitions, excessive rhetorical questions, and school-essay sequencing. Avoid repeatedly using “首先/其次/最后”, “值得注意的是”, “换句话说”, and symmetrical slogan-like sentences.

## Final fact audit

Before finalizing, check every factual sentence against the source. Confirm that:

- all figures and units are correct;
- source scope, sample, and method are accurately represented;
- correlation is not written as causation;
- limitations are included when they materially change interpretation;
- source conclusions, the article's explanations, and the author's extensions remain distinct.

## Deliver

Write both files following [references/deliverables.md](references/deliverables.md). Link both files in the final response and briefly report any unresolved factual gaps. Do not expose the internal Fact/Explanation/Extension labels in the publishable draft.
