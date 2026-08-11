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

For any claim about a key factual node, also record its **support level** before writing: **explicit** (the source says this directly), **bounded** (the source supports only part of this description), or **absent** (the source does not say it). Key factual nodes include the object being studied, operational definitions, data source, sample, procedure, experimental setup, comparison condition, metric, result, mechanism, and conclusion. Do not use polishing to fill in an omitted step, motive, mechanism, threshold, or relationship. A sentence may sound more natural than the source, but it must not become more specific, more causal, or more certain than the source.

**Ambiguity rule**: when the source leaves room for more than one reading, do not choose one and write it as the factual account. Either (1) retain the ambiguity in plain language, (2) rewrite only the explicit common ground, or (3) move the reading into a clearly labelled interpretation. For example, if a paper reports that participants received a prompt but does not explain how it was used, write “研究中加入了这项提示” rather than “研究者借此引导参与者……”. If it reports an outcome without establishing why, write “结果呈现出……” rather than “这说明/这是因为……”.

Return to the original source before stating numbers, samples, methods, dates, comparisons, causal claims, named entities, or study conclusions. Do not turn correlation, self-report, or a limited sample into causal or universal claims.

For every claim that could become a conclusion, also record its **conclusion status in the source**: the source states it as an established conclusion, only partially supports it, or explicitly says there is no conclusion yet. Mirror that status in the draft — 来源明确，才写明确结论；来源说“尚未证实”“尚无定论”“存在争议”，正文就必须原样保留这种不确定，不得升格成事实。

### 2. Find the article's real question

State the central tension in one sentence. Prefer a human-scale question over a technology headline. Distinguish what the source studies from the larger question the article wants to discuss.

For research writing, explain the research question, method, key findings, and limitations only to the level needed for the narrative; do not simulate academic expertise by adding irrelevant technical detail.

### 3. Build an outline with paragraph jobs

Before prose, assign every section a unique job: scene, question, concept, method, evidence, interpretation, extension, or ending. For each section, specify its one new idea and its source basis.

Move from a concrete experience to the source material, then back to the reader's world. Do not write a sequence of disconnected observations.

For intro- and example-type sections, also answer “它引出什么” in the outline. 这类段落的唯一职责是把读者引到后面的表达或结论；如果一段介绍或例子无法说清“它引出了什么”，就从提纲里删掉。

### 4. Draft with evidence and voice

- Bind factual claims to the source ledger. Attribute studies precisely (e.g., “the survey reports”, not “research proves”).
- For **bounded** claims, write only the source-supported portion. Do not repair an awkward or incomplete source description with assumed details. Prefer a slightly less fluent but exact sentence over a smooth sentence that narrows the reader's interpretation.
- For **absent** claims, do not let contextual wording smuggle the claim into the draft. A rhetorical transition, illustrative scene, or causal connective cannot turn it into a fact. Delete it, verify it from an authorized source, or state it as the author's question or interpretation.
- Signal extensions with phrasing such as “这让我想到”, “放到软件测试里看”, or “论文没有直接回答，但…”.
- Match tone to the material: reflective and vivid for personal work; calm, curious, and lightly playful for research explanation; never sterile or sensational.
- Use concrete scenes, specific verbs, varied sentence length, and selective first-person observation where appropriate.
- Let uncertainty remain when the source does not settle a question.

**介绍与举例要“引出”，不要“陈列”**：

- 介绍先给读者一个具体的场景、疑问或反差，再自然过渡到要讲的东西；不要先堆背景信息，让读者在还没关心之前就被倒了一桌资料。
- 例子只选最能支撑当前论点的那一个，把它写进叙述里；不要用“举个例子：A。再比如：B。”这种罗列式，也不要为了“显得丰富”硬塞多个例子。
- 例子写完后，至少用半句话接到它要说明的结论上；接不上，就说明这个例子没在干活。
- 少用或不用生硬连接词：值得一提、举个例子来说、事实上、不难发现、众所周知、首先/其次/最后。
- 自查：如果一段介绍或例子删掉后，后面的表达与结论依然成立且无损，就重写或删除它。

**结论的强弱必须匹配来源**：

- 来源明确，才用明确语气；来源含糊、未证实或有争议，就用限定语气（“据…报道”“目前尚无定论”“论文没有直接回答”）。
- 每条强结论都能回指到来源的具体句子；回指不上，就把它降级为明确标注的“我的解读”，或删掉。
- 待核实内容不能充当论证支点：它只能作为明确标注的上下文或疑问出现，不能作为结论的前提。

**关键节点禁止“顺手补全”**：

- 不把“提到某项设置”润色为“通过该设置实现了某种机制”，除非来源同时明确了设置和机制。
- 不把结果的并列出现写成因果、目的或先后链条；“因此”“从而”“借此”“导致”“为了”都需要原文依据。
- 不把一项方法的名称、常见做法或领域常识当作本研究已经采用的具体操作。
- 不把图表中可见的趋势扩写为作者没有陈述的解释；图注、正文与作者讨论的表述优先于读图推断。
- 描述性转述完成后，反向追问：读者能否仅凭这句话推断出来源没有写过的细节？能，则收回到来源的原始粒度。

### 5. Edit for structure, repetition, and readability

Perform three passes before delivery:

1. **Structure**: confirm each paragraph advances the argument and bridges to the next.
2. **Redundancy**: keep each core claim's full explanation in one primary location. Delete or compress later restatements unless they add evidence, contrast, or a new consequence.
3. **Voice**: remove formulaic AI prose, inflated declarations, empty transitions, excessive rhetorical questions, and school-essay sequencing. Avoid repeatedly using “首先/其次/最后”, “值得注意的是”, “换句话说”, and symmetrical slogan-like sentences. 同时检查每一段介绍与例子是否自然、是否在把读者引向下一个表达或结论。

## Final fact audit

Before finalizing, check every factual sentence against the source. Confirm that:

- all figures and units are correct;
- source scope, sample, and method are accurately represented;
- correlation is not written as causation;
- limitations are included when they materially change interpretation;
- source conclusions, the article's explanations, and the author's extensions remain distinct.

再单独过两遍：

- 有没有把来源标注为“尚未证实 / 尚无结论 / 存在争议”的内容，当成事实直接下了结论？
- 有没有一段介绍或例子只是在“陈列”素材，而没有引出后面的表达或结论？
- 对每一个关键事实节点，是否能在底稿中定位到直接依据？若依据只支持其中一部分，正文是否只保留了那一部分？
- 是否有“为了 / 通过 / 因此 / 从而 / 导致 / 说明”等连接词，把来源未说明的目的、机制或因果关系写实了？
- 是否因为追求顺畅而替来源消除了歧义、补全了过程，或替作者解释了图表？有则改回描述性、保留不确定性，或移入明确标注的个人解读。

## Deliver

Write both files following [references/deliverables.md](references/deliverables.md). Link both files in the final response and briefly report any unresolved factual gaps. Do not expose the internal Fact/Explanation/Extension labels in the publishable draft.
