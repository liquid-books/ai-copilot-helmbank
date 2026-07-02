---
title: "Chapter 11: Week 4, Session A — Advanced Prompting"
subtitle: "From Power User to Prompt Architect"
short_title: "Advanced Prompting"
description: "Taking prompting to the next level — system prompts, iterative refinement, multi-turn conversation design, prompt templates, Copilot Pages, and building a personal prompt library for Helm Bank banking professionals."
label: ch-11-advanced-prompting
tags: [advanced prompting, system prompts, iterative prompting, prompt templates, Copilot Pages, Helm Bank, Microsoft 365, multi-turn, prompt library, banking]
---

```{admonition} Download this Chapter as PDF
:class: tip
[Download PDF](https://github.com/liquid-books/ai-copilot-helmbank/raw/main/pdfs/ch11-advanced-prompting.pdf)
```

# Chapter 11: Advanced Prompting — From Power User to Prompt Architect

---

## The Monday Morning That Changed Everything

It's 7:52 AM on a Monday. Valeria, a Senior Relationship Manager at Helm Bank's Brickell office, is staring at her screen. A long-standing client — a Colombian textile exporter with $4.2 million in annual wire volume — has just sent a terse message: *"I need to understand what's happening with my last three transactions. Call me before noon."*

The client, Don Alberto, is not a complainer. When he says something's wrong, something is wrong.

Valeria has forty minutes before her first internal meeting. She needs to pull three months of transaction records, cross-reference them against OFAC holds from the compliance team, draft a clear explanation of what happened, and prepare speaking points for a sensitive conversation — all while keeping the relationship intact.

Six months ago, this would have taken half a day and a prayer.

Today, Valeria opens Copilot in Microsoft Teams and types — not a generic question, but a carefully constructed prompt she's been refining for exactly these situations:

> *"You are a senior relationship manager at an international bank serving Latin American clients. A valued Colombian client is concerned about delays in three recent wire transfers. My role is to de-escalate and retain the relationship while being honest about compliance-related holds. Help me prepare for a sensitive client call. I'll give you the transaction details. Start by asking me clarifying questions."*

Copilot responds with a structured set of questions. Valeria pastes in the relevant data. The conversation that follows — seven turns, twelve minutes — produces a client-ready explanation, a list of empathy-first talking points, a follow-up email draft, and a note flagging a possible regulatory pattern worth escalating to compliance.

She makes the call at 9:15. Don Alberto is not just satisfied. He's impressed.

What Valeria did wasn't magic. It was *architecture*. She didn't just prompt — she designed a conversation. That's what this chapter is about.

---

## Beyond the Five Basics

By now, you've internalized the five foundations of effective prompting: **Role, Task, Context, Format, and Constraints**. You know how to give Copilot clear instructions, how to ground your requests in specifics, and how to get clean, usable outputs.

That's Power User territory. It's genuinely valuable. But there's a next level.

In this chapter, we're going to move from *using* prompts to *designing* them. We'll cover:

1. **System prompts** — setting the stage before the conversation begins
2. **Iterative refinement** — treating the first response as a draft, not a deliverable
3. **Multi-turn conversation design** — orchestrating dialogue like a director, not just a participant
4. **Prompt templates** — creating reusable structures that your whole team can use
5. **Copilot Pages** — a collaborative surface for shared prompt work and living documents
6. **Building your personal prompt library** — your professional edge, packaged and portable

Every concept will be anchored in Helm Bank's world: commercial lending, compliance, cross-border transactions, relationship management, and the HelmInOne platform. These aren't abstract techniques. They're tools for your actual daily work.

Let's build.

---

:::{figure} ../images/ch11-advanced-prompting-infographic.png
:alt: A visual roadmap of the six advanced prompting concepts covered in Chapter 11 — system prompts, iterative refinement, multi-turn design, prompt templates, Copilot Pages, and personal prompt libraries — arranged as ascending steps on a staircase, with a Helm Bank-branded color palette of navy and gold. Each step is labeled with an icon representing the concept.
:width: 90%
:align: center

*The six pillars of advanced prompting at Helm Bank. Each builds on the last — master all six and you become a Prompt Architect.*
:::

---

## System Prompts: Establishing the Stage

Think of a system prompt as the briefing you give a new analyst before they walk into their first client meeting. You're not just assigning a task — you're establishing *context, role, tone, and operating parameters* before the conversation even starts.

In Microsoft Copilot, a system prompt is the first message you send in a new conversation thread — one that sets the frame for everything that follows. Done well, it means you don't have to re-explain yourself with every follow-up question.

### Anatomy of a Strong System Prompt

A well-built system prompt has four components:

**1. Identity** — Who is Copilot being asked to be?
**2. Situation** — What's the context or scenario?
**3. Constraints** — What are the rules, limitations, or sensitivities?
**4. Invitation** — How should Copilot begin engaging?

Here's a bare example:

> *"You are a [role] helping me with [situation]. Key constraints: [list]. Begin by [action]."*

And here's what that looks like in a real Helm Bank scenario:

```{admonition} Helm Bank Application
:class: note

**System Prompt — Compliance Pre-Screening:**

*"You are a compliance analyst at an international bank specializing in Latin American correspondent banking. I'm a relationship manager preparing a new client file for KYC review. Your job is to help me identify potential red flags, missing documentation, and questions I should anticipate from the BSA team. Be rigorous but not alarmist. Ask me for information you need rather than making assumptions. Do not provide legal advice. Let's begin — I'll describe the client."*

This single prompt, sent at the start of a Copilot session, transforms the tool into a focused compliance-prep partner rather than a general-purpose assistant.
```

### Why System Prompts Matter So Much

Without a system prompt, Copilot operates in a kind of neutral default mode — helpful, but generic. With a good system prompt, it's calibrated to your world, your role, and your constraints. The difference is enormous.

Consider these two requests about the same situation:

:::::{tab-set}
::::{tab-item} Without System Prompt
**Prompt:**
*"What documents are needed for a new corporate client from Venezuela?"*

**Result:** A generic list of KYC documents with no bank-specific context, no sensitivity to current OFAC designations, no awareness of Helm Bank's risk appetite, and no differentiation between entity types.

**What you get:** Adequate. Wikipedia-level. You'll spend ten minutes editing it to be useful.
::::

::::{tab-item} With System Prompt
**System Prompt first:**
*"You are a KYC specialist at Helm Bank, a Miami-based international bank serving the US-Latin America corridor. Helm Bank has a conservative risk posture toward Venezuelan-domiciled entities given current OFAC environment. Help me build a client onboarding checklist for a new corporate account. Ask clarifying questions about the entity structure before generating the checklist."*

**Follow-up prompt:**
*"New client: Venezuelan-registered holding company with US subsidiaries, family-owned, petroleum sector."*

**Result:** A nuanced, sector-aware checklist that specifically addresses UBO documentation for holding companies, petroleum sector enhanced due diligence, and the OFAC considerations for Venezuelan nationals — with a note to confirm specific requirements with Helm Bank's BSA team.

**What you get:** A working draft you can actually take to the compliance team.
::::
:::::

The same underlying question. Dramatically different outputs. The system prompt is the difference.

### System Prompt Templates for Helm Bank Roles

Here are ready-to-use system prompts for common Helm Bank roles:

**For Relationship Managers:**
> *"You are a senior relationship manager at Helm Bank, a Miami-based international bank serving clients across the US-Latin America corridor. I work with commercial clients in [sector]. Help me with client communications, account planning, and relationship strategy. Keep responses professional, empathetic, and client-focused. I'll tell you what I need."*

**For Commercial Lending Officers:**
> *"You are a commercial lending analyst at an international bank with expertise in cross-border credit structures. I'm preparing credit memos, financial analysis, and deal structures for clients doing business between Latin America and the United States. Be precise, use standard banking terminology, and flag assumptions clearly. Ask for financial data when you need it."*

**For Operations and Wire Teams:**
> *"You are a banking operations specialist with expertise in international wire transfers and correspondent banking. Help me draft client communications about wire delays, prepare internal escalation notes, and troubleshoot transaction issues. Be clear, accurate, and never promise specific resolution timelines."*

**For HelmInOne Platform Support:**
> *"You are a digital banking specialist helping Helm Bank clients use the HelmInOne platform. I'll describe client issues or questions about the platform. Help me draft clear, step-by-step responses. Use simple language appropriate for clients who may not be tech-savvy. Escalate anything involving actual transaction errors."*

---

## Iterative Refinement: The First Response Is a Draft

Here's the mindset shift that separates good prompters from great ones: **the first response is never the final answer**. It's a starting point — a draft that you shape, push, and refine through conversation.

This isn't a limitation of Copilot. It's how good thinking works. A first draft clears the fog. The second and third drafts are where quality emerges.

### The Refinement Toolkit

When you receive a first response, you have a set of refinement moves available to you:

| Move | What You Say | When to Use It |
|------|-------------|----------------|
| **Zoom In** | *"Expand the section on [X]"* | When a point is too brief |
| **Zoom Out** | *"Give me a one-paragraph summary of this"* | When the response is too dense |
| **Reframe** | *"Rewrite this for a [different audience]"* | When tone or level is wrong |
| **Redirect** | *"That's not quite right — [correction]. Try again."* | When the response misses the mark |
| **Sharpen** | *"Make this more specific to [context]"* | When it's too generic |
| **Challenge** | *"What are the weaknesses in this approach?"* | To stress-test analysis |
| **Extend** | *"Now add a section on [X]"* | To build on what works |
| **Format Shift** | *"Convert this to a table / bullet list / email"* | To change the output structure |

The key is not to accept the first response passively. Engage with it. React to it. Push back. That's when Copilot becomes genuinely powerful.

### Refinement in Practice: A Credit Memo Example

Watch how this works across a real Helm Bank workflow:

**Turn 1 — Initial request:**
> *"Write a summary of a commercial loan request for a Miami-based freight forwarding company seeking a $1.2 million revolving line of credit to support trade finance operations between Miami and Medellín."*

*Copilot produces a solid but generic two-paragraph summary.*

**Turn 2 — Zoom in and sharpen:**
> *"Good start. Now add specific risk factors relevant to a logistics company with heavy Colombia exposure. Include currency risk, counterparty concentration, and cargo insurance considerations."*

*Copilot expands with relevant risk factors.*

**Turn 3 — Challenge:**
> *"Now play devil's advocate. If you were a credit committee member skeptical of this deal, what questions would you ask?"*

*Copilot generates a pointed list of committee questions — exactly what the lending officer needs to prepare for.*

**Turn 4 — Format shift:**
> *"Convert the risk factors section into a table with three columns: Risk Factor, Description, and Proposed Mitigation."*

*Clean, presentation-ready table.*

**Turn 5 — Reframe:**
> *"Now rewrite the executive summary paragraph as if it were written by the lending officer making a recommendation to approve, with appropriate confidence and professional tone."*

Four refinement moves, five turns. The result is a credit memo draft that would have taken two hours to write from scratch, produced in under fifteen minutes — and because the lending officer engaged with the process, they know the content cold before it ever goes to committee.

```{admonition} Helm Bank Application
:class: note

**Iterative Refinement for Client Proposals:**

Helm Bank's trade finance team uses a three-pass refinement process for client proposals:

- **Pass 1:** Generate the structural draft (what sections, what data points)
- **Pass 2:** Sharpen the language and add client-specific details
- **Pass 3:** Reframe for the client's cultural context (Colombian business culture differs from Venezuelan, which differs from Argentine — tone, formality, and relationship framing matter)

The third pass — cultural calibration — is something that used to require a senior banker's review. Now it's built into the prompting workflow.
```

---

:::{figure} ../images/ch11-iterative-refinement-workflow.png
:alt: A circular diagram showing the iterative prompting workflow with five stages arranged in a loop: Draft Request, Review Output, Select Refinement Move, Send Follow-up Prompt, and Evaluate Result. Arrows connect each stage in sequence, with a branch at the Evaluate Result stage for either Accept or Refine Again. The diagram uses Helm Bank's navy and gold color scheme with clean sans-serif typography.
:width: 80%
:align: center

*The iterative refinement loop. Most valuable outputs come from the third or fourth pass, not the first.*
:::

---

## Multi-Turn Conversation Design

Iterative refinement is about improving a single output. Multi-turn conversation design is bigger — it's about *orchestrating an entire dialogue* to reach a complex goal.

Think of it like planning a meeting before you walk in. You know the outcomes you need. You structure the agenda. You know what questions to ask in what order. You anticipate where the conversation might stall and have a recovery move ready.

Multi-turn conversation design applies that same intentionality to your Copilot sessions.

### The Three-Act Structure

High-quality multi-turn Copilot conversations tend to follow a natural three-act structure:

**Act 1: Establish and Explore**
Set the system prompt. Establish role and context. Ask Copilot to surface what it needs from you. This is the briefing phase — don't rush it.

**Act 2: Build and Refine**
Do the substantive work. Provide data. Generate outputs. Refine. Challenge. Extend. This is the production phase — most of your turns happen here.

**Act 3: Package and Deliver**
Ask Copilot to synthesize, format, and prepare the output for its intended audience. Reframe if needed. Clean up. This is the delivery phase — don't skip it.

### A Full Multi-Turn Design: Cross-Border Compliance Review

Here's a complete multi-turn conversation design for one of the most complex tasks in Helm Bank's daily operations: preparing a client file for enhanced due diligence on a cross-border transaction.

---

**CONVERSATION DESIGN: Enhanced Due Diligence Prep**

**Goal:** Prepare a structured EDD summary for a new corporate client sending high-value wires between Panama and Miami.

**Pre-conversation planning:**
- Client: Panamanian holding company, construction sector
- Transaction pattern: Bi-weekly wires, $200K–$400K range
- Trigger: Transaction volume crossed threshold requiring EDD review
- Deadline: BSA team review in 48 hours

---

*Act 1 — Establish:*

**Turn 1:**
> *"You are an enhanced due diligence specialist at an international bank. I'm a relationship manager preparing an EDD file for a Panamanian corporate client in the construction sector. The client sends bi-weekly wires to Miami in the $200K–$400K range. I need to build a structured summary for BSA review. Before we start, what key information should I gather about this client?"*

*Copilot produces a structured information-gathering checklist.*

*Act 2 — Build:*

**Turn 2:**
> *"Here's what I have: [paste client summary data]. Based on this, identify the three highest risk factors that BSA will focus on."*

**Turn 3:**
> *"For each risk factor, suggest the specific documentation or explanation that would address BSA's likely concern."*

**Turn 4:**
> *"The client's ownership structure has three layers — a Panamanian holding company owned by a BVI entity owned by two Colombian nationals. Draft the beneficial ownership narrative section of the EDD report."*

**Turn 5:**
> *"Now draft the 'Source of Funds' section. The client has provided a three-year audited financial statement showing construction project revenues from Colombian infrastructure contracts."*

**Turn 6:**
> *"We have a gap — the client hasn't provided the underlying construction contracts. Draft an email to the client requesting this documentation without alarming them or making it sound like they're under investigation."*

*Act 3 — Package:*

**Turn 7:**
> *"Now synthesize everything into a structured EDD summary report. Format: Executive Summary (3 sentences), Client Profile, Risk Assessment (use High/Medium/Low ratings), Documentation Status (table format), Outstanding Items, Relationship Manager Recommendation."*

Seven turns. A complete EDD prep package. The kind of work that used to take a half-day of back-and-forth between the RM, the BSA team, and the client.

```{admonition} Helm Bank Application
:class: note

**Conversation Design for Loan Structuring:**

The commercial lending team at Helm Bank uses a five-turn conversation design for preliminary loan structuring:

1. **Turn 1:** Feed Copilot the client's financial summary and ask for the three most viable loan structures
2. **Turn 2:** For the preferred structure, identify the covenant package
3. **Turn 3:** Draft the term sheet executive summary
4. **Turn 4:** Anticipate client objections to the proposed structure
5. **Turn 5:** Draft the follow-up email to schedule the term sheet presentation

The entire sequence takes 20 minutes and produces materials that were previously assembled across two or three separate meetings.
```

### Conversation Design Principles

**Principle 1: Front-load the context.** Everything important belongs in Act 1. Don't trickle in critical information — it forces Copilot to revise its mental model mid-conversation.

**Principle 2: One objective per turn.** Resist the temptation to pack multiple requests into a single message. "Write the summary AND convert it to a table AND make it shorter" produces worse results than three sequential turns.

**Principle 3: Name the transition.** When moving from Act 1 to Act 2, or Act 2 to Act 3, signal the shift explicitly: *"Okay, we have enough context. Now let's build the actual document."*

**Principle 4: Bank the wins.** When a turn produces something excellent, say so: *"That risk assessment is exactly right. Keep that framing for the rest of the document."* Explicit affirmation within a session anchors the successful elements.

**Principle 5: Close the loop.** End complex sessions with a synthesis request. Even if you've built things piece by piece, ask for a final consolidated output before you close the tab.

---

## Prompt Templates: Standardize Your Best Thinking

If iterative refinement is about improving a single output, and multi-turn design is about orchestrating a conversation, **prompt templates** are about capturing your best work so you never have to rebuild it from scratch.

A prompt template is a tested, reusable prompt structure — one that has already been refined through real use and reliably produces quality outputs. It's the difference between improvising every time and having a playbook.

### Anatomy of a Prompt Template

A good prompt template has four parts:

```
[TEMPLATE NAME]: Short descriptive name

[SYSTEM SETUP]: The role and context framing

[TASK STRUCTURE]: The actual prompt with [BRACKETS] for variables

[EXAMPLE OUTPUT]: What a good response looks like (optional but valuable)
```

The brackets are the key — they mark the parts you'll customize each time you use the template.

### Helm Bank Prompt Template Library: Starter Pack

Here are five production-ready templates for common Helm Bank workflows:

---

**Template 1: Client Communication — Sensitive Situation**

```
[SYSTEM]: You are a senior relationship manager at an international bank
serving Latin American clients. You write with empathy and professionalism.

[TASK]: Draft a client communication for the following situation:
- Client Name: [CLIENT NAME]
- Client Relationship Level: [VIP / Standard / New]
- Issue: [DESCRIBE THE PROBLEM]
- Our Role in the Issue: [Our fault / Third-party / Regulatory hold / Client error]
- Desired Outcome: [Retain relationship / Provide explanation / Request documentation]
- Tone: [Empathetic / Formal / Apologetic / Matter-of-fact]
- Format: [Email / Call talking points / WhatsApp message]

Begin with an empathetic acknowledgment. Close with a clear next step.
```

---

**Template 2: Credit Memo — Executive Summary**

```
[SYSTEM]: You are a commercial lending analyst at an international bank
with expertise in US–Latin America trade finance.

[TASK]: Write a credit memo executive summary for:
- Borrower: [COMPANY NAME AND DESCRIPTION]
- Loan Type: [Revolving LOC / Term Loan / Trade Finance Facility]
- Amount: [LOAN AMOUNT]
- Purpose: [USE OF PROCEEDS]
- Key Strengths: [LIST 2-3]
- Key Risks: [LIST 2-3]
- Recommendation: [Approve / Approve with conditions / Decline]

Format: 3 paragraphs. Paragraph 1: Borrower and request overview.
Paragraph 2: Credit strengths. Paragraph 3: Risks and recommendation.
Use formal credit memo language throughout.
```

---

**Template 3: Compliance — Transaction Narrative**

```
[SYSTEM]: You are a BSA/AML compliance analyst at an international bank.
You write clear, factual transaction narratives for regulatory review.

[TASK]: Draft a transaction narrative for the following:
- Transaction Date(s): [DATE(S)]
- Amount(s): [AMOUNTS AND CURRENCIES]
- Originator: [NAME / ENTITY]
- Beneficiary: [NAME / ENTITY]
- Stated Purpose: [WHAT CLIENT SAYS]
- Supporting Documentation: [WHAT WE HAVE]
- Flags or Concerns: [ANY RED FLAGS]

Write in past tense, third person. Be factual, not speculative.
Note documentation gaps clearly. Do not include conclusions about
suspicious activity — describe facts only.
```

---

**Template 4: Meeting Prep — Client Review Call**

```
[SYSTEM]: You are a senior relationship manager preparing for a
quarterly client review call at an international bank.

[TASK]: Prepare a call agenda and talking points for:
- Client: [NAME AND BRIEF DESCRIPTION]
- Relationship Duration: [X] years
- Key Products: [LIST]
- Recent Issues or Highlights: [DESCRIBE]
- Business Goals This Quarter: [WHAT WE WANT TO ACHIEVE]
- Client Concerns (if known): [DESCRIBE]

Output:
1. Agenda (5 items max, with time allocations)
2. Opening talking points (relationship affirmation)
3. Business points (specific asks or offers)
4. Closing (next steps, follow-up)
5. One "surprise delight" idea (something we can offer that the client doesn't expect)
```

---

**Template 5: HelmInOne Platform — Client Onboarding Guidance**

```
[SYSTEM]: You are a digital banking specialist helping Helm Bank clients
use the HelmInOne platform. Write clearly for clients who may not be
technically sophisticated.

[TASK]: Draft a step-by-step guide for:
- Client Type: [Individual / Business]
- Language: [English / Spanish / Portuguese]
- Task: [DESCRIBE WHAT CLIENT NEEDS TO DO ON PLATFORM]
- Known Issue or Obstacle: [IF ANY]
- Preferred Format: [Email / WhatsApp / PDF guide]

Use numbered steps. Include what to expect at each step.
Flag anything that requires Helm Bank staff assistance.
Close with contact information for support.
```

---

```{admonition} Helm Bank Application
:class: note

**Template Governance at Helm Bank:**

The most effective teams at Helm Bank maintain a shared prompt template library in a Teams channel or SharePoint folder. New templates get peer-reviewed before being added to the shared library. Templates are versioned (v1.0, v1.1) and include a "Last Tested" date.

This isn't bureaucracy — it's quality control. A template that was sharp six months ago may need updating as Copilot improves, regulations change, or the bank's offerings evolve. Treat your prompt library like you treat your policy manuals: living documents that require maintenance.
```

---

:::{figure} ../images/ch11-prompt-template-anatomy.png
:alt: A labeled diagram showing the four components of a prompt template — System Setup, Task Structure, Variable Brackets, and Example Output — arranged as color-coded sections of a single document. Each section is annotated with explanatory callouts. The document is shown on a laptop screen with a Helm Bank logo visible in the corner.
:width: 85%
:align: center

*Anatomy of a reusable prompt template. The bracket notation [LIKE THIS] marks the variables you customize for each use.*
:::

---

## Copilot Pages: The Collaboration Surface

Everything we've covered so far happens in your head and your Copilot conversation thread. Copilot Pages brings that work into a *shared space* where teams can collaborate, iterate, and build on each other's AI-assisted work.

### What Is a Copilot Page?

Copilot Pages is a feature in Microsoft 365 Copilot that lets you take Copilot-generated content and move it into an editable, shareable canvas — think of it as a living document that sits between a Word file and a shared conversation thread.

Key capabilities:
- **Push content from Copilot into a Page** with a single click
- **Edit directly** in the Page, or continue prompting to refine it
- **Share with colleagues** who can view, comment, or add their own Copilot-generated content
- **Reference back** in future Copilot conversations
- **Export** to Word, Teams, or Outlook when the document is ready

### Pages in the Helm Bank Workflow

Think about the workflows where multiple people need to contribute to a single document:

**Credit Committee Prep:** The RM drafts the relationship summary. The lending analyst adds the financial analysis. The BSA team contributes the compliance section. Traditionally, this is three email chains and two rounds of version confusion. With Copilot Pages, each contributor works in the same canvas, with Copilot generating and refining their section in real time.

**Client Proposal Development:** The product team generates a services overview. The RM personalizes it for the client. The compliance team checks the regulatory disclosures. One page. Three contributors. No version control nightmare.

**Weekly Wire Operations Review:** The ops team generates a Copilot summary of the week's transaction patterns. The risk team adds its commentary. The team lead reviews and edits. The final document is ready for leadership without a single forwarded email.

### How to Use Copilot Pages Effectively

**Step 1: Generate in Chat, then push to Pages**
Do your initial Copilot work in the chat interface. When you have a solid draft, click the "Add to Page" button to move it to a Page.

**Step 2: Continue refining in the Page**
Once content is in a Page, you can prompt directly within it: highlight text and prompt *"Make this section more concise"* or *"Add a risk assessment paragraph here."*

**Step 3: Share and collaborate**
Share the Page with colleagues via the standard Microsoft 365 sharing permissions. They can edit, comment, and prompt within their own sections.

**Step 4: Maintain a single source of truth**
Resist the temptation to copy content out of Pages and into separate email threads. Keep the canonical version in the Page and link to it.

**Step 5: Archive or export when complete**
When the document is final, export to Word for formal records or send directly from the Page as a Teams message or email attachment.

```{admonition} Helm Bank Application
:class: note

**Copilot Pages for Cross-Border Deal Structuring:**

When Helm Bank's team is working on a cross-border financing deal — say, a construction project with funding sources in both Miami and Bogotá — the coordination burden is significant. Different team members are in different time zones, speaking different languages, working with different pieces of information.

Copilot Pages creates a single deal room canvas. The Miami RM generates the client relationship summary in English. The Bogotá correspondent adds the local regulatory context in Spanish. Copilot translates and integrates. The credit analyst builds the financial model summary. The compliance team signs off on the EDD section.

What previously required four meetings, six email threads, and one very tired compliance officer now happens in a shared canvas over 48 hours.
```

### Pages vs. Traditional Documents

:::::{tab-set}
::::{tab-item} Traditional Document Workflow
1. One person drafts in Word
2. Email to colleagues for review
3. Each person downloads, edits, sends back
4. Coordinator merges conflicting edits
5. Another round of review
6. Final version created (maybe)
7. Someone sends "final_FINAL_v3.docx"

**Time:** 3–5 days for complex documents
**Version control:** Chaotic
**AI assistance:** None embedded in the process
::::

::::{tab-item} Copilot Pages Workflow
1. First contributor generates draft with Copilot in Pages
2. Page shared with collaborators in one click
3. Each person refines their section with Copilot assistance
4. Real-time visibility into changes
5. Final document lives in one place
6. Export when ready

**Time:** 24–48 hours for complex documents
**Version control:** Automatic
**AI assistance:** Embedded throughout the entire workflow
::::
:::::

---

## Building Your Personal Prompt Library

Everything in this chapter — system prompts, refinement techniques, conversation designs, templates — is most valuable when it lives somewhere you can access it consistently. That somewhere is your **personal prompt library**.

Think of your prompt library as your professional intellectual property. The prompts you develop and refine over months of real work are insights about *your job, your clients, your workflows, and your Copilot usage patterns*. They're worth capturing, organizing, and protecting.

### What Goes in Your Prompt Library

**Tier 1: Workhorses (use multiple times per week)**
- Your go-to system prompts for your role
- Client communication templates
- Meeting prep structures
- Any prompt you've used more than five times

**Tier 2: Specialists (use for specific, important occasions)**
- Credit memo templates
- Compliance narrative prompts
- Sensitive conversation prep prompts
- Board or executive presentation prompts

**Tier 3: Experiments (prompts you're still testing)**
- New techniques you're trying
- Prompts borrowed from colleagues
- Prompts you found in training and are adapting for your actual work

### Where to Store Your Prompt Library

| Option | Best For | Pros | Cons |
|--------|----------|------|------|
| **OneNote** | Individual use | Easy access, synced across devices | Not easily shared |
| **SharePoint List** | Team sharing | Structured, searchable, permissioned | Requires setup |
| **Teams Wiki** | Department use | Accessible, conversation-linked | Less structured |
| **Word/Excel file** | Template management | Familiar format | Version control challenges |
| **Copilot Pages** | Living library | AI-assisted updates, integrated | Newer feature, still evolving |

For most Helm Bank professionals: a **OneNote personal library** for your individual prompts, and a **SharePoint List or Teams channel** for shared team templates.

### Organizing Your Prompt Library

Use a consistent structure for each entry:

```
PROMPT NAME: [Short, searchable name]
CATEGORY: [Communication / Analysis / Compliance / Operations / Other]
LAST UPDATED: [Date]
USE CASE: [One sentence describing when to use this]
SYSTEM PROMPT: [If applicable]
TEMPLATE: [The actual prompt with [VARIABLES] marked]
NOTES: [What works well, what to watch out for]
EXAMPLE OUTPUT: [A sample of what a good result looks like]
```

This structure seems like more work upfront than just saving a text snippet. It is. But when you're in a high-pressure situation — client call in twenty minutes, compliance review tomorrow — you want to find the right prompt instantly and know exactly how to use it. The structure makes that possible.

### Prompt Library Maintenance

A prompt library that isn't maintained becomes a prompt graveyard. Schedule a fifteen-minute monthly review:

1. **Archive** prompts you haven't used in three months
2. **Update** prompts that have drifted from current workflows
3. **Elevate** experimental prompts that have proven reliable
4. **Add** new prompts from the past month's best sessions
5. **Share** one new template with your team

That's fifteen minutes a month to maintain your professional edge. Worth every minute.

```{admonition} Helm Bank Application
:class: note

**The Helm Bank Prompt Champion Program:**

Several Helm Bank departments have designated a "Prompt Champion" — a team member who maintains the shared prompt library, runs monthly prompt review sessions, and onboards new colleagues to the library. This isn't a full-time role; it's typically 2–3 hours per month.

Prompt Champions report two unexpected benefits: first, the act of documenting prompts forces clarity about what the team actually does and how they do it. Second, the library becomes a de facto knowledge base — new team members who learn from the prompt library understand the department's workflows faster than those who learn by shadowing alone.
```

---

:::{figure} ../images/ch11-prompt-library-screenshot.png
:alt: A screenshot mockup of a OneNote page titled "Helm Bank Prompt Library" showing three prompt templates organized in a structured format, with sections for Prompt Name, Category, Last Updated, Use Case, Template text with variable brackets highlighted in yellow, and Notes. The OneNote interface shows the library organized under sections for Workhorses, Specialists, and Experiments. The color scheme is professional with Helm Bank navy accents.
:width: 90%
:align: center

*A well-organized prompt library in OneNote. Variable brackets are highlighted, entries are categorized, and the format is consistent across all templates — so you can find what you need in seconds, not minutes.*
:::

---

## Hands-On Exercises

### Exercise 1: Build Your System Prompt

**Time:** 15 minutes
**Objective:** Create a personalized system prompt for your specific role at Helm Bank

**Instructions:**

1. Choose one of your core job responsibilities — the thing you do most often or find most challenging to write about.
2. Using the four-part system prompt anatomy (Identity + Situation + Constraints + Invitation), draft a system prompt for that responsibility.
3. Open a new Copilot conversation and paste your system prompt as the first message.
4. Test it with a real current work situation. Describe briefly what you're working on and let Copilot engage.
5. Evaluate the response: Is it more contextually useful than what you'd get without the system prompt? What would you change?

**Refinement Challenge:** Share your system prompt with a colleague doing a similar role. Ask them to test it in their context. Their feedback will improve it faster than solo testing ever could.

**Debrief Questions:**
- What surprised you about how Copilot responded once you set the context?
- Which constraint turned out to matter most?
- What important element did you initially leave out?

---

### Exercise 2: The Five-Turn Conversation Design

**Time:** 25 minutes
**Objective:** Design and execute a complete five-turn multi-turn conversation for a real work product

**Instructions:**

1. Choose a work product you need to create in the next week — a client email, a report section, a meeting agenda, a compliance note, or anything real and consequential.
2. Before opening Copilot, plan your five turns on paper using the three-act structure:
   - **Turn 1 (Act 1):** System prompt + initial context — establish the frame
   - **Turn 2 (Act 2):** Core generation request — ask for the first real output
   - **Turn 3 (Act 2):** Apply a refinement move — zoom in, challenge, or sharpen
   - **Turn 4 (Act 2):** Extend or redirect — push the quality further
   - **Turn 5 (Act 3):** Package — format for delivery to its intended recipient
3. Execute the planned conversation in Copilot.
4. Note where the conversation diverged from your plan and why.

**Reflection Questions:**
- Which turn produced the biggest leap in quality?
- Where did Copilot surprise you — positively or negatively?
- How long did the conversation take vs. how long the work product would have taken without Copilot?

**Bonus:** Repeat the exercise with a colleague. Observe each other's conversation designs and share one observation about what each person did that the other could adopt.

---

### Exercise 3: Build Your Prompt Library Starter Pack

**Time:** 30 minutes
**Objective:** Leave this session with a personal prompt library containing at least three production-ready entries

**Instructions:**

1. Identify the three situations at work where you most frequently need to write something from scratch — situations where you often stare at a blank page or rewrite the same email for the fifteenth time.

2. For each situation, draft a prompt template using the four-part anatomy:
   - Template Name (short, descriptive)
   - System Setup (role and context framing)
   - Task Structure with [VARIABLE BRACKETS]
   - Notes on what a good output looks like

3. Test each template with a real scenario from the past week. Refine based on the output quality.

4. Create a OneNote page titled "My Prompt Library — [Your Name]" and add your three templates using the structured format from this chapter.

5. Share your best template with the group. By the end of the exercise, the room collectively has built a team library of N templates — one per participant — in thirty minutes of parallel work.

**Team Challenge:** After sharing, each person adopts one template from a colleague and tests it. Report back: did someone else's template work for your context? What did you modify?

---

## Putting It All Together: The Prompt Architect Mindset

You've now covered six advanced techniques. The question isn't whether each one is useful in isolation — it's whether you'll use them together, consistently, as a set of professional habits.

The Prompt Architect doesn't just know how to prompt. They think about prompting *before* they open Copilot. They ask:

- **What role should Copilot play in this conversation?** → System prompt
- **What's the quality level I need, and how many passes will it take?** → Iterative refinement plan
- **What's the sequence of outputs I need, and in what order?** → Multi-turn design
- **Do I already have a template for this?** → Prompt library check
- **Will this output need to be shared and refined by others?** → Copilot Pages

That thirty-second mental check, practiced habitually, is what separates someone who *uses* Copilot from someone who *deploys* it strategically.

At Helm Bank, where the complexity of transactions, the sensitivity of relationships, and the rigor of compliance demands are all higher than average, that strategic mindset isn't a nice-to-have. It's a competitive differentiator.

Valeria, our Relationship Manager from the opening story, didn't stumble onto her Monday morning success. She had built a prompt library over three months, maintained a set of system prompts for her most common scenarios, and practiced multi-turn conversation design until it felt natural. When Don Alberto sent his message at 7:52 AM, she had the tools ready and the instincts to deploy them.

You now have the tools too. The next step is practice.

---

## Chapter Summary

:::::{tab-set}
::::{tab-item} Key Concepts
**System Prompts**
The opening frame that sets Copilot's role, context, and constraints for the entire conversation. Invest 60 seconds upfront; save 20 minutes of cleanup later. Include Identity, Situation, Constraints, and an Invitation to begin.

**Iterative Refinement**
The first response is a draft, not a deliverable. Use the eight refinement moves — Zoom In, Zoom Out, Reframe, Redirect, Sharpen, Challenge, Extend, Format Shift — to drive toward quality outputs across multiple turns.

**Multi-Turn Conversation Design**
Plan Copilot conversations before you start them. Use the three-act structure: Establish and Explore → Build and Refine → Package and Deliver. One objective per turn. Signal transitions explicitly.

**Prompt Templates**
Reusable prompt structures with [VARIABLE] brackets for customization. Build templates for your most frequent workflows. Version them, maintain them, and share the best ones with your team.

**Copilot Pages**
A collaborative canvas for AI-assisted documents. Best for multi-contributor workflows where version control chaos is the enemy. Generates, edits, and shares from a single living surface.

**Personal Prompt Library**
Your professional intellectual property. Organized in three tiers — Workhorses, Specialists, Experiments — stored in OneNote or SharePoint, and reviewed monthly to stay current.
::::

::::{tab-item} The Helm Bank Edge
Advanced prompting skills translate directly into business value at Helm Bank:

- **Faster client responsiveness** — system prompts and templates mean less time staring at a blank screen when Don Alberto calls at 7:52 AM
- **Higher quality compliance documentation** — multi-turn design catches gaps before they reach BSA review, not during it
- **Stronger credit presentations** — iterative refinement produces polished credit memos that anticipate committee questions
- **Better cross-border coordination** — Copilot Pages eliminates version-control chaos on multi-contributor deal documents
- **Institutional knowledge capture** — prompt libraries preserve best practices that currently live only in senior bankers' heads, protecting the bank when those bankers move on

These aren't peripheral productivity hacks. They're central to how Helm Bank competes in the US–Latin America corridor.
::::

::::{tab-item} Skills Checklist
Before the next session, confirm you can:

- [ ] Write a system prompt from scratch for at least two common scenarios in your role
- [ ] Name all eight iterative refinement moves and use at least five in a single session
- [ ] Design a five-turn conversation structure on paper before starting it in Copilot
- [ ] Create a prompt template using the four-part anatomy with [VARIABLE BRACKETS]
- [ ] Explain clearly when Copilot Pages adds value over a shared Word document
- [ ] Locate your personal prompt library and find a specific template within 30 seconds
- [ ] Name the three tiers of prompt library organization (Workhorses, Specialists, Experiments)
::::
:::::

---

## Your Homework

Before the next session (Chapter 12: Copilot for Data and Analytics), complete the following:

**Assignment 1: System Prompt Sprint**
Create system prompts for three different scenarios you'll face in the next two weeks. Use them in real Copilot sessions and take brief notes on what works and what needs adjustment. Bring your before/after observations to the next session — we'll use them as case studies.

**Assignment 2: Library Seeding**
Add five entries to your personal prompt library using the structured format from this chapter. At least one should be a prompt you developed this week from a real work need — not a theoretical exercise, but something that produced an output you actually used.

**Assignment 3: Conversation Design Practice**
Before opening Copilot for a complex task this week, spend five minutes designing the conversation on paper first. Map out your turns using the three-act structure. Execute the conversation, then write two sentences: how did the pre-planned structure help, and where did you have to adapt on the fly?

**Optional Challenge: Pages Pilot**
If your team currently has a document being built via email chain, propose moving it to a Copilot Page for one week. At the end of the week, assess: what worked, what friction you encountered, and whether you'd do it again. Bring your findings to share.

---

```{admonition} Looking Ahead: Chapter 12
:class: tip
**Chapter 12: Copilot for Data and Analytics** — Next session, we explore how Helm Bank professionals can use Copilot to analyze financial data, generate insights from transaction reports, interpret complex regulatory datasets, and build presentation-ready summaries — no data science background required. We'll work with Excel, Power BI, and Copilot Studio to turn raw numbers into decisions that move deals forward.
```

---

*Chapter 11 of "The Essence of AI: A Microsoft Copilot Master Class for Helm Bank" — Week 4, Session A.*

*Helm Bank values: Empathy · Curiosity · Creativity · Passion*

*© Helm Bank USA. All rights reserved. For internal training use only.*
