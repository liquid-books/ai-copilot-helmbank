---
title: "Chapter 18: Week 6, Session B — Showcase Project Development Workshop"
subtitle: "Build, Test, and Refine — Your AI Project Goes Live"
short_title: "Showcase Project Development"
description: "A structured studio session where Helm Bank professionals build and test their AI transformation projects, debug their workflows, prepare compelling before/after demonstrations, and learn the Showcase Framework for presenting their work."
label: ch-18-showcase-development
tags: [showcase, project development, workflow testing, demo preparation, Copilot debugging, before-after, Helm Bank, banking AI, studio session, presentation skills]
---

```{admonition} Download this Chapter as PDF
:class: tip
[Download PDF](https://github.com/liquid-books/ai-copilot-helmbank/raw/main/pdfs/ch18-showcase-development.pdf)
```

# Chapter 18: Week 6, Session B — Showcase Project Development Workshop

## Build, Test, and Refine — Your AI Project Goes Live

---

> *"A prototype that works in the room is worth more than a thousand slide decks about what AI could theoretically do."*
> — Overheard at a Helm Bank internal technology showcase, Q3 2025

---

## Opening: The Day Everything Gets Real

There is a specific moment in every great project when it stops being an idea and becomes a thing. A real, demonstrable, testable thing. In engineering they call it "first light" — the moment a telescope opens its eye and actually sees a star. In software, it is the first time a user touches your code and the code does something useful back.

Today is that day for you.

You arrived at this program six weeks ago with a vague sense that AI could help your work. Over the past five sessions you built something more concrete: a clear picture of where Helm Bank's most important processes live, a blueprint for one specific transformation, and the beginnings of a working Copilot integration. You have read about prompts. You have practiced techniques. You have seen demonstrations.

Now the training wheels come off.

This session — the Showcase Project Development Workshop — is a structured studio environment. The room becomes a lab. The instructor becomes a coach. You and your teammates become builders. By the time the session closes, you will have a working demonstration of your AI transformation project, a compelling before-and-after story to tell, and a presentation framework ready for the Final Showcase next session.

This chapter serves as your complete guide to everything that happens in the workshop: the methodology, the pitfalls, the debugging playbook, the Showcase Framework, and three worked examples drawn from real Helm Bank departments. Read it before the session to orient yourself. Keep it open during the session as a reference. Return to it afterward when you are refining your presentation.

The work you do today will outlast this training program. Let's make it count.

---

## The Studio Session Structure

Unlike a traditional class session — where an instructor delivers content and participants receive it — a studio session inverts the model. You are the creator. The instructor is the resource. The clock is the constraint. This is how professional design firms, engineering teams, and innovation labs actually work.

The Showcase Project Development Workshop runs in five distinct phases, each with a specific purpose:

```{figure} figures/ch18-studio-phases.png
:name: fig-studio-phases
:alt: Five phases of the studio session: Orient, Build, Test, Refine, Frame
:width: 85%

**The Five Phases of the Development Studio.** Each phase has a time box and a defined deliverable. Teams that treat the phase boundaries seriously finish the session with a polished, demonstrable project.
```

**Phase 1 — Orient (20 minutes)**
Review your Chapter 16 blueprint and Chapter 17 integration notes. Confirm your project scope. Identify the single workflow you will demonstrate. Assign roles if working in a team. Write your "before" story in plain language before you touch Copilot.

**Phase 2 — Build (60 minutes)**
Construct the core of your Copilot workflow. This is the main work block. Focus on getting a working prototype — not a perfect one. Perfection is the enemy of demonstrable.

**Phase 3 — Test (30 minutes)**
Run your workflow with real (or realistic) data. Document what works and what breaks. Execute the debugging protocol described in this chapter.

**Phase 4 — Refine (20 minutes)**
Fix the two or three most important issues. Improve prompt clarity. Tighten outputs. Do not attempt to rebuild from scratch — make surgical improvements only.

**Phase 5 — Frame (20 minutes)**
Structure your 10-minute Showcase presentation using the Showcase Framework. Practice your opening hook. Identify your most powerful data point.

Total session time: 150 minutes, with short breaks between phases.

---

## Before You Build: Writing Your "Before" Story

The most common mistake in AI project demonstrations is leading with the technology. Participants eager to show off a polished Copilot output skip directly to the impressive part — and lose their audience in the first thirty seconds.

Every powerful demonstration begins with pain.

Your "before" story is the articulation of what life looked like before your AI transformation. It should make the audience feel the friction, the delay, the cognitive load, or the risk that your project addresses. A good before story does not need to be dramatic — it needs to be *true*.

```{admonition} Workshop Exercise
:class: important

**Writing Your Before Story**

Before opening Copilot or any Microsoft 365 application, answer these four questions in writing. Take ten minutes. Be specific. Use real numbers where you have them.

1. **What is the task?** Describe the exact process your project addresses in one sentence. Not "we want to use AI for compliance" — something like "every Monday morning, our compliance team manually reviews 40–60 transaction exception reports and writes a summary memo for the Chief Compliance Officer."

2. **How long does it take today?** Give a time estimate. "About three hours every Monday morning, meaning two compliance analysts are occupied until roughly noon."

3. **What is the human cost?** Describe the cognitive burden, the frustration, or the opportunity cost. "Those same analysts could be investigating the flagged transactions more deeply, but instead they are copy-pasting summary statistics."

4. **What could go wrong when humans do it under time pressure?** "When the Monday memo is late — which happens when a public holiday shifts the schedule — the CCO makes decisions without full information for a period."

When you have answered these four questions, you have your before story. It will become the first two minutes of your Showcase presentation.
```

The before story also serves a critical technical function: it forces you to define exactly what your Copilot workflow needs to *do*. A vague before story produces a vague workflow. A specific before story points directly to the prompt structure, the data inputs, and the output format your project requires.

---

## The Build Phase: From Blueprint to Working Prototype

### Choosing Your Scope

One of the hardest lessons for motivated participants: your showcase project does not need to do everything. It needs to do one thing well and demonstrably.

Review your Chapter 16 blueprint. It likely contains three to five potential Copilot applications across your workflow. For this workshop, select the *single* highest-impact, *lowest-complexity* application. This is the one that:

- Has clear, available inputs (data, documents, emails you actually have access to)
- Produces a discrete, visible output (a summary, a draft, a structured table, a risk flag)
- Can be set up and tested within the Build phase
- Has an obvious before/after comparison

If your blueprint targeted a complex, multi-step automation — connecting Copilot to SharePoint lists, Power Automate flows, and a custom AI plugin — set that vision aside for now. Your showcase demonstrates the *core value proposition*. The infrastructure vision can be described verbally.

```{figure} figures/ch18-scope-matrix.png
:name: fig-scope-matrix
:alt: Scope selection matrix with axes of impact and complexity
:width: 75%

**Showcase Scope Selection Matrix.** For this workshop, target the high-impact, low-complexity quadrant. Complex, high-impact visions belong in your verbal description of future state — not in a live demo that might break under pressure.
```

### Building Your Prompt Architecture

For most Helm Bank showcase projects, the core Copilot interaction is a carefully engineered prompt — or a short sequence of prompts — that transforms a real input into a useful output. Prompt architecture at this stage means making deliberate choices about four elements:

**Role assignment.** Tell Copilot what expert it is embodying. "You are a senior credit analyst at an international commercial bank specializing in Latin American markets." This primes the model to use appropriate terminology, make relevant assumptions, and calibrate its level of technicality.

**Context injection.** Provide the specific information Copilot needs that it cannot infer. For a compliance workflow, this might mean pasting the relevant regulatory standard, the firm's internal policy reference, or a summary of the client relationship history. Do not assume Copilot knows what Helm Bank knows.

**Task specification.** State the output you want with precision. Not "analyze this document" but "identify the three highest-risk items in this document, explain why each is high-risk with reference to BSA/AML guidelines, and suggest a specific follow-up action for each."

**Format instruction.** Specify how you want the output structured. A busy Helm Bank executive reads a three-bullet executive summary differently from a two-page narrative report. Both might contain the same information — but the right format for the right audience is part of the value your AI workflow delivers.

```{admonition} Workshop Exercise
:class: important

**Building Your Prompt Architecture**

Using the four-element framework above, draft your primary prompt in writing before entering it into Copilot.

1. Write the **Role** sentence: "You are a [role] specializing in [domain]."
2. Write the **Context** block: What must Copilot know that is specific to your situation? Paste in 3–5 sentences of context, or reference a document you will attach.
3. Write the **Task** sentence: "Your task is to [specific action] producing [specific output]."
4. Write the **Format** instruction: "Structure your response as [format]."

Combine all four into a single prompt. Before running it, read it aloud. Would a highly competent human expert understand exactly what you need? If not, revise.

This written prompt becomes Exhibit A in your Showcase presentation — the moment you show the audience exactly what you typed, and then reveal what came back.
```

### Working with Real Helm Bank Data

One of the most frequent build-phase questions: "Can I use real client data in my demonstration?"

The answer, without exception, is **no**. Client data is protected by privacy regulations, the Bank Secrecy Act, and Helm Bank's own data governance policies. This is non-negotiable.

For workshop purposes, use one of these three approaches:

**Approach 1 — Synthetic data.** Create a realistic but entirely fictional scenario. A fictional client, "Constructora Andina S.A.," with a fictional loan application containing realistic but invented figures. The demonstration is just as technically valid, and you bear zero compliance risk.

**Approach 2 — Anonymized and scrubbed data.** Take a real document type and manually replace all identifying information — names, account numbers, addresses, specific dollar amounts — with generic placeholders before the session. "[CLIENT NAME]", "[LOAN AMOUNT]", "[COUNTRY OF ORIGIN]". The structure is authentic; the content is protected.

**Approach 3 — Template inputs.** Use standardized document templates — blank loan application forms, empty compliance checklists, generic financial statement structures — and populate them with clearly fictional information. This approach is especially clean because the audience recognizes the template format and immediately understands the workflow's applicability.

Whichever approach you choose, have your test data prepared *before* the Build phase begins. Scrambling to create test inputs during your build time is one of the most common causes of teams running short on the clock.

---

## The Test Phase: Debugging Copilot Workflows

### Why Testing Is Not Optional

In a training demonstration, a failed prompt is mildly embarrassing. In a production environment, a failed prompt means a colleague received wrong information, a client got an inaccurate summary, or a compliance flag was missed. The habit of rigorous testing is not just good practice for your showcase — it is the professional standard for anyone deploying AI tools in a regulated financial institution.

The Test phase is not about finding problems to eliminate. It is about *finding problems before your audience does* — and about developing the intellectual honesty to understand where your AI workflow's limits are.

### The Debugging Protocol

When a Copilot output is not what you expected, resist the impulse to conclude that "AI doesn't work." Work through the following five-step debugging protocol systematically:

```{figure} figures/ch18-debug-protocol.png
:name: fig-debug-protocol
:alt: Five-step debugging protocol flowchart
:width: 80%

**The Five-Step Debugging Protocol.** Most prompt failures fall into one of three categories: ambiguous task specification, insufficient context, or format mismatch. The protocol guides you to the root cause quickly.
```

**Step 1 — Read the output carefully before judging it.**
Sometimes Copilot produces something different from what you expected — but what it produced is actually *correct* given the prompt you wrote. Before concluding the output is wrong, ask: "If a human expert read exactly the prompt I wrote, would they reasonably produce this output?" If yes, the problem is in your prompt, not in Copilot's reasoning.

**Step 2 — Identify the failure type.**
AI output failures fall into five categories. Name which one you are experiencing before attempting a fix:

- *Hallucination* — Copilot stated facts that are not in the source material and cannot be verified
- *Incompleteness* — Copilot addressed part of the task but omitted sections you needed
- *Format failure* — The content is correct but the structure is wrong for your use case
- *Tone mismatch* — The output is factually fine but written for the wrong audience
- *Task confusion* — Copilot answered a different question than the one you meant to ask

**Step 3 — Fix one element at a time.**
Do not rewrite your entire prompt to fix a formatting problem. Change the format instruction only — keep everything else identical — and rerun. This isolates whether your fix actually solved the problem. Rewriting everything at once makes it impossible to know what worked.

**Step 4 — Add specificity, not complexity.**
The most reliable fix for most failures is making your prompt *more specific*, not *more complex*. If Copilot is producing summaries that are too long, add "in no more than 150 words." If it is missing a required element, name that element explicitly: "Include a section titled 'Regulatory Risk Assessment' with reference to the specific regulation."

**Step 5 — Test with a second input.**
After fixing your prompt, test it with a *different* input than the one that surfaced the failure. A prompt that works perfectly on one type of document but fails on a slightly different variant is fragile. Your showcase — and your real-world deployment — needs a prompt that is robust across the realistic range of inputs your team will encounter.

```{admonition} Workshop Exercise
:class: important

**The Stress Test**

Once your primary prompt produces a satisfactory output, deliberately try to break it. Run each of the following stress tests and document what happens:

1. **The edge case input:** Use an input that is at the boundary of your expected range. If your workflow summarizes loan applications, use a very short, incomplete one — and then an unusually complex one with many attached conditions.

2. **The adversarial input:** Use an input that contains contradictory information or missing fields. Does Copilot flag the inconsistency, or does it produce a confident-sounding but incorrect output?

3. **The wrong language:** If Helm Bank's workflows involve Spanish-language documents (as many do, given the Latin America corridor), test your prompt against a Spanish-language input. Does it handle the language switch gracefully? Does your format instruction need to specify output language?

4. **The time-pressured scenario:** Imagine you are running this workflow on a Monday morning with 40 documents queued. Is the output quality consistent on the fifth document as it was on the first? For live Copilot, this means running the prompt multiple times in sequence and comparing outputs.

Document your findings in the Test Log template. These findings become a valuable part of your Showcase presentation — they demonstrate professional rigor and honest assessment of AI capabilities.
```

### Common Pitfalls During Build and How to Avoid Them

Across Helm Bank's pilot programs and internal AI workshops, certain failure modes appear repeatedly. Knowing them in advance lets you avoid them.

**Pitfall 1 — The Scope Creep Build**
Symptoms: Team starts with one workflow, then adds "just one more thing" — and then another — until the demonstration tries to show five things and does none of them well. Fix: Write your scope on a whiteboard or sticky note at the start of the Build phase. When the temptation to expand arises, write the idea down in a "Version 2" list — do not build it now.

**Pitfall 2 — The Perfection Paralysis**
Symptoms: Team spends forty-five minutes refining the prompt on one test case and never runs a second test. The demonstration looks great on the single carefully-chosen input and fails on every other input. Fix: Set a timer. After twenty minutes of building on a single prompt, move on to testing — even if you are not satisfied with the output. Testing will tell you what refinement to prioritize.

**Pitfall 3 — The Technology-First Demo**
Symptoms: The presenter opens the showcase by showing Copilot features — "Look, it can summarize! Look, it can translate!" — without connecting those features to a specific Helm Bank workflow problem. The audience is impressed but unclear on the business value. Fix: Write your before story *before* you open Copilot. Your demo sequence must always start with the problem.

**Pitfall 4 — The Unreliable Live Demo**
Symptoms: The workflow works in Build, works in Test, and then fails unpredictably during the actual showcase — because the presenter is nervous, the network is slow, or the live data is subtly different from the test data. Fix: Have a pre-recorded backup. Capture a screen recording of your workflow running successfully during the Test phase. If the live demo fails, switch to the recording without apology. A failed live demo that you handle gracefully is actually more impressive than a flawless demo — it shows you prepared.

**Pitfall 5 — The Missing Measurement**
Symptoms: The presenter confidently claims the AI workflow "saves a lot of time" without specifying how much. The audience wants to believe the claim but has nothing to hold onto. Fix: Measure. Time yourself doing the "before" version of the task during Phase 1 of this workshop. Then time the AI-assisted version. The difference — in minutes saved, steps eliminated, or error rate reduced — is your most powerful slide.

---

## The Showcase Framework: Your 10-Minute Presentation Architecture

The Final Showcase is the capstone of the Helm Bank Copilot Master Class. Each project team presents their AI transformation to a mixed audience: colleagues from other departments, senior leadership, and potentially members of Helm Bank's technology and innovation committees. You have ten minutes. Here is how to use every second.

```{figure} figures/ch18-showcase-framework.png
:name: fig-showcase-framework
:alt: The 10-Minute Showcase Framework timeline showing all six segments
:width: 90%

**The 10-Minute Showcase Framework.** Each segment has a fixed time allocation and a specific job to do. Teams that over-invest in the demo segment and under-invest in the business impact segment consistently leave audiences unsatisfied — even when the technology is impressive.
```

### Segment 1 — The Hook (60 seconds)

Open with a single, vivid, specific statement of the problem. Not a title slide reading "AI in Compliance Operations." A story: "Every Monday at Helm Bank, two of our sharpest compliance analysts spend their entire morning cutting and pasting numbers from exception reports into a summary memo. Last quarter, that added up to over 200 analyst-hours on a task that requires no analysis — just transcription." Pause. Let it land. Then introduce your project in one sentence.

The hook must be specific enough to be credible. It must be concrete enough to be felt. And it must be brief enough that the audience wants to hear what you did about it.

Common hook structures that work for Helm Bank projects:

- **The time statement:** "Every [frequency], our team spends [hours] doing [task]. That is [annualized number] of [role] hours per year."
- **The risk statement:** "Our current process creates a window of [X hours/days] during which [specific risk] is not detected."
- **The opportunity cost statement:** "Our [role] spend [X%] of their time on [low-value task], leaving [Y%] for the relationship work that actually grows our portfolio."

### Segment 2 — Before State (90 seconds)

Show exactly what the process looks like today. Use a simple visual — a process flowchart with time stamps, a screenshot of the manual steps, or a timeline showing the decision bottleneck. The audience must *see* the before state, not just hear about it. Quantify wherever possible: number of steps, time elapsed, human effort required, error rate or risk exposure.

The before visual should be clean and readable from the back of the room. Use large fonts. Highlight the pain point in red or orange. A single annotated screenshot is worth three paragraphs of narration.

### Segment 3 — The Solution Overview (90 seconds)

Describe your AI transformation in plain language. Avoid jargon. You are not pitching a technology — you are describing a new way of working. "We built a Copilot workflow that ingests the Monday exception reports, analyzes them against our standard risk criteria, and produces a structured summary memo in the CCO's preferred format — in under two minutes." Then briefly explain the three key design decisions you made: what Copilot does, what humans still do, and what guardrails you built in.

The guardrails statement is crucial for a banking audience. Say explicitly: "Every AI-generated output is reviewed by [role] before it is acted on. No AI output goes directly to a client or regulator without human review." This is not a weakness of your project — it is evidence that you understand the compliance environment you work in.

### Segment 4 — Live Demonstration (3 minutes)

This is the moment the audience has been waiting for. Execute your workflow in real time, narrating as you go. Use the three-part narration structure:

**"Here is the input"** — Show what goes into Copilot. If it is a document, briefly describe it. If it is a prompt, read the key elements aloud. Do not rush past the input — it is half the story.

**"Here is the workflow"** — Run it. Let the audience watch the output appear. Do not rush this moment — the generation of output in real time is inherently compelling. Narrate what Copilot is doing as it works: "It is pulling the key financial ratios, ranking the risk factors, and now structuring the output in our standard memo format."

**"Here is the output"** — Point to the specific elements that matter. "Notice that it identified the three highest-risk exceptions, ranked them by severity, and linked each one to the specific regulatory standard. That took twenty-three seconds. The same task took our team forty-five minutes manually."

If anything goes wrong during the live demo, say calmly: "Let me switch to our recorded demo — same workflow, captured during our test session this morning." Then play it. Do not apologize more than once.

### Segment 5 — Business Impact (2 minutes)

This is the segment that separates good showcases from great ones. Present your measured impact data:

- Time saved per workflow execution
- Projected annual hours saved (extrapolated from your measurement)
- Quality improvement (error reduction, consistency increase, coverage expansion)
- Risk reduction (compliance flags that might be missed in the manual process)
- Team impact (what do your colleagues do with the time that is freed up?)

Then connect to Helm Bank's strategic priorities. How does this workflow support the bank's Latin America growth agenda? How does it strengthen the compliance posture required for correspondent banking relationships? How does it improve the client experience for commercial lending customers? The audience includes people who think about strategy. Meet them where they are.

### Segment 6 — Next Steps and Ask (60 seconds)

Close with a specific request, not a vague aspiration. "We are asking for approval to pilot this workflow with the compliance operations team for sixty days, with a formal review at the end. We need thirty minutes with the IT security team to confirm our data handling approach, and we would like to schedule a follow-up with the CCO's office to validate the output format." A concrete ask turns a presentation into a proposal.

Avoid closing with "we hope this can be deployed someday." Decision-makers in the room need something to approve or decline. Give them a clear, low-risk starting point: a pilot, a meeting, a review. Make it easy to say yes.

---

### The Showcase Framework Template

Use this template to prepare your presentation. Fill in each section before your rehearsal.

```
SHOWCASE FRAMEWORK TEMPLATE
Project Name: _______________________________
Department: _________________________________
Team Members: _______________________________
Presentation Date: __________________________

SEGMENT 1 — THE HOOK (60 seconds)
Opening story or statistic (be specific):
_____________________________________________
One-sentence project description:
_____________________________________________

SEGMENT 2 — BEFORE STATE (90 seconds)
Process being transformed:
_____________________________________________
Time/effort required today: ________________
Number of steps: ___________________________
Key risk or quality issue: _________________
Visual I will use: (flowchart / screenshot / timeline)

SEGMENT 3 — SOLUTION OVERVIEW (90 seconds)
What Copilot does: _________________________
What humans still do: ______________________
Guardrails built in: _______________________

SEGMENT 4 — LIVE DEMONSTRATION (3 minutes)
Input I will use: __________________________
Prompt key elements I will read aloud: _____
_____________________________________________
Output highlight I will point to: __________
Backup plan if demo fails: _________________

SEGMENT 5 — BUSINESS IMPACT (2 minutes)
Time saved per execution: __________________
Annual hours saved (projected): ____________
Quality improvement: _______________________
Connection to Helm Bank strategy: __________

SEGMENT 6 — NEXT STEPS AND ASK (60 seconds)
Specific request: __________________________
Resources needed: __________________________
Timeline: _________________________________
Who I need to meet with: __________________
```

---

## Three Worked Examples: Helm Bank Projects in the Studio

The following three examples show real-category Helm Bank projects being developed, tested, and framed for the Showcase. Names and specifics are illustrative; the workflows are representative of actual projects that emerged from Helm Bank's AI pilot programs.

---

### Example 1: Commercial Lending — Credit Memo First Draft Generation

**Department:** Commercial Lending, Miami headquarters
**Team:** Two relationship managers, one credit analyst
**Blueprint origin:** Chapter 16 identified credit memo preparation as consuming 4–6 hours per deal before first submission to credit committee

**The Before Story**

When a Helm Bank commercial lending relationship manager wins a new deal — a construction company in Colombia seeking a $3.2 million trade finance facility, for example — the credit memo is the first major internal document. It synthesizes the client's financial statements, the purpose and structure of the facility, the risk assessment, the country risk factors, and the collateral analysis into a 12–18 page document that the credit committee reads before approving.

Today, the relationship manager and a junior credit analyst build this document manually. The analyst pulls numbers from the audited financials, enters them into an Excel model, extracts the key ratios, and writes narrative sections describing what the numbers mean. The relationship manager writes the client background, the relationship history, and the strategic rationale. They combine the sections in Word, reformat to the template standard, and submit.

Average time: 5.5 hours from full document receipt to first submission. Credit committee turnaround: 48 hours minimum. Total deal cycle impact: significant.

**The Workflow Built in the Studio**

The team built a two-step Copilot workflow in Word:

*Step 1 — Financial Statement Analysis Prompt*

> "You are a senior credit analyst at an international commercial bank specializing in Latin American middle-market companies. I am providing the audited financial statements for [CLIENT NAME] for fiscal years [YEAR-2], [YEAR-1], and [YEAR]. Your task is to: (1) Extract the key financial metrics for each year into a structured table including revenue, EBITDA, net income, total debt, total equity, current ratio, and debt/EBITDA. (2) Identify the three most significant trends — positive or negative — in the financial performance. (3) Flag any items that would require additional due diligence or credit committee discussion. Format your output with the table first, followed by numbered trend observations, followed by a Due Diligence Flags section. Respond in English."

*Step 2 — Credit Memo Draft Prompt*

> "Using the financial analysis above and the following additional information — [relationship summary paragraph], [facility structure details], [collateral description] — draft the Financial Analysis and Risk Assessment sections of a Helm Bank commercial credit memo. Follow the standard section structure: Financial Performance Summary, Key Ratios Analysis, Risk Factors, Mitigating Factors. Write in formal, precise banking language suitable for a senior credit committee. Flag any section where additional information would strengthen the analysis. Maximum length: 600 words per section."

**Test Phase Findings**

- The financial table (Step 1) was accurate on two of three test cases. On the third — a holding company with complex intercompany eliminations — Copilot misattributed a revenue figure. *Fix: Added instruction "note any consolidation complexity and flag it for analyst review rather than making assumptions."*
- The credit memo draft (Step 2) occasionally included hedging language ("it could be argued that...") inconsistent with the authoritative tone expected in Helm Bank documents. *Fix: Added "use declarative statements; avoid hedging language or conditional phrasing."*
- Spanish-language financial statements required explicit language instruction. *Fix: Added "if the source documents are in Spanish, translate all quoted figures and terms to English in your output."*

**Measured Impact**

- Before: 5.5 hours average per credit memo
- After: 2.1 hours (analyst still reviews and edits all AI-generated content; relationship manager still writes client background and strategic rationale)
- Time saved: 3.4 hours per deal
- Volume: approximately 8–10 new credit memos per month
- Projected annual savings: 27–34 analyst-hours per month, or roughly 325–408 hours per year
- Quality note: Early drafts were more consistent in structure than manual drafts; credit committee feedback noted improved readability of the financial analysis section

**Showcase Presentation Notes**

*Hook:* "At Helm Bank, closing a new commercial deal starts with a credit memo. And for our team, that memo has historically meant a full working day — before we even get to the interesting part of our jobs. We asked: what if Copilot could handle the first draft?"

*Key visual for Before State:* A timeline showing the 5.5-hour manual process broken into five steps, with the time each step consumes. The audience immediately sees where the hours go.

*Guardrails statement:* "Every draft produced by Copilot is reviewed line by line by a credentialed credit analyst. Nothing goes to the credit committee that has not been verified by a human expert. What Copilot does is give that expert a structured starting point instead of a blank page."

*Lead impact metric for this audience (credit committee, head of commercial lending):* "Our current credit memo backlog contributes to deal cycles averaging 12 days from application to first credit committee review. We believe this workflow can reduce that by 2–3 days — which directly affects our competitive position when clients are comparing us to other lenders."

---

### Example 2: Compliance — Transaction Exception Report Triage

**Department:** Compliance Operations, BSA/AML team
**Team:** One BSA officer, one compliance analyst
**Blueprint origin:** Chapter 16 identified Monday morning exception report triage as the highest-frequency, highest-time-cost routine compliance task

**The Before Story**

Helm Bank's transaction monitoring system generates exception reports — flagged transactions that require human review — on a continuous basis, with a weekly batch delivered Monday morning. The typical Monday report contains 40–70 flagged items, each with transaction details, the rule that triggered the flag, and basic account information.

The compliance team's current process: the analyst reads every exception, categorizes it by risk level (Level 1/2/3 under internal policy), drafts a brief justification note for each Level 1 item, and compiles everything into a summary memo for the BSA officer. The BSA officer reviews, adds judgments, and sends the memo to the Chief Compliance Officer by noon.

On an average Monday, this occupies both team members from 8:00 AM to 11:30 AM — 7 combined person-hours — before any actual investigation begins.

**The Workflow Built in the Studio**

The team built a Copilot workflow using Excel (for the report data) and Word (for the memo), connected through a carefully structured prompt sequence:

*Step 1 — Exception Categorization Prompt (run in Copilot in Excel)*

> "You are a BSA/AML compliance analyst at an international bank. The table below contains transaction exceptions flagged by our monitoring system. For each exception: (1) Assign a preliminary risk level of 1 (high), 2 (medium), or 3 (low) based on the transaction amount, the triggering rule, and the account type. Use our risk criteria: Level 1 if the triggering rule is related to structuring, high-risk geography, or unusual wire patterns above $50,000; Level 2 for rule violations under $50,000 or unusual cash patterns; Level 3 for technical rule triggers with low contextual risk. (2) Write a one-sentence preliminary justification. (3) Flag any item where you lack sufficient information to categorize with note 'NEEDS REVIEW'. Output a table with columns: Exception ID, Assigned Level, Justification, Needs Review Flag."

*Step 2 — Executive Summary Memo Prompt (run in Copilot in Word)*

> "Using the categorized exception table above, draft the Monday Transaction Exception Summary memo for the Chief Compliance Officer. Structure: (1) Executive Summary — total exceptions reviewed, breakdown by risk level, any items requiring immediate escalation. (2) Level 1 Items — list each with ID, brief description, and preliminary justification. (3) Notable Patterns — if any rule categories, geographic concentrations, or account types are overrepresented this week compared to a typical week, note them. (4) Recommended Actions — for each Level 1 item, suggest the standard next step under our review protocol. Format: formal memo, from Compliance Operations to CCO, dated today, maximum 2 pages."

**Test Phase Findings**

- Categorization was consistent and conservative — when uncertain, Copilot erred toward Level 1 (higher risk), which aligned with the BSA officer's preference. No fix needed; this is the correct behavior for a compliance context.
- The "Notable Patterns" section occasionally read as speculative without sufficient data. *Fix: Added instruction "only note a pattern if at least 3 exceptions share the same characteristic; otherwise omit this section."*
- The team discovered Copilot could not access the monitoring system data directly and required manual data preparation (copy-paste from the report system into Excel). *Note for Version 2: this is where a Power Automate integration would add significant value — flagged for the next steps slide.*

**Measured Impact**

- Before: 7 combined person-hours Monday morning
- After: 2.5 combined person-hours (analyst still prepares data, BSA officer still reviews and approves all categorizations and recommendations)
- Time saved: 4.5 combined person-hours per Monday
- Annual impact: approximately 234 combined person-hours per year
- Risk improvement: AI categorization produced zero instances of a Level 1 item being initially logged as Level 3 during testing; manual process had produced 2 such miscategorizations in the prior quarter (caught in review, but requiring rework)

**Showcase Presentation Notes**

*Hook:* "Seven hours every Monday. That is what our compliance team was spending before a single investigation began. We are not talking about low-skill work — we are talking about two of our most knowledgeable BSA officers. We decided to build something that gives them their Monday mornings back."

*Key visual for Before State:* A Monday morning timeline from 8:00 AM to 11:30 AM, color-coded by activity. The visual makes instantly clear that the first three and a half hours are consumed by structuring and documentation — not investigation.

*Guardrails statement:* "The AI categorization is preliminary. Our BSA officer reviews every Level 1 designation individually and has overridden AI categorizations in testing when additional relationship context changed the risk picture. The AI does not make compliance decisions — it organizes information so our human experts can make those decisions faster."

*Lead impact metric for this audience (CCO, Chief Risk Officer):* "Two miscategorized Level 1 items in the prior quarter — caught in review but requiring rework — represent the kind of process error that, in a different context, could contribute to a regulatory finding. Our workflow's conservative categorization bias has produced zero such errors across all test runs."

---

### Example 3: Relationship Management — Client Communication Drafts for the Latin America Corridor

**Department:** International Banking, Relationship Management
**Team:** Three relationship managers covering Colombia, Mexico, and Peru corridors
**Blueprint origin:** Chapter 16 identified client communication drafting — especially cross-language, cross-culture correspondence — as a high-friction activity consuming disproportionate time relative to its complexity

**The Before Story**

Helm Bank's Latin America corridor relationship managers maintain active relationships with dozens of correspondent banks, corporate clients, and institutional partners in Spanish-speaking markets. Client communication is constant: loan status updates, documentation request letters, market commentary, annual review invitations, and relationship nurture messages.

Each communication requires careful calibration. Helm Bank's Miami-based relationship managers must write in English and often Spanish; they must strike a tone that is professional but warm — relationship banking is deeply relational in Latin American business culture; they must reference the correct regulatory and compliance context; and they must personalize appropriately to the individual client relationship.

A single well-crafted client letter — say, an annual credit facility renewal notification for a long-standing correspondent banking partner in Bogotá — can take 45–90 minutes to write, review, and translate. The relationship manager typically produces 8–12 such communications per week.

**The Workflow Built in the Studio**

The team built a Copilot workflow in Outlook with Word drafting support, using a prompt template system that allowed rapid variable substitution:

*Primary Communication Drafting Prompt*

> "You are a senior relationship manager at Helm Bank, a Miami-based international bank specializing in the US–Latin America corridor. You have been working with [CLIENT NAME] at [INSTITUTION], [CITY, COUNTRY] for [RELATIONSHIP DURATION]. The tone of this relationship is [professional and warm / formal / friendly]. I need to write a [COMMUNICATION TYPE] regarding [TOPIC]. Key points to include: [BULLET LIST OF FACTS]. If writing in Spanish: use formal usted address, appropriate regional conventions for [COUNTRY], and ensure the tone reflects the warmth and relationship orientation expected in Latin American business correspondence. If writing in English: maintain Helm Bank's professional international banking voice. Output: Subject line, opening paragraph, body (2–3 paragraphs), closing paragraph, and signature block. Length: [SHORT (under 300 words) / MEDIUM (300–500 words) / LONG (500–800 words)]."

The team created a Copilot prompt template saved as a custom instruction set, allowing relationship managers to fill in the bracketed variables quickly rather than rewriting the full prompt each time.

*Follow-Up Tone Review Prompt*

> "Review the draft letter above. Identify any passages that could be perceived as overly formal, cold, or transactional for a relationship banking context in [COUNTRY]. Suggest specific revisions that maintain professionalism while increasing warmth and relationship orientation. Also flag any cultural considerations specific to [COUNTRY] business correspondence that the draft does not account for."

**Test Phase Findings**

- English drafts were consistently strong and required minimal editing.
- Spanish drafts required the relationship managers to review for regional vocabulary preferences — Copilot sometimes used generic Latin American Spanish where Colombia-specific expressions would be more appropriate. *Fix: Added country-specific instruction; team created a companion notes file of preferred regional expressions for each corridor country.*
- The tone review prompt (Step 2) was unexpectedly valuable — it surfaced a subtle issue in one draft where a payment reminder was phrased in a way that could read as accusatory in the Colombian business context. The relationship manager corrected it before sending. This became a centerpiece of the showcase: "Copilot didn't just draft the letter — it helped us catch a relationship risk before it happened."
- Bilingual documents (English body, Spanish P.S. or vice versa) required explicit structure instruction. *Fix: Added "if the document contains both English and Spanish sections, clearly label each section by language."*

**Measured Impact**

- Before: 45–90 minutes per complex communication; 10–15 minutes for simple updates
- After: 10–20 minutes per complex communication; 3–5 minutes for simple updates
- Average time savings: 35–70 minutes per complex communication
- Volume: 8–12 communications per relationship manager per week across a 3-person team = 24–36 communications per week
- Weekly team savings: 14–42 hours per week (range reflects communication complexity mix)
- Midpoint estimate: approximately 28 hours per week of relationship manager time redirected from drafting to actual relationship activities
- Strategic impact: Team estimated they could increase active portfolio coverage by 15–20% with the recovered time, without adding headcount

**Showcase Presentation Notes**

*Hook:* "Relationship banking is about time with clients, not time at the keyboard. But our relationship managers were spending up to ninety minutes crafting a single letter. We built something that handles the drafting — so they can spend that ninety minutes on a call to Bogotá instead."

*Key visual for Before State:* A pie chart of how a relationship manager's week is currently spent: time with clients, time on internal meetings, time on documentation and administration, time on drafting communications. The drafting slice is larger than audiences expect.

*Guardrails statement:* "Every draft is reviewed by the relationship manager before it is sent. The manager knows the client. They add the personal touches, the specific references to conversations, the nuances that no AI can know. What Copilot does is handle the structure and language, so the manager can focus on the relationship intelligence that only they have."

*Lead impact metric for this audience (Head of International Banking, Chief Revenue Officer):* "A 15–20% increase in active portfolio coverage from the same team, without headcount additions, translates directly to revenue capacity. At Helm Bank's average corridor deal size, that coverage expansion represents meaningful pipeline growth."

---

## The Refine Phase: Making Surgical Improvements

With your test findings documented, the Refine phase is not a second Build phase. You are not starting over. You are making the smallest changes that produce the largest improvement.

Prioritize your refinements using this simple triage: What failure mode would be *most visible* to your showcase audience? What would undermine the audience's confidence in the workflow most significantly? Fix that first. Everything else goes on the Version 2 list.

Common high-value refinements that take five minutes or less:

**Tighten output length.** If Copilot is producing outputs that are too long for your use case, add a specific word or paragraph limit. This single instruction change often produces a dramatically more useful output.

**Add a confidence flag.** Instruct Copilot to add a sentence at the end of its output: "If any part of this analysis relies on assumptions rather than stated facts in the source document, flag those assumptions explicitly." This one instruction dramatically reduces hallucination risk in factual analysis tasks.

**Specify what to omit.** If Copilot consistently includes disclaimers, caveats, or meta-commentary you do not want ("As an AI, I should note that..."), add explicit negative instructions: "Do not include AI disclaimers or meta-commentary about the analysis process. Write as if you are the human expert producing this document."

**Calibrate the reading level.** If your audience is senior leadership, add "write at an executive reading level: precise, confident, and jargon-free." If your audience is technical specialists, add "use standard industry terminology without simplification."

**Anchor to Helm Bank standards.** If outputs need to conform to internal style standards, add a brief style note: "Match the tone and structure of Helm Bank's standard [document type] format." If you have a sample document available, paste the key structural elements as a reference.

```{admonition} Workshop Exercise
:class: important

**The Five-Minute Refinement**

For each issue identified in your Test Log, apply this discipline:

1. Write the issue in one sentence.
2. Write the single prompt change you will make to address it.
3. Make that change only — run the prompt — evaluate.
4. If the issue is resolved, move to the next item.
5. If not resolved after two iterations, add it to the Version 2 list and move on.

Participants who spend more than ten minutes on a single issue during the Refine phase almost always run out of time for the Showcase Framework preparation. Time-box your refinements ruthlessly. A 90%-right prompt that you demonstrate confidently is more persuasive than a 99%-right prompt that you never finish.
```

---

## Framing Your Before/After Story for Maximum Impact

The Showcase Framework gives you structure. Within that structure, the before/after story is your most powerful persuasion tool. Here is how to make it land.

**Make the "before" specific and costly.** Audiences tune out vague inefficiency ("it takes a long time and is kind of annoying"). They lean forward when the cost is concrete: "Two analysts, every Monday morning, for three and a half hours — before a single real compliance decision gets made."

**Make the "after" credible, not miraculous.** Do not claim AI does everything better than humans. Claim what it actually does: "Copilot produces the first draft of the categorization and memo. Our BSA officer still reviews every single item and makes every final determination. What changed is how long that review takes."

**Show the human in the workflow.** Helm Bank leadership is sophisticated about AI. They know that unsupervised AI in a regulated banking environment is not acceptable. Your showcase gains credibility — not loses it — when you clearly articulate what humans still control, decide, and approve. The most persuasive AI transformation story is not "AI replaced the human" — it is "AI gave the human more time to do what only a human can do."

**Use the number that matters most.** Every project has multiple impact metrics. For your showcase, lead with the one that resonates most with your specific audience. For the CCO, it might be the reduction in uncategorized exceptions. For the CFO, it might be the hours saved translated to FTE cost. For the Head of Relationship Management, it might be the increase in client-facing time. Know your audience and lead with their number.

**Acknowledge the limits honestly.** The most credible showcase presentations include a moment of honest limitation: "Our workflow currently requires the analyst to prepare the data manually before running the Copilot prompt — we have not yet automated the data ingestion step. That is our Version 2 target." Audiences — especially in banking, where risk awareness is core to the culture — trust presenters who show they understand where the guardrails are. A presenter who claims their AI workflow is perfect has clearly not tested it.

---

## Handling Tough Questions in the Showcase

Even with thorough preparation, your showcase will generate questions. Here are the most common categories and how to address them:

**"How do we know the AI output is accurate?"**
"We test every workflow against known outputs — cases where we already have the correct answer — and verify the AI reaches the same conclusion. For any production deployment, we recommend a parallel-run period where AI outputs and manual outputs are compared for a defined number of cases before transitioning fully."

**"What happens if Copilot is wrong and we act on bad information?"**
"That is exactly why we have built human review into every step of this workflow. No AI output in our design reaches a client, a regulator, or a credit committee without a credentialed team member signing off. The AI is a first-draft tool — accountability remains with the professional."

**"How much does this cost to deploy?"**
"The Copilot licenses are already included in our Microsoft 365 E3/E5 agreement. The development investment for this workflow was approximately [X hours] of staff time across the workshop period. The implementation cost for a production pilot is primarily the IT security review and a short training period — both of which we have scoped in our next steps."

**"Could this put someone's job at risk?"**
"Our impact analysis shows time savings that we are projecting into portfolio growth and service quality improvement — not headcount reduction. The same team that currently manages [X] relationships would be positioned to manage [X + 15-20%] relationships. We are growing the pie, not cutting the team."

---

## Chapter Summary

The Showcase Project Development Workshop is where this program's investment becomes tangible. In a single 150-minute session, you move from a blueprint and a set of learned techniques to a working, tested, demonstrable AI transformation project — and a polished framework for presenting it to your organization.

The key principles to carry forward from this chapter:

**Build narrow and deep.** A workflow that does one thing reliably is more valuable than a demonstration that attempts five things and wobbles on all of them. Choose the highest-impact, most demonstrable element of your blueprint and execute it cleanly. Breadth is a Version 2 story.

**Test honestly.** The debugging protocol exists not to make you look bad but to make your workflow genuinely better. Teams that test rigorously produce showcases that hold up under the audience's questions — because they already asked those questions themselves. Stress-test your workflow before your audience does.

**Tell the before story first.** Technology impresses. Problems resonate. Always start with the pain your project solves. The audience needs to feel the friction before they can appreciate the relief.

**Quantify everything you can.** Time saved is powerful. But time saved translated to what your team can do with that time is transformative. Push your impact story one level deeper than the obvious number — from "hours saved" to "deals closed faster" or "clients covered without adding headcount."

**Keep humans in the loop and say so.** In a regulated financial institution, AI that operates without human oversight is not a feature — it is a liability. Your showcase is stronger, not weaker, when you articulate clearly where human judgment remains essential. The compliance culture of Helm Bank is an asset in this context: you already know how to build guardrails.

**The Showcase Framework is your confidence architecture.** Ten minutes feels short. The framework ensures every second carries weight. Segment 5 — Business Impact — is where most presentations underinvest. Plan your two minutes of impact before you plan your three minutes of demo. The demo is the proof; the impact is the point.

**Acknowledge limits to gain trust.** The most credible presenters in any showcase are the ones who know where their workflow's boundaries are — and say so. A Version 2 list is not a confession of failure. It is evidence that you think like a professional deploying a real system, not a student submitting a homework assignment.

The work you built today does not end when this session closes. Your workflow is now a prototype. The next step — whether it is a sixty-day pilot, an IT security review, or a conversation with your department head — is the ask you will make in Segment 6 of your showcase.

Make the ask specific. Make it actionable. Make it easy to say yes to. The most important thing about a Final Showcase at Helm Bank is that it produces real decisions, real pilots, and real transformations — not applause and then a return to the old way of working.

The final showcase is one session away. You are ready.

---

## Key Terms

**Before/After Story** — The narrative structure that grounds a technology demonstration in a specific, quantified business problem and its resolution. The single most important persuasion tool in a showcase presentation.

**Confidence Flag** — A prompt instruction directing Copilot to explicitly identify any assumption it makes that is not grounded in the source document. A key hallucination-reduction technique for high-stakes banking workflows.

**Prompt Architecture** — The deliberate design of an AI prompt using four elements: role assignment, context injection, task specification, and format instruction. The foundation of a reliable, repeatable Copilot workflow.

**Showcase Framework** — The six-segment, 10-minute presentation structure used in the Helm Bank AI Copilot Showcase: Hook, Before State, Solution Overview, Live Demonstration, Business Impact, and Next Steps and Ask.

**Studio Session** — A structured work session in which participants function as creators and the instructor functions as a resource; the primary mode of the Showcase Project Development Workshop. Modeled on professional design and engineering lab practice.

**Stress Testing** — The practice of deliberately running an AI workflow on edge-case, adversarial, or unusual inputs to surface failures before production deployment. Essential for any workflow that will be used in a regulated environment.

**Synthetic Data** — Fictional but realistic data created for testing and demonstration purposes, used in place of real client data to maintain compliance with privacy regulations and Helm Bank data governance policies.

**Test Log** — A structured record of outputs, failure types, identified root causes, and applied fixes maintained during the Test phase of the development studio.

---

## Looking Ahead

**Chapter 19 — The Final Showcase: Presenting Your AI Transformation** walks you through the showcase event itself: logistics, audience dynamics, how to handle tough questions from senior leadership, and what happens after your presentation. It also introduces the Helm Bank AI Adoption Scorecard — the framework leadership uses to evaluate projects for pilot approval and eventual deployment across the institution.

Your prototype is built. Your story is ready. In the final session, you make the case for what comes next. The room will include decision-makers. Come prepared to make decisions happen.

---

*End of Chapter 18*

---

```{admonition} Quick Reference — Studio Session Checklist
:class: tip

**Before the session:**
- [ ] Review Chapter 16 blueprint and Chapter 17 integration notes
- [ ] Prepare test data (synthetic or anonymized — NO real client data)
- [ ] Write your four-question before story

**Phase 1 — Orient (20 min):**
- [ ] Confirm project scope (one workflow, one deliverable)
- [ ] Assign team roles if working in a group
- [ ] Write before story with quantification

**Phase 2 — Build (60 min):**
- [ ] Draft prompt architecture (role / context / task / format)
- [ ] Build primary Copilot workflow
- [ ] Capture a screen recording of first successful run

**Phase 3 — Test (30 min):**
- [ ] Run primary test
- [ ] Run stress test (edge case, adversarial, language variant)
- [ ] Complete test log with failure types and root causes

**Phase 4 — Refine (20 min):**
- [ ] Prioritize top 2–3 issues by showcase visibility
- [ ] Make surgical fixes only — one element at a time
- [ ] Retest after each fix; add unresolved issues to Version 2 list

**Phase 5 — Frame (20 min):**
- [ ] Complete Showcase Framework Template
- [ ] Practice opening hook aloud (60 seconds max)
- [ ] Identify your lead impact metric for your specific audience
- [ ] Confirm backup demo plan (screen recording ready)
- [ ] Write your specific ask for Segment 6
```
