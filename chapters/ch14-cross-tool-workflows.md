---
title: "Chapter 14: Week 5, Session A — Cross-Tool AI Workflows"
subtitle: "The Connected Intelligence Layer"
short_title: "Cross-Tool AI Workflows"
description: "How Microsoft Copilot connects across Word, Excel, PowerPoint, Teams, and OneNote to create end-to-end AI-assisted workflows — from deal origination to board presentation, built for Helm Bank professionals."
label: ch-14-cross-tool-workflows
tags: [cross-tool workflows, Microsoft 365, Copilot, workflow design, Microsoft Graph, deal origination, ALCO, client onboarding, Helm Bank, banking automation]
---

```{admonition} Download this Chapter as PDF
:class: tip
[Download PDF](https://github.com/liquid-books/ai-copilot-helmbank/raw/main/pdfs/ch14-cross-tool-workflows.pdf)
```

---

## Opening: Tuesday Morning, Brickell Avenue

It is 7:52 AM. Mariela, a senior relationship manager at Helm Bank's Miami headquarters, is finishing her café cubano before an 8:00 AM client call. Her client — a Colombian exporter looking to establish a $4.2 million revolving credit facility — has moved up the meeting by two days. The credit memo that was supposed to take a week to build is now needed by Thursday.

Four years ago, this would have triggered a minor panic. Today, Mariela opens Teams, fires up Copilot, and types: "Summarize everything we have on Grupo Exportador del Valle — emails, meetings, shared files — and flag any open credit questions."

By 8:00 AM she has a three-paragraph brief ready. During the call, she drops into OneNote and asks Copilot to capture action items in real time. By 9:30 AM, those notes are in a structured Word memo draft. By noon, her analyst Carlos has an Excel credit model pre-populated with the financial figures they discussed. By Wednesday afternoon, a PowerPoint deck for the Credit Committee is half-built, pulling from the Word memo and Excel model.

The deal closes in eleven days. A record for this type of facility.

This is not magic. It is not science fiction. It is what happens when you understand — really understand — how Copilot operates *across* Microsoft 365, not just *within* each tool.

That is what this chapter is about.

---

## The Problem With Siloed Thinking

Most professionals use Microsoft 365 the way people used to use physical filing cabinets: each drawer is a different tool, each folder is a different project, and you spend half your time walking between cabinets looking for the thing you need.

Word for writing. Excel for numbers. PowerPoint for presenting. Teams for talking. OneNote for notes. These are five separate tools, and for years, that is how people treated them — as five separate islands.

The result? Information gets trapped. A key data point from a Teams call never makes it into the credit memo. The Excel model assumptions differ slightly from what the Word memo says. The PowerPoint deck uses numbers from last week's model, not this week's. Someone has to manually reconcile everything, and that someone is always the person who can least afford the time.

Copilot breaks down these walls. But only if you know how to let it.

The secret is Microsoft Graph — and understanding it changes how you think about every tool in your kit.

---

## What Is Microsoft Graph? The Connective Tissue

Think of Microsoft Graph as the nervous system of Microsoft 365. It is an API layer that connects everything: your emails, calendar events, Teams messages, SharePoint documents, OneDrive files, OneNote notebooks, and meeting recordings. Every time you interact with any Microsoft 365 service, Graph is keeping track.

When Copilot answers a question in Word, it does not just look at the document you have open. It can reach into Graph and pull context from:

- A Teams meeting you attended yesterday about this client
- An email thread with the client's CFO from last month
- A OneNote page your colleague added three days ago
- An Excel file shared in a Teams channel two weeks back
- A previous Word memo on a related deal

This is what Microsoft calls "grounded" AI — Copilot's responses are grounded in *your actual organizational data*, not just its training data. It is the difference between a smart stranger and a smart colleague who has been with you for years.

```{figure} figures/ch14-graph-architecture.png
:name: fig-graph-architecture
:alt: Diagram showing Microsoft Graph at the center connecting Teams, OneNote, Word, Excel, PowerPoint, SharePoint, and Outlook. Arrows flow bidirectionally between each tool and Graph. Copilot sits atop Graph, drawing from all connected services simultaneously.

**Figure 14.1 — Microsoft Graph as the Connective Layer.** Copilot accesses all Microsoft 365 data through the Graph API, enabling it to pull context from any connected service when helping you work in any individual tool.
```

### What Graph Knows About Your Work

When Copilot is properly configured and you have the right licenses, Graph tracks:

| Data Type | Examples Available to Copilot |
|-----------|-------------------------------|
| **People** | Who you work with most, who worked on similar deals |
| **Files** | Documents shared with you, recent edits, version history |
| **Meetings** | Transcripts, recordings, action items (if enabled) |
| **Emails** | Threads relevant to a project, client communications |
| **Chats** | Teams messages about a topic or with a person |
| **Calendar** | Meeting history, upcoming commitments |
| **Pages** | OneNote content shared in your organization |

```{admonition} Helm Bank Application
:class: note
At Helm Bank, Graph connectivity means Copilot can answer questions like "What did we discuss with this client in the last 90 days?" by pulling from Teams call transcripts, email threads in Outlook, and OneNote meeting notes simultaneously — without you having to search each place manually. This is particularly powerful for the Latin America corridor, where deals often involve months of relationship-building before formal credit discussions begin.
```

### The Privacy Architecture — What Copilot Cannot See

Graph respects your organization's permission model. Copilot will only surface content you already have access to. If a credit analyst does not have access to the CEO's email inbox, Copilot will not show them information from it — even if that information is technically in Graph. This is not a workaround; it is the design. Microsoft calls this "permission-aware retrieval."

This means: if your Helm Bank tenant is properly configured with role-based access controls, Copilot is not a security liability. It is a security-aware assistant.

---

## The Five-Tool Orchestra

Before we map specific workflows, let us establish what each tool does best, and what Copilot brings to it.

:::::{tab-set}
::::{tab-item} Teams
**Primary Role:** Communication and collaboration hub

**What Copilot adds:**
- Real-time meeting summaries and action items
- Post-meeting recap generation
- Thread summarization ("What did we decide in this channel?")
- Draft replies to complex message threads
- Cross-meeting insight synthesis

**Best for:** Capturing the *event* — who said what, what was decided, what needs to happen next
::::

::::{tab-item} OneNote
**Primary Role:** Structured note-taking and knowledge capture

**What Copilot adds:**
- Reformat raw notes into structured outlines
- Summarize across multiple notebook pages
- Generate follow-up action lists from meeting notes
- Fill gaps in notes from Teams transcripts
- Create templates from scratch

**Best for:** Organizing the *knowledge* — turning raw capture into structured, searchable information
::::

::::{tab-item} Word
**Primary Role:** Document creation and formal writing

**What Copilot adds:**
- Draft memos, reports, and analysis from notes/data
- Rewrite for tone (formal, executive, regulatory)
- Summarize long documents
- Generate from a prompt grounded in other files
- Review and edit for clarity and completeness

**Best for:** Producing the *artifact* — the formal document that represents work product
::::

::::{tab-item} Excel
**Primary Role:** Quantitative analysis and financial modeling

**What Copilot adds:**
- Explain what a formula or model does
- Suggest formulas based on natural language
- Generate charts and visualizations
- Identify patterns and anomalies in data
- Create structured tables from unstructured inputs

**Best for:** Building the *model* — turning data into analysis
::::

::::{tab-item} PowerPoint
**Primary Role:** Visual communication and presentations

**What Copilot adds:**
- Generate full decks from a Word document or prompt
- Suggest slide layouts and speaker notes
- Summarize long decks into executive overviews
- Rewrite slide text for different audiences
- Pull content from referenced files

**Best for:** Communicating the *story* — turning analysis into persuasive narrative
::::
:::::

The key insight: these tools form a natural progression from *event* to *knowledge* to *artifact* to *model* to *story*. A well-designed workflow moves information through this progression, with Copilot accelerating each handoff.

---

## The Master Workflow: Anatomy of a Helm Bank Deal

Let us build the complete workflow from the ground up. We will use the deal origination pipeline as our primary example, because it touches every tool and represents the most complex, high-stakes work Helm Bank professionals do.

```{figure} figures/ch14-master-workflow.png
:name: fig-master-workflow
:alt: Linear workflow diagram showing five stages flowing left to right: Stage 1 Teams Meeting with a Copilot icon showing "Record, Transcribe, Summarize"; Stage 2 OneNote with "Organize, Structure, Tag"; Stage 3 Word with "Draft, Refine, Finalize"; Stage 4 Excel with "Model, Analyze, Validate"; Stage 5 PowerPoint with "Design, Narrate, Present". Below each stage, a Microsoft Graph icon shows data flowing down into a shared repository, with a horizontal arrow labeled "Copilot accesses all previous stages at any point."

**Figure 14.2 — The Helm Bank Deal Origination Workflow.** Each stage produces structured output that feeds the next. Microsoft Graph makes all previous stages accessible to Copilot at any subsequent stage — meaning your PowerPoint deck can reference what was said in the original Teams meeting three weeks ago.
```

### Stage 1 — Teams: The Intelligence Capture

Everything begins with a conversation. Whether it is an initial client call, an internal credit discussion, or a site visit debrief, the Teams meeting is where deal intelligence first enters the system.

**Before the meeting:**
- Ask Copilot to prepare a brief from previous interactions: "What do we know about this client from our last six months of communications?"
- Pull the agenda from OneNote if one exists and have Copilot suggest talking points

**During the meeting:**
- Enable Copilot real-time features (requires meeting transcript)
- Ask Copilot mid-meeting: "What questions have we not covered yet based on our agenda?"
- Use Copilot to track commitments as they are made

**After the meeting:**
- Ask Copilot to generate a meeting summary: "Summarize this meeting, listing decisions made, action items by person, and open questions."
- Ask for a "deal signal" summary: "Based on this call, what are the key credit risks and client motivations we should document?"

```{admonition} Helm Bank Application
:class: note
**Latin America Corridor Tip:** When working with Spanish-language participants, Copilot can summarize bilingual meetings and produce summaries in either language. This is valuable for meetings with clients from Colombia, Peru, or Venezuela where participants may mix languages. Ask: "Summarize this meeting in English, noting any points where participants switched to Spanish and what was discussed." This is a practical daily-use capability for Helm Bank's international team.
```

**Typical output from Stage 1:**
- A structured meeting summary saved or exported to OneNote
- A list of action items with owners
- A "deal signal" brief with credit considerations flagged
- Verbatim quotes from the client captured for the relationship history

### Stage 2 — OneNote: The Knowledge Architecture

Raw meeting summaries are a starting point, not a destination. OneNote is where raw intelligence gets organized into something usable.

Helm Bank uses a standard OneNote notebook structure for active deals:

```
Deal Room — [Client Name]
  Client Overview
  Meeting Log
    YYYY-MM-DD: Initial Exploratory Call
    YYYY-MM-DD: Financial Due Diligence Call
    YYYY-MM-DD: Site Visit Debrief
  Credit Considerations
  Compliance and KYC Notes
  Open Questions Tracker
  Document Checklist
```

**Copilot tasks in OneNote:**

After pasting or importing the Teams summary, ask Copilot to:
- "Reformat this meeting summary into the Helm Bank meeting log template."
- "Extract all open questions from this meeting summary and add them to the Open Questions Tracker section."
- "What are the credit considerations mentioned across all our meeting notes for this client? Summarize them."
- "We are preparing the credit memo. What client information are we still missing based on our notes?"

That last prompt is especially powerful. Copilot reads across all your OneNote sections for this deal and identifies gaps — before you spend three hours drafting a memo only to realize you do not have the client's audited financials from 2023.

```{admonition} Helm Bank Application
:class: note
**Compliance Integration:** Copilot in OneNote can also help with BSA/AML documentation. Ask: "Based on our KYC notes, list all the beneficial ownership questions we have not yet confirmed answers to." This creates a ready-made checklist for your compliance review before the credit memo goes to underwriting. At Helm Bank, where the Latin America corridor demands rigorous OFAC and FinCEN compliance, this saves significant time and reduces the risk of missing a documentation requirement.
```

### Stage 3 — Word: The Formal Artifact

Now the real writing begins. The Word credit memo is the formal work product — the document that will be reviewed, approved, filed, and potentially shown to examiners. It must be accurate, complete, and professionally written.

This is where Copilot earns its salary.

**Starting from scratch with Copilot:**

Rather than staring at a blank page, open a new Word document and use Copilot's draft-from-reference capability:

"Draft a credit memo introduction for a $4.2M revolving credit facility request from Grupo Exportador del Valle, a Colombian agricultural exporter. Use the meeting notes from the OneNote Deal Room notebook and any related emails from the last 90 days. Follow Helm Bank's standard credit memo structure."

Copilot will pull from your OneNote notes and email history via Graph and produce a working first draft. It will not be perfect — it never is — but it will be 70% of the way there, and you will be editing rather than starting from zero.

**Section-by-section Copilot prompts for a credit memo:**

| Section | Copilot Prompt |
|---------|----------------|
| Executive Summary | "Write a 3-paragraph executive summary for this credit request, suitable for a credit committee that has 60 seconds to read it." |
| Borrower Overview | "Describe the borrower's business model, ownership structure, and key markets based on our OneNote client notes." |
| Financial Analysis | "Summarize the key financial ratios from the attached Excel model. Flag any ratios outside our policy limits." |
| Risk Assessment | "List the primary credit risks identified in our due diligence meetings. Suggest a risk mitigation for each." |
| Recommendation | "Write a credit recommendation paragraph, stating the proposed terms and conditions, based on the analysis above." |

**Refinement prompts:**
- "This section sounds too casual for a regulatory document. Rewrite it in formal banking language."
- "Make this paragraph more concise. Target 75 words maximum."
- "Add a sensitivity analysis discussion referencing the scenario tables in our Excel model."

```{admonition} Helm Bank Application
:class: note
**Examiner-Ready Language:** Copilot can be explicitly prompted to write in language that anticipates regulatory review. Try: "Rewrite this risk section using language consistent with OCC examination guidelines for credit risk. Make sure we are addressing repayment capacity, collateral adequacy, and guarantor strength explicitly." This reduces the back-and-forth with examiners and demonstrates that Helm Bank's credit culture is well-documented and defensible.
```

### Stage 4 — Excel: The Quantitative Foundation

The credit memo says "strong repayment capacity." The Excel model proves it.

Excel is where the financial due diligence lives — spreading historical financials, projecting forward scenarios, calculating coverage ratios, running sensitivity analyses. Copilot in Excel will not do the banker's analytical thinking for you, but it dramatically accelerates the mechanical work.

**Copilot tasks in Excel for credit analysis:**

*Populating the model:*
- "I have three years of income statement data in columns B through D. Create a summary table showing year-over-year growth rates for revenue, EBITDA, and net income."
- "Calculate DSCR using the annual debt service in row 15 and EBITDA in row 8. Show me the formula."

*Building scenarios:*
- "Create a sensitivity table showing DSCR outcomes if revenue drops 10%, 20%, or 30% from base case, and if interest rates rise 100bps or 200bps from current."

*Identifying anomalies:*
- "Flag any rows in this financial data where the year-over-year change exceeds 25% in either direction."
- "This client's gross margin dropped from 34% to 21% in 2024. What are the most common explanations for this kind of margin compression in an agricultural export business?"

*Communicating findings:*
- "Create a chart showing the last three years of revenue and EBITDA with a trendline."
- "Write a text summary of three sentences describing what this credit model shows about the borrower's repayment capacity."

That last prompt generates text you can paste directly into your Word memo — another cross-tool handoff, facilitated by Copilot.

```{admonition} Helm Bank Application
:class: note
**ALCO Prep in Excel:** The Asset/Liability Committee packet is one of the most time-intensive recurring deliverables at Helm Bank. Copilot can significantly reduce the preparation time. Once your base data is loaded, ask: "Summarize the key trends in our rate sensitivity table for the past three months and flag any positions that have moved outside our policy limits." Then ask: "Draft a one-paragraph narrative for the ALCO chairman summarizing the interest rate risk position this month." This narrative can go directly into the ALCO presentation deck.
```

### Stage 5 — PowerPoint: The Story

The credit committee is busy. The ALCO members are executives. The board directors are not reading 47-page credit memos in the meeting — they are reviewing a deck.

This is PowerPoint's job, and Copilot is remarkably good at building decks from existing content.

**The "generate from document" workflow:**

Open PowerPoint, click Copilot, and try:

"Create a presentation from the Grupo Exportador del Valle credit memo. The audience is the Helm Bank Credit Committee. Target 10-12 slides. Include an executive summary slide, a borrower overview slide, a financial highlights slide with our key ratios, a risk and mitigants slide, and a recommendation slide."

Copilot will generate a working deck in under a minute. It pulls from the Word document content and structures it into slides with appropriate headers and speaker notes.

**Refinement workflow:**

After generating, go through each slide and ask:
- "This slide has too much text. Summarize it to 4 bullet points maximum."
- "Add speaker notes to this slide that explain the DSCR calculation methodology."
- "The risk slide needs a second column showing our proposed mitigants for each risk. Add that."

**Adapting for different audiences:**

The credit committee deck and the board summary deck are different documents. From the same source material:

"Create a 5-slide executive summary version of this presentation for the Helm Bank Board of Directors. Use plain language. Remove the technical ratio calculations and focus on the strategic rationale and risk posture."

---

## Mapping Helm Bank's Four Critical Workflows

Beyond the deal origination pipeline, Helm Bank has several recurring workflows where cross-tool Copilot integration delivers significant value. Let us map each one.

```{figure} figures/ch14-four-workflows.png
:name: fig-four-workflows
:alt: A 2x2 grid showing four workflow boxes. Top left: Deal Origination Pipeline (Teams to OneNote to Word to Excel to PowerPoint). Top right: ALCO Preparation (Excel to Word to PowerPoint to Teams). Bottom left: Client Onboarding (Teams to Word to OneNote to Excel). Bottom right: Examiner Response Package (Word to Excel to PowerPoint to Teams). Each box shows the tool sequence with arrows and Copilot icons at each stage.

**Figure 14.3 — Helm Bank's Four Core Cross-Tool Workflows.** Each workflow moves through different tools in a different sequence, but all use Microsoft Graph as the connective layer and Copilot as the acceleration engine at each stage.
```

### Workflow A: Deal Origination Pipeline

*Already detailed above. Summary:*

**Route:** Teams to OneNote to Word to Excel to PowerPoint

**Total time savings (estimated):** 40-60% reduction in document preparation time

**Critical handoff points:**

1. Teams summary to OneNote: Must be structured immediately after the meeting (within 2 hours) while context is fresh
2. OneNote to Word: Copilot should reference the full OneNote notebook, not just the most recent page
3. Word to Excel: The memo's financial assumptions must match the model — Copilot can cross-check if you ask it to
4. Excel to PowerPoint: Charts and tables should be linked, not copied as static images

---

### Workflow B: ALCO Preparation

The Asset/Liability Committee meets monthly. The preparation packet includes interest rate risk analysis, liquidity reports, investment portfolio summaries, and policy exception tracking. It typically takes three to five days to assemble.

**Route:** Excel (data) to Word (narratives) to PowerPoint (board deck) to Teams (final review call)

**Stage 1 — Excel: Data Assembly and Analysis**

The ALCO team maintains a master Excel workbook with rate sensitivity data, gap analysis, and liquidity metrics. Copilot assists with:

- "Compare this month's NII sensitivity table to last month's. What changed materially?"
- "We have three new interest rate scenarios (up 100, up 200, down 50 bps). Calculate the projected NII impact for each based on our current repricing schedule."
- "Flag any deposit categories where the repricing beta assumption has changed from our policy model."

**Stage 2 — Word: Executive Narratives**

Each section of the ALCO packet requires a written narrative. These used to take hours to write from scratch. With Copilot:

- "Based on the rate sensitivity table in our ALCO Excel workbook, write the interest rate risk narrative section for this month's ALCO packet. The audience is the CFO and board risk committee. Highlight any positions outside our policy limits."
- "Write the liquidity section narrative. We ended the month with an LCR of 118% against a policy minimum of 110%. Explain what drove the change from last month's 124%."

**Stage 3 — PowerPoint: The ALCO Deck**

- "Convert the ALCO packet Word document into a 15-slide board presentation. Include one slide per major risk category, plus an executive summary and key decisions required slide."

**Stage 4 — Teams: Final Review**

Before the ALCO meeting, the team holds a 30-minute prep call. Copilot can:
- Summarize the deck for latecomers
- Track questions raised during the call
- Generate a pre-meeting briefing for the Chairman

```{admonition} Helm Bank Application
:class: note
**Regulatory Timing:** Helm Bank's ALCO packet is due to the board risk committee 48 hours before the meeting. Using this workflow, the data assembly and narrative drafting that previously took three days can be compressed to one day, providing a full extra day for management review and revision before submission. This buffer is valuable when FDIC or state regulator inquiries arrive mid-month and compete for the team's attention.
```

---

### Workflow C: Client Onboarding

A new client relationship at Helm Bank — particularly for international clients in the Latin America corridor — requires significant documentation: KYC, beneficial ownership certification, account agreements, FATCA declarations, and risk ratings. The onboarding workflow spans weeks and multiple team members.

**Route:** Teams (kickoff call) to Word (documentation package) to OneNote (tracking) to Excel (risk rating model)

**Stage 1 — Teams: Kickoff and KYC Interview**

- Copilot captures the client interview in real time
- After the call: "Generate a KYC preliminary risk assessment from this meeting. Note any responses that require follow-up documentation."

**Stage 2 — Word: Documentation Package**

- "Draft the beneficial ownership disclosure letter for this client based on the information gathered in our onboarding call. Use Helm Bank's standard BSA template language."
- "Create an account opening summary memo that includes all the client information we have collected and identifies any pending documentation."

**Stage 3 — OneNote: Progress Tracking**

- Copilot maintains a running checklist of required documents
- "Update our onboarding tracker for this client. Based on the emails from this week, which documents have been received and which are still outstanding?"

**Stage 4 — Excel: Risk Rating**

- "Based on the client profile in our OneNote onboarding notebook, suggest initial inputs for our BSA risk rating model. Flag which fields require manual validation."

**Timeline impact:** A well-orchestrated onboarding workflow can reduce time-to-account from 6-8 weeks to 3-4 weeks, which matters significantly for clients who are simultaneously being courted by competitor banks.

---

### Workflow D: Examiner Response Package

When regulators arrive — whether OCC, FDIC, or Florida OFR — Helm Bank needs to respond to information requests quickly, completely, and in a format that demonstrates organizational competence. A poorly organized examiner response can turn a routine examination into an extended supervisory event.

**Route:** Word (response letters) to Excel (data schedules) to PowerPoint (management presentations) to Teams (coordination)

**Stage 1 — Word: Response Letters**

Examiners issue Document Request Lists (DRLs). For each item:

- "Draft a response to this DRL item requesting our credit underwriting policies. Reference our current policy manual and note the last review date."
- "This DRL asks for all loan modifications since January 2024. Write a cover letter explaining our modification framework and attaching the schedule."

**Stage 2 — Excel: Data Schedules**

- "The examiner has requested a listing of all loans over $500K with their risk ratings as of March 31. Format this data schedule in a way that is clean and self-explanatory for someone outside the bank."
- "Add a column to this loan schedule explaining the basis for each risk rating in plain language."

**Stage 3 — PowerPoint: Management Presentations**

Examiners typically request a management overview presentation on the first day:

- "Create an 8-slide management overview presentation for our OCC examination. Cover: bank overview, strategic plan summary, financial performance highlights, credit portfolio summary, liquidity position, capital adequacy, and key risks and mitigants."

**Stage 4 — Teams: Internal Coordination**

During an examination, teams are fielding questions in real time:

- "What documents have we provided to the examiners so far this week? Summarize from our Teams examination channel."
- "Draft a response to the examiner's verbal question about our CECL methodology. Pull from our OneNote policy documentation."

```{admonition} Helm Bank Application
:class: note
**Examination Pro Tip:** Create a dedicated Teams channel called "Exam War Room" at the start of every examination. All examiner requests and bank responses go there. Copilot can then serve as your institutional memory during the exam: "What did we tell the examiners about our concentration limits? Check the War Room channel." This prevents the embarrassing situation where different team members give inconsistent answers to the same question asked multiple days apart.
```

---

## Designing Your Own Cross-Tool Workflows

Understanding Helm Bank's four core workflows is useful. Knowing how to design your own is transformative.

### The Workflow Design Framework

Good cross-tool workflows share five characteristics:

**1. Clear trigger event** — What starts the workflow? A meeting, a regulatory notice, a client inquiry, a recurring date.

**2. Defined outputs at each stage** — What does each tool produce? Summary, memo, model, deck, decision.

**3. Explicit handoff prompts** — What Copilot prompt moves content from one tool to the next?

**4. Named owners** — Who is responsible at each stage?

**5. Quality checkpoints** — Where does a human review before moving forward?

### Designing a New Workflow: Step by Step

Use this template when designing a new cross-tool workflow:

```
WORKFLOW NAME: [Name]
TRIGGER: [What starts this workflow?]
TOOLS IN SEQUENCE: [List in order]
OUTPUTS:
  - [Tool 1] produces: [deliverable]
  - [Tool 2] produces: [deliverable]
  - [Tool 3] produces: [deliverable]
COPILOT HANDOFF PROMPTS:
  - [Tool 1] to [Tool 2]: "[Exact Copilot prompt]"
  - [Tool 2] to [Tool 3]: "[Exact Copilot prompt]"
REVIEW CHECKPOINTS:
  - After [Tool N]: [Who reviews? What criteria?]
ESTIMATED TIME SAVINGS: [vs. manual process]
```

```{admonition} Helm Bank Application
:class: note
**Team Workflow Libraries:** Helm Bank teams are encouraged to document their most effective cross-tool workflows and share them in a dedicated SharePoint "Workflow Library." When a new team member joins, they can browse the library and import proven workflow templates. Copilot can even help create these templates: "Based on my last five credit memos, what workflow pattern am I using? Document it as a reusable template."
```

### Common Workflow Anti-Patterns to Avoid

Even with Copilot, workflows can break down. Watch for these failure patterns:

:::::{tab-set}
::::{tab-item} The Information Silo
**What it looks like:** Team members keep notes in personal OneNote notebooks (not shared), send emails from personal Outlook without copying shared mailboxes, and store Excel models locally rather than in SharePoint.

**Why it fails:** Copilot's Graph access is limited to content shared with you. If your colleague's credit analysis is in a local file, Copilot cannot see it. The workflow breaks at every handoff.

**Fix:** Establish team SharePoint libraries and shared OneNote notebooks as the default storage location. Make "save to SharePoint" a habit, not an option.
::::

::::{tab-item} The Prompt Black Box
**What it looks like:** Team members use Copilot to generate content but do not document which prompts they used or what sources Copilot cited. When a manager asks "where did this number come from?", no one knows.

**Why it fails:** Copilot outputs can be wrong. If you do not know what input Copilot used, you cannot verify the output.

**Fix:** Always ask Copilot to cite its sources: "List the documents and meetings you referenced to create this summary." Save those citations in your OneNote tracker.
::::

::::{tab-item} The Serial Bottleneck
**What it looks like:** Each stage of the workflow must be 100% complete before the next person can start. The credit memo must be final before the Excel model can be built. The model must be approved before the deck is started.

**Why it fails:** This eliminates the parallelism that makes cross-tool workflows powerful.

**Fix:** Use Copilot to generate "draft-quality" outputs at each stage so parallel work can begin, with a reconciliation step built in. The analyst can start the Excel model from a draft memo while the RM is still refining the narrative.
::::

::::{tab-item} The Copilot Dependency
**What it looks like:** Team members stop reading source documents because "Copilot summarized it." They stop verifying numbers because "Copilot calculated it." They submit AI-generated memos without substantive review.

**Why it fails:** Copilot makes mistakes. In banking, a mistake in a credit memo can result in a bad loan, a regulatory citation, or reputational damage. AI is a first draft, not a final product.

**Fix:** Institute a "Copilot Sanity Check" rule: every Copilot-generated output must be reviewed against at least one primary source before it becomes a formal work product. Make this a cultural norm, not just a policy.
::::
:::::

---

## Hands-On Exercises

### Exercise 14.1 — The Deal Brief Sprint

**Time:** 20 minutes
**Tools:** Teams and Copilot, OneNote

**Scenario:** You just finished a 45-minute exploratory call with a new prospect — a Peruvian mining equipment distributor looking for a $1.8M trade finance facility. You took some rough notes during the call.

**Your task:**

1. Open Microsoft Teams and navigate to Copilot (or use a recent meeting if available)
2. If you have a meeting transcript available, ask: "Summarize this meeting in the format of a Helm Bank initial client brief. Include: client background, stated credit need, key financial metrics mentioned, questions we asked, client responses, and next steps agreed."
3. If no transcript is available, type your rough notes into a Teams Copilot chat and ask it to reformat them using the same prompt
4. Copy the output into a new OneNote page titled "Initial Client Brief — [Prospect Name]"
5. In OneNote, ask Copilot: "Based on this client brief, what additional information do we need before we can begin credit analysis? List as an action checklist with suggested owner — RM or Analyst."

**Debrief:** Compare the Copilot-generated checklist to what you would have written manually. What did it catch that you might have missed? What did it include that does not apply?

---

### Exercise 14.2 — Cross-Tool Memo Builder

**Time:** 30 minutes
**Tools:** OneNote, Word, Copilot in both

**Scenario:** You have three OneNote pages for an active deal: "Initial Client Brief," "Due Diligence Call Notes," and "Financial Document Review." You need to draft the Executive Summary section of the credit memo.

**Your task:**

1. Open the three OneNote pages in sequence
2. In each page, ask Copilot: "Extract the 5 most important facts from this page that should appear in a credit memo executive summary."
3. Open a new Word document
4. In Word Copilot, type: "I am writing the executive summary of a credit memo for [client name and deal type]. I have the following key facts gathered from due diligence: [paste the facts from OneNote]. Write a 3-paragraph executive summary in formal banking language suitable for a credit committee."
5. Review the output. Ask Copilot to make two targeted refinements — for example, make the risk statement more specific, add the proposed structure terms.
6. Save the document to your team SharePoint deal folder.

**Debrief:** How long did this take versus how long writing an executive summary from scratch typically takes you? What would you need to verify before submitting this as a work product?

---

### Exercise 14.3 — The Deck-from-Memo Challenge

**Time:** 25 minutes
**Tools:** Word, PowerPoint, Copilot in both

**Scenario:** You have a completed or near-complete Word credit memo. You need to create a 10-slide Credit Committee presentation by end of day.

**Your task:**

1. Open a complete or sample credit memo in Word
2. Ask Word Copilot: "Create a slide-by-slide outline for a 10-slide Credit Committee presentation based on this memo. For each slide, provide the title, 3-4 bullet points, and one question the Committee might ask about this slide's content."
3. Review the outline. Adjust any slides that do not fit the structure.
4. Open PowerPoint and use Copilot to generate the deck: "Create a presentation based on [the Word document]. Follow this structure: [paste the outline]."
5. Review each slide. For two slides, ask Copilot to rewrite the content — one for "more concise" and one for "more data-driven."
6. Add speaker notes to the Recommendation slide: "Write speaker notes for this slide that prepare the presenter for the three most likely questions from a credit committee."

**Debrief:** What was the quality of the auto-generated deck? What required the most human intervention? Would you be comfortable presenting this deck after 25 minutes of work?

---

## Advanced Techniques: Copilot as Workflow Orchestrator

Once you have mastered the basic five-tool progression, there are advanced techniques that experienced Helm Bank professionals can apply.

### Technique 1: The Multi-Source Synthesis Prompt

Rather than moving sequentially through tools, you can ask Copilot to synthesize across multiple sources simultaneously:

"I need to brief the Chief Credit Officer on the Grupo Exportador deal in 5 minutes. Pull from our deal room OneNote, the latest credit memo in Word, and the Excel model summary tab. Give me a 90-second verbal brief covering: deal structure, key risks, and the one thing the CCO is most likely to push back on."

This is a cross-tool, multi-source, audience-aware synthesis — and Copilot handles it in seconds.

### Technique 2: The Consistency Checker

Before finalizing any multi-document package, use Copilot to check for internal consistency:

"Compare the financial figures in our credit memo Word document with the Excel model summary. List any discrepancies in dollar amounts, percentages, or ratios."

This catches the number-one error in complex deal packages: the PowerPoint says one thing, the Excel model says another, and neither matches the memo. Human reviewers often miss these. Copilot catches them reliably.

### Technique 3: The Audit Trail Builder

For regulatory purposes, you may need to demonstrate how you arrived at a credit decision. Copilot can help reconstruct the analytical trail:

"Review our OneNote deal room, Word credit memo, and Excel model for this credit. Write a one-page analytical summary showing the sequence of information gathered, analysis performed, and conclusions reached. This is for the credit file audit trail."

### Technique 4: The Parallel Track Generator

When you have multiple deals at different stages, use Copilot to manage your deal pipeline:

"Review my OneNote deal tracker. For each active deal, tell me: what stage it is in, what the next deliverable is, who is responsible, and whether it is on track based on the dates in the notes."

This turns your OneNote into a live deal pipeline dashboard — without building a formal project management system.

---

## Troubleshooting Cross-Tool Copilot Issues

Even in a well-configured Microsoft 365 environment, cross-tool workflows can hit friction. Here is how to diagnose and fix the most common issues.

### "Copilot Cannot Find My OneNote"

**Likely cause:** The notebook is stored locally or in a personal OneDrive folder that has not been shared with your team.

**Fix:** Move the notebook to a SharePoint-linked location or a shared Teams channel notebook. Copilot accesses SharePoint-connected content most reliably.

### "Copilot's PowerPoint Does Not Match My Word Doc"

**Likely cause:** Copilot did not reference the correct version of the Word document, or the document was not saved to a shared location.

**Fix:** Before running the PowerPoint generation prompt, explicitly reference the file: "Using the document named [exact filename] in my SharePoint deal folder, create a presentation..."

### "Copilot Summarized the Wrong Meeting"

**Likely cause:** Multiple meetings with similar names or participants. Copilot grabbed the most recent or most relevant match.

**Fix:** Be specific with date and participant: "Summarize the Teams meeting I had on [specific date] with [specific participants] about [specific topic]."

### "The Excel Formulas Copilot Suggested Do Not Work"

**Likely cause:** Copilot made an assumption about your data layout that does not match your actual spreadsheet.

**Fix:** Describe your data layout explicitly: "Column A has loan IDs, Column B has balances, Column C has interest rates. Row 1 is headers. Data runs from row 2 to row 145. Now write a formula to calculate..."

---

## The Human in the Loop: Where You Must Not Delegate

Copilot is a powerful co-pilot. The operative word is *co*. There are specific points in every workflow where a human banker — with judgment, accountability, and relationship context — must be in the seat.

**Never delegate to Copilot:**

**1. Final credit judgment.** Copilot can analyze; you decide. The credit risk sign-off is yours.

**2. Client relationship nuance.** Copilot does not know that this client's CFO is sensitive about questions regarding their Colombia operations, or that the CEO prefers to receive bad news in person. You do.

**3. Regulatory attestations.** Any document you sign attesting to accuracy or compliance is your attestation. Copilot's role in creating that document does not transfer its legal weight.

**4. Ethical judgment calls.** If a deal has something that feels wrong — an ownership structure that seems designed to obscure, a business model that does not quite make sense — that instinct is yours to act on. Copilot has no intuition.

**5. Final document review.** Every Copilot-generated document that becomes a formal work product must be reviewed by a human with subject-matter expertise before it is submitted, shared, or filed.

At Helm Bank, the value proposition of Copilot is not replacing banker judgment — it is giving bankers more time to exercise that judgment by eliminating the mechanical work that currently crowds it out.

---

## Chapter Summary

This chapter covered the architecture and practice of cross-tool AI workflows at Helm Bank. The key ideas:

**Microsoft Graph is the connective tissue.** It is what makes Copilot aware of your meetings, emails, notes, and documents across all Microsoft 365 tools simultaneously.

**The five-tool progression maps to a natural workflow.** Teams captures events, OneNote organizes knowledge, Word produces formal artifacts, Excel builds quantitative models, and PowerPoint communicates stories. Copilot accelerates every stage and smooths every handoff.

**Helm Bank's four core workflows** — Deal Origination, ALCO Prep, Client Onboarding, and Examiner Response — can each be dramatically accelerated using this framework.

**Good workflow design requires five elements:** A clear trigger, defined outputs, explicit handoff prompts, named owners, and quality checkpoints.

**Anti-patterns kill workflows.** Information silos, undocumented prompts, serial bottlenecks, and over-reliance on Copilot output without verification are the four most common failure modes.

**The human in the loop is non-negotiable.** Credit judgment, regulatory attestation, client relationship nuance, and final review are always human responsibilities.

---

## Your Homework

Before Session B of Week 5, complete the following:

**Assignment 1 — Workflow Audit (30 minutes)**

Pick one recurring work product you create at Helm Bank — a report, a memo, a presentation, a meeting summary. Map the current process:
- How many tools do you touch?
- Where does information get lost between tools?
- How long does it currently take?

Then redesign it as a Copilot-assisted cross-tool workflow using the framework from this chapter. Document the workflow using the five-element template.

**Assignment 2 — Run the Deal Brief Sprint**

If you have not done Exercise 14.1 in class, do it with a real recent meeting or a case from your active deal pipeline. Note how long it takes and what Copilot does well versus poorly.

**Assignment 3 — Consistency Check Test**

Find a deal or project where you have both a Word document and an Excel workbook. Run the consistency checker prompt: "Compare the financial figures in [Word doc] with [Excel workbook]. List any discrepancies." What does Copilot find? What does it miss?

**Reflection Question (bring to Session B):**

Where in your current work does information fall through the cracks between tools? Be specific. In Session B, we will workshop solutions using everything covered in this chapter.

---

```{admonition} Looking Ahead: Week 5, Session B
:class: tip
In Session B, we will go hands-on with building your personal Helm Bank Workflow Library — documenting your team's most valuable cross-tool workflows in a shareable format. We will also cover Copilot Studio: how Helm Bank's power users can build custom Copilot experiences that automate multi-step workflows with a single prompt. Bring your workflow audit from Assignment 1 — we will use them as raw material.
```

---

*Chapter 14 — Cross-Tool AI Workflows | The Essence of AI: A Microsoft Copilot Master Class for Helm Bank*
*For Internal Training Use Only*
