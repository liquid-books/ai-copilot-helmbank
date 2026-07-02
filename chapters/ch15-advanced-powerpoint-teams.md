---
title: "Chapter 15: Week 5, Session B — Advanced Copilot in PowerPoint & Teams"
subtitle: "From Slides to Strategy, From Meetings to Momentum"
short_title: "Advanced PowerPoint & Teams"
description: "Advanced techniques for Microsoft Copilot in PowerPoint and Teams — Presentation Coach, Intelligent Recap, Loop integration, channel intelligence, and high-stakes presentation workflows for Helm Bank professionals."
label: ch-15-advanced-powerpoint-teams
tags: [Copilot PowerPoint, Copilot Teams, Presentation Coach, Intelligent Recap, Loop, Microsoft 365, board deck, examiner presentation, Helm Bank, advanced]
---

```{admonition} Download this Chapter as PDF
:class: tip
[Download PDF](https://github.com/liquid-books/ai-copilot-helmbank/raw/main/pdfs/ch15-advanced-powerpoint-teams.pdf)
```

## The Night Before Everything

It is 9:47 PM on a Tuesday. Tomorrow at 10:00 AM, three OCC examiners will sit down in Helm Bank's eighth-floor conference room on Brickell Avenue. They have flown in from Washington. They are not here for the café con leche. They are here to examine your BSA/AML program, your internal controls, and your management's capacity to articulate risk in a clear, organized, and confident manner.

Your lead examiner presentation is due to be loaded onto the screen by 9:45 AM. You have a Word document with sixty-seven bullet points, a compliance team's summary email from last week, last quarter's risk dashboard from Excel, and a pile of meeting notes. You have no finished deck.

Fifteen years ago, this scenario ended careers. Tonight, it ends differently.

You open PowerPoint. You open Microsoft Copilot. You type: *"Create a presentation for an OCC examination on our BSA/AML compliance program. Include sections on governance, transaction monitoring, SAR filing statistics, customer due diligence, and our 2025 remediation plan. Use a professional, confident tone. I'll paste my source material."*

By 11:30 PM, you have a structured, branded, examiner-ready deck. By midnight, you have rehearsed it with Presentation Coach, tightened the narrative, and refined three slides that Copilot flagged as too text-heavy. At 7:00 AM, you send it to your CCO for a quick review.

The examination goes well.

This chapter is about how that happens — not as a one-time miracle, but as a repeatable, professional-grade capability. We go deep into Copilot's advanced features in PowerPoint and Teams, the two tools where Helm Bank professionals spend the most high-stakes communication time. We move beyond "generate a slide" into narrative architecture, brand alignment, post-meeting intelligence, and the kind of workflow integration that separates professionals who use AI from those who are merely curious about it.

---

## Part One: Advanced Copilot in PowerPoint

### Beyond "Create a Presentation"

Every Copilot user eventually discovers the basic create command. You type a topic, Copilot generates slides, and you stare at a deck that is structurally sound but somehow feels generic. This is the wall most people hit. They conclude that Copilot in PowerPoint is useful but limited.

The wall is not Copilot's ceiling. It is the depth of your prompt.

Advanced Copilot use in PowerPoint operates across four distinct layers, each building on the last:

1. **Structural prompting** — telling Copilot not just *what* to create, but *how* to think about the audience, the narrative arc, and the purpose of each slide
2. **Source-anchored generation** — feeding Copilot your actual documents, data, and notes so the output is grounded in your specific reality, not generic content
3. **Redesign and refinement** — using Copilot to iteratively improve existing slides, not just generate from scratch
4. **Brand alignment** — ensuring every generated element conforms to Helm Bank's visual identity, tone, and regulatory communication standards

Let us work through each layer in detail.

### Layer 1: Structural Prompting

The difference between a mediocre prompt and a powerful one is usually the absence of context. Copilot needs to understand three things before it can create presentation-quality output: the **audience**, the **purpose**, and the **desired emotional journey** of the presentation.

Consider the difference between these two prompts:

**Weak prompt:**
> "Create a presentation about Helm Bank's wire transfer process."

**Structured prompt:**
> "Create a 12-slide presentation about Helm Bank's wire transfer process for an audience of OCC bank examiners. The purpose is to demonstrate that our controls are rigorous, our staff is trained, and our escalation procedures are documented. The tone should be factual, confident, and organized. Structure: (1) Executive Summary, (2) Wire Transfer Volume Overview, (3) Origination Controls, (4) OFAC Screening Process, (5) Threshold Monitoring, (6) Correspondent Banking Controls, (7) Staff Training and Certification, (8) Audit Findings and Remediation, (9) Technology Infrastructure, (10) Key Metrics Dashboard, (11) Upcoming Enhancements, (12) Management Commitment Statement. Each slide should have a clear header, 4-5 bullet points maximum, and a designated space for a supporting chart or table."

The second prompt gives Copilot a complete architectural brief. It knows the audience (examiners), the purpose (demonstrate control rigor), the tone (factual and confident), the structure (12 named slides), and the visual constraints (4-5 bullets, chart space). The output will be dramatically more usable.

```{admonition} Helm Bank Presentation Types
:class: note
At Helm Bank, you will prepare presentations across at least four high-stakes contexts, each requiring a different structural approach:

**Regulatory/Examiner Presentations** (OCC, FDIC, FinCEN): Factual, evidence-based, control-focused. Lead with governance. End with remediation and management commitment.

**Board of Directors Decks**: Strategic framing first. Risk summary with trend lines. Forward-looking. Less detail, more judgment.

**Latin America Client Pitches**: Relationship-forward. Start with Helm Bank's binational story. Emphasize your understanding of their corridor. Close with a specific value proposition.

**Deal Closing Presentations**: Urgency-aware. Timeline visible. Decision points highlighted. Objection-handling slides embedded.

When prompting Copilot, always specify which type you are building.
```

### Layer 2: Source-Anchored Generation

The most powerful use of Copilot in PowerPoint is not creating from thin air — it is creating from *your* content. This is where Copilot becomes genuinely transformative for knowledge-intensive roles like compliance, finance, and relationship management.

**How to feed source material to Copilot:**

In the Copilot chat panel within PowerPoint, you can reference a document using the `/` command followed by the file name. For example: *"Using the Q2 Risk Report in SharePoint [/Q2-Risk-Report-2025.docx], create slides summarizing our top five operational risks and their current mitigation status."*

For shorter source material — emails, meeting notes, brief reports — paste the text directly into the Copilot prompt and instruct it to synthesize: *"Here is our compliance team's summary from last week's SAR review meeting [paste text]. Create three slides: one summarizing filing volume trends, one on key typologies identified, and one on process improvements implemented."*

If your source is a structured Word document, open it and ask Copilot to generate a presentation from it: *"Create a presentation based on this document. Treat each major section heading as a slide title. Extract the key findings from each section as bullet points."*

```{admonition} Source Material Quality Matters
:class: warning
Copilot synthesizes from what you give it. If your source document is disorganized, contains contradictory data, or uses internal jargon without definition, the resulting slides will reflect those same weaknesses. Before feeding a document to Copilot, spend five minutes organizing the structure. A clear source produces a clear presentation.
```

### Layer 3: Slide-by-Slide Refinement

One of the most underused features in Copilot for PowerPoint is the per-slide refinement capability. Rather than regenerating the entire presentation, you can select a specific slide and ask Copilot to improve it in targeted ways.

This is particularly useful when a slide is text-heavy and needs visual restructuring, when the language is too technical for your audience, when you want to add specific data that was not in the original source, or when the slide's narrative does not connect logically to the slides before and after it.

**To refine a single slide:**
1. Click on the slide in the slide panel
2. Open the Copilot panel (Home → Copilot)
3. With the slide selected, type your refinement instruction

**Refinement prompt examples:**

- *"This slide has too much text. Rewrite it with no more than 4 bullet points, each under 12 words. Keep only the most critical information."*
- *"The language on this slide is too technical for a non-banker board member. Simplify without losing the key point."*
- *"Add a callout box on this slide highlighting our 98.3% OFAC screening accuracy rate as a key metric."*
- *"Rewrite the title of this slide as a specific, evidence-based claim rather than a generic label. For example, instead of 'Training Program,' write 'Staff Certification Rate Increased 34% in 2025.'"*

That last prompt reflects an important principle in high-stakes presentation design: **slide titles should make claims, not just name topics**. A title that makes a claim ("Customer Due Diligence Controls Exceed Regulatory Expectations") is far more persuasive than one that merely labels a subject ("Customer Due Diligence").

```{figure} images/ch15-slide-refinement-workflow.png
:alt: Screenshot showing the Copilot panel in PowerPoint open alongside a selected slide, with a refinement prompt typed in the chat and the suggested revision visible on the slide canvas.
:width: 85%

Copilot's per-slide refinement workflow: select a slide, open the panel, prompt for a specific improvement. The change is applied directly to the slide, not to the entire deck.
```

### Layer 4: Brand Kit Alignment

Helm Bank has a visual identity — specific fonts, colors, logo placement, and image style that reflect the bank's positioning as a sophisticated, Miami-based international institution. Copilot-generated presentations, by default, may not match this identity exactly.

The most reliable way to ensure brand alignment is to apply Copilot generation *on top of* an approved Helm Bank PowerPoint template. Open your approved Helm Bank master template stored in the shared SharePoint Templates library. Do not start from a blank file — your master template carries all the branded slide layouts, color themes, and font settings. With the template open, trigger Copilot to generate content: the new slides will adopt your template's formatting rather than Copilot's defaults. After generation, use Design → Designer to let PowerPoint suggest layout refinements within your brand colors.

**Manual Brand Alignment Checks:**

Even with a template in place, Copilot sometimes introduces elements that drift from brand standards. After any Copilot-generated presentation, run this four-point check:

- [ ] All fonts match the approved typeface (typically Calibri or a bank-approved alternative)
- [ ] Color palette uses only approved Helm Bank brand colors (check the Color Picker against your brand guide hex codes)
- [ ] Logo placement is consistent across all slides
- [ ] Images and icons use the approved library style (photography vs. illustration; warm versus cool tones)

```{admonition} Helm Bank Brand Tip
:class: tip
Helm Bank's visual identity reflects its dual character: rigorous enough for regulatory confidence, warm enough for client relationships. When Copilot offers you image suggestions, favor photography of real people in professional settings over generic stock illustrations. The bank's Latin America client base in particular responds to authentic imagery. If Copilot generates an image placeholder, replace it with a photo from the approved Helm Bank imagery library in SharePoint.
```

---

### Presentation Coach: Your Secret Rehearsal Partner

Presentation Coach is one of the most underappreciated features in Microsoft 365, and when used alongside Copilot, it becomes a genuine competitive advantage for anyone who presents high-stakes content.

**What Presentation Coach Does:**

Presentation Coach listens as you rehearse and provides real-time and post-rehearsal feedback on:

- **Pacing** — are you speaking too fast or too slow?
- **Filler words** — how many times did you say "um," "uh," "basically," or "you know"?
- **Monotone delivery** — flagging when your vocal pitch is flat
- **Body language** (in Teams/camera rehearsal mode) — eye contact, posture, gesturing
- **Slide coverage** — did you spend too long on a single slide and rush through others?
- **Originality** — a flag if you are reading directly from the slide text, which is a cardinal sin in examiner presentations

**How to Access Presentation Coach:**

In PowerPoint, go to **Slide Show → Rehearse with Coach**. The presentation will begin in full-screen mode with a small Coach overlay in the corner. Rehearse as if the audience is in front of you. When finished, Presentation Coach generates a detailed report with metrics and specific improvement recommendations.

```{admonition} Examiner Presentation Best Practice
:class: important
OCC and FDIC examiners are experienced professionals who can immediately detect when a presenter is reading from slides. Presentation Coach will flag this behavior. Practice until you are speaking *to* the slides, not from them. Your slides should contain keywords and data points; your spoken words should add context, judgment, and management perspective that is not on the slide.
```

**The Copilot + Coach Workflow:**

The most effective rehearsal workflow combines both tools in sequence:

1. **Generate with Copilot** — create your initial deck from source material
2. **Refine with Copilot** — tighten slide content, improve titles, reduce text density
3. **Rehearse with Coach** — deliver the presentation out loud, noting Coach's feedback
4. **Refine again with Copilot** — take Coach's feedback (for example, "Slide 7 is text-heavy and you spent 8 minutes on it") and ask Copilot to help restructure that slide
5. **Rehearse again** — until Coach's feedback is consistently positive

For a high-stakes presentation like an OCC examination opener, plan for at least three full rehearsals with Coach. The first will feel rough. The third will feel ready.

```{figure} images/ch15-presentation-coach-report.png
:alt: Presentation Coach summary report showing metrics for pace in words per minute, filler word count, and a timeline showing time spent on each slide during rehearsal, with specific improvement tips listed below.
:width: 80%

A Presentation Coach post-rehearsal report: quantified feedback on pace, filler words, and slide timing. Use this report to direct your next round of Copilot refinements.
```

---

### Narrative Architecture: The Spine of a Great Presentation

Copilot can generate content. It cannot automatically create the *meaning* that connects slides into a persuasive argument. That architecture comes from you — but Copilot can help you build and stress-test it.

**The Three-Act Structure for Bank Presentations:**

Regardless of presentation type, high-stakes bank presentations follow a reliable narrative structure:

**Act 1 — Context and Stakes** (approximately 20% of slides)
- Where we are
- Why this matters
- What we will show you

**Act 2 — Evidence and Analysis** (approximately 60% of slides)
- The detailed case
- Data, controls, processes, outcomes
- Addressing potential objections preemptively

**Act 3 — Confidence and Forward Look** (approximately 20% of slides)
- What we have accomplished
- What we are committed to
- The ask or the close

Use Copilot to audit your narrative structure with this prompt: *"Review the titles of these slides [list them] and tell me if the narrative flows logically from context to evidence to conclusion. Flag any gaps, repetitions, or slides that seem out of sequence."*

Copilot will identify where your story loses thread — a slide that introduces a new idea without context, a section that repeats a point made earlier, or a conclusion that does not follow from the evidence presented.

---

### Hands-On Exercise 1: The Examiner Deck Sprint

**Scenario:** You have 90 minutes to build an OCC-ready presentation on Helm Bank's BSA/AML transaction monitoring program. You have three source documents: a process description document, a Q2 metrics email, and a list of audit findings and their resolution status.

**Step 1 — Structural Prompt (10 minutes)**

Open PowerPoint with the Helm Bank master template. Open the Copilot panel. Type:

*"Create a 10-slide presentation for OCC bank examiners on Helm Bank's transaction monitoring program within our BSA/AML framework. Structure: (1) Overview of TM Program, (2) Monitoring System Architecture, (3) Alert Generation and Thresholds, (4) Alert Review Workflow, (5) Escalation to SAR Decision, (6) Q2 Monitoring Metrics, (7) Key Typologies Identified, (8) Recent Audit Findings, (9) Remediation Status, (10) Program Enhancements Planned. Tone: professional, factual, confident. Maximum 5 bullet points per slide."*

**Step 2 — Source Integration (20 minutes)**

Paste your Q2 metrics email into the Copilot prompt for slide 6: *"Using this data [paste email], replace the placeholder content on Slide 6 with specific metrics: alert volume, investigation rate, SAR conversion rate, and average investigation time."*

Repeat for slides 8 and 9 using your audit findings list.

**Step 3 — Narrative Refinement (20 minutes)**

Ask Copilot: *"Review the titles of all 10 slides and rewrite any that are generic topic labels into specific claim statements that convey confidence and control."*

**Step 4 — Coach Rehearsal (30 minutes)**

Rehearse twice with Presentation Coach. After the first rehearsal, note which slides took too long and which felt underprepared. Use Copilot to expand bullet points on the underprepared slides and reduce text on the overloaded ones.

**Step 5 — Final Polish (10 minutes)**

Run the four-point brand alignment check. Confirm all images are appropriate. Verify that the final slide includes management contact information and a clear next-steps statement.

**Expected outcome:** A polished, examiner-ready presentation in 90 minutes that would have taken a full day without Copilot.

---

### Advanced Slide Types: Data, Dashboards, and Comparisons

Copilot in PowerPoint has specific strengths when working with data-heavy slides — the kind that dominate board decks and regulatory presentations.

**Dashboard Slides:**

When creating a KPI dashboard slide, prompt Copilot with specific metrics: *"Create a dashboard slide titled '2025 Compliance Program Health Metrics' with six KPI boxes. Include: SAR Filing Rate (on target), OFAC False Positive Rate (improved), CDD Completion Rate (exceeds threshold), Training Completion Rate (98%), Audit Finding Closure Rate (ahead of schedule), and Technology System Uptime (99.7%). Use green/yellow/red status indicators."*

Copilot will generate the layout; you will manually update the actual figures from your source data. The value is that the structure, hierarchy, and visual logic are already in place.

**Comparison Slides:**

For before/after or peer comparison content: *"Create a side-by-side comparison slide showing Helm Bank's transaction monitoring performance in 2023 versus 2025. Left column: 2023 metrics [list them]. Right column: 2025 metrics [list them]. Title the slide to reflect that improvement is the key message."*

**Timeline Slides:**

For remediation plans and project roadmaps: *"Create a timeline slide showing our 2025 BSA Remediation Plan milestones: Q1 [milestone], Q2 [milestone], Q3 [milestone], Q4 [milestone]. Mark Q1 and Q2 as complete. Q3 as in progress. Q4 as planned."*

These three slide types — dashboards, comparisons, and timelines — cover the majority of high-value content in board decks and regulatory presentations. Mastering how to prompt for each will eliminate the most time-consuming manual slide-building work.

---

## Part Two: Advanced Copilot in Microsoft Teams

### From Meeting Tool to Intelligence Platform

Most Teams users understand Copilot as a meeting assistant — it takes notes, summarizes discussions, and answers questions during calls. That understanding captures perhaps 30% of what Copilot in Teams can actually do.

The remaining 70% lives in three areas that most professionals have not fully explored:

1. **Intelligent Recap** — deep post-meeting intelligence that goes far beyond a summary
2. **Channel Copilot** — using Copilot to navigate, synthesize, and act on information in Teams channels, where much of Helm Bank's institutional knowledge actually lives
3. **Loop integration** — connecting meeting intelligence to collaborative, living documents that keep teams aligned between meetings

Let us go deep into each.

### Intelligent Recap: Post-Meeting Intelligence

Intelligent Recap is what happens after your meeting ends and the recording is processed. If you have been skipping the Recap tab in Teams, you have been leaving a significant intelligence resource untapped.

**What Intelligent Recap Provides:**

After a recorded meeting with transcription enabled, Teams generates:

- **AI-generated meeting notes** — a structured summary organized by topic, not just chronologically
- **Action items with owners** — automatically identified from the conversation ("I'll send that report by Friday" becomes an assigned action item)
- **Chapter markers** — the meeting divided into named segments so you can jump directly to the conversation about a specific topic without watching the full recording
- **Speaker timeline** — who spoke when, and for how long
- **Mentioned names and follow-ups** — anyone referenced in the meeting who might need follow-up
- **Keyword and topic search** — type any word and jump to the moment in the recording where it was discussed

**Advanced Recap Workflows:**

For recurring committee meetings such as the BSA Committee, Loan Review, and Risk Committee: after each meeting, open the Recap and immediately copy the action items into a Teams channel post or Loop component. This creates a running, searchable record of commitments made in every meeting — invaluable when examiners ask "what actions did your BSA Committee take in Q3?"

For examiner preparation: if your team has conducted internal prep calls for an upcoming examination, use Recap to extract every commitment and action item made during those calls. Create a checklist in Loop and assign ownership to each item.

For client relationship calls with Latin America partners: Recap is particularly valuable when calls involve multiple participants with different native languages. The AI notes often capture nuance that manual note-takers miss, especially when conversation moves quickly between English and Spanish.

```{admonition} Helm Bank Application: BSA Committee Documentation
:class: note
The BSA/AML Officer at Helm Bank must maintain documented evidence that the BSA Committee meets regularly, discusses specific topics, and takes action on identified risks. Intelligent Recap generates ready-made documentation for every meeting. Create a SharePoint folder structure organized by committee and quarter. After each BSA Committee meeting, export the Recap — notes plus action items — to that folder. When examiners request meeting documentation, it is already organized and waiting.
```

```{figure} images/ch15-intelligent-recap-view.png
:alt: The Teams Intelligent Recap interface showing a recorded meeting with chapter markers on the left, AI-generated notes in the center panel organized by topic, and action items with assigned owners in the right column.
:width: 85%

Intelligent Recap in Teams: chapter-marked recording, AI-organized notes by topic, and automatically extracted action items with owners. This is post-meeting intelligence, not just a transcript.
```

### Copilot in Teams Channels: Where Institutional Memory Lives

Meetings get most of the attention, but channels are where Helm Bank's day-to-day institutional knowledge actually accumulates. A channel with six months of posts, shared files, and threaded conversations contains an enormous amount of valuable information — and it is nearly impossible for any individual to navigate it manually.

Copilot in Teams channels changes this equation entirely.

At the top of any Teams channel, you can ask Copilot questions about the channel's content. This includes posts, replies, shared files, and meeting summaries from meetings held in that channel.

**For the Compliance Operations channel:**
- *"What were the main topics discussed in this channel over the past 30 days?"*
- *"Summarize all posts related to the SAR filing process. What concerns have been raised?"*
- *"List every document that has been shared in this channel in 2025."*
- *"Who has been most active in discussions about the new monitoring thresholds, and what positions have they taken?"*
- *"Are there any unresolved questions or open items in this channel?"*

**For the Helm Bank Latin America Desk channel:**
- *"Which clients have been discussed most frequently in the past quarter?"*
- *"Summarize the conversation about correspondent banking restrictions from last month."*
- *"What deals are currently referenced as in progress in this channel?"*

**For the Loan Review channel:**
- *"What loans were discussed in this channel but did not result in an approval recommendation?"*
- *"Summarize the concerns raised about commercial real estate concentrations."*

This is institutional memory on demand. Instead of spending an hour scrolling through months of posts to prepare for a meeting, you ask Copilot and get a synthesized briefing in seconds.

```{admonition} Pro Tip: Channel Hygiene for Copilot
:class: tip
Copilot can only surface what is in the channel. If your team routinely discusses important decisions in private messages or group chats rather than in channels, that institutional memory is invisible to Copilot. Helm Bank teams that want to maximize channel intelligence should adopt a clear norm: substantive decisions, important context, and key documents belong in channels, not in DMs. This practice also serves regulatory documentation purposes — if it matters, it should be in the channel.
```

### Loop Integration: Living Documents That Move with Your Work

Microsoft Loop is the connective tissue between meetings, channels, and documents. A Loop component is a collaborative block of content — a table, checklist, note, or agenda — that can be embedded simultaneously in a Teams chat, a Teams channel, a Word document, and an Outlook email. When anyone edits it anywhere, it updates everywhere.

Combined with Copilot, Loop becomes the foundation of a powerful post-meeting workflow.

**The Anatomy of a Copilot-Powered Loop Workflow:**

**Step 1: Pre-meeting — Create a Loop agenda**
Before any important meeting, open Loop and create a meeting agenda component. Share it in the Teams meeting invite and in the channel. All participants can add topics and pre-meeting notes before the call begins.

**Step 2: During the meeting — Copilot captures**
With transcription enabled, Copilot tracks the conversation. You focus on participating, not note-taking.

**Step 3: Post-meeting — Intelligent Recap feeds Loop**
After the meeting, open Intelligent Recap. Copy the action items. Paste them into a Loop checklist in the channel. Assign owners. Set due dates. The Loop component is now live in the channel, in any open Outlook threads about the meeting, and accessible to every team member.

**Step 4: Between meetings — Copilot summarizes progress**
In the days between meetings, team members update the Loop checklist as items are completed. At any point, you can ask Copilot in the channel: *"Summarize the current status of the action items from the [meeting name] on [date]."*

**Step 5: Next meeting — Loop as the opening context**
Open the next meeting by pulling up the Loop component. Everyone sees what was committed, what was completed, and what is still open. Copilot can generate a pre-meeting briefing: *"Based on the Loop checklist from our last Compliance Review meeting, what items are still open and which need to be discussed today?"*

```{figure} images/ch15-loop-workflow-diagram.png
:alt: A workflow diagram showing a Loop component embedded in a Teams meeting invite, a Teams channel, and an Outlook email simultaneously. The action items section is highlighted, showing how updates made in any location appear in all other locations automatically.
:width: 90%

Loop's embedded-everywhere architecture: one action item checklist, simultaneously live in the meeting invite, the Teams channel, and the follow-up email thread. No more searching for where decisions were tracked.
```

---

### Hands-On Exercise 2: Building the Post-Meeting Intelligence System

**Scenario:** You are the BSA/AML Officer. Your monthly BSA Committee meeting just ended. You need to document the meeting, extract action items, and set up a tracking system that will satisfy regulatory documentation standards.

**Step 1 — Access Intelligent Recap (5 minutes)**

In Teams, navigate to the meeting in your calendar or in the Chat tab. Click on the meeting entry and select the **Recap** tab. Review the AI-generated notes. Confirm that the major topics discussed are correctly identified.

**Step 2 — Audit and Correct (5 minutes)**

Scroll through the action items Copilot has extracted. For any that are incorrect or missing, add them manually. For any that are incorrectly assigned, reassign them to the correct person. This is your human judgment layer — Copilot identifies, you verify.

**Step 3 — Create a Loop Action Item Component (5 minutes)**

In the BSA Committee Teams channel, create a new post. Type `/` and insert a Loop component by selecting Checklist. Paste or retype each action item as a checklist entry. Assign each to its owner using @mention. Add a due date in the notes field.

**Step 4 — Export to SharePoint Documentation Folder (5 minutes)**

In Intelligent Recap, export the meeting notes as a PDF or Word document. Navigate to your BSA Documentation SharePoint folder and upload the file with the naming convention: `BSA-Committee-YYYY-MM-DD-Recap.pdf`.

**Step 5 — Send Meeting Follow-Up (5 minutes)**

Return to Outlook. Open a new email to all committee members. Insert the Loop action item checklist as an embedded component. Write a brief opening sentence and send. Every recipient now sees the same live checklist — when they complete items, everyone's view updates automatically.

**Total time: Under 25 minutes for complete BSA Committee meeting documentation that meets examiner standards.**

---

### Advanced Meeting Intelligence: Asking Smarter Questions

During a live meeting, Copilot's in-meeting chat is available to all participants — not just the organizer. Most people use it only to ask for a summary of what they missed. That is the tip of the iceberg.

**Advanced in-meeting Copilot prompts:**

For complex discussions:
- *"What are the different positions that have been expressed about [topic] so far?"*
- *"Summarize the arguments for and against the proposed change to our monitoring thresholds."*
- *"What questions have been asked in this meeting that have not yet been answered?"*

For action clarity:
- *"What commitments have been made in this meeting so far and who made them?"*
- *"What is [person's name] proposing to do next?"*

For late arrivals without interrupting the meeting:
- *"I joined late. Summarize what has been discussed about the Q3 risk assessment."*

For facilitators:
- *"Are there any topics from the agenda that have not yet been addressed?"*
- *"Summarize the key decisions made in this meeting so far."*

```{admonition} Cultural Note for Latin America Calls
:class: note
Helm Bank's client calls with Latin American partners often involve indirect communication styles, relationship-building segments at the start of calls, and conversations that mix business and personal topics. When asking Copilot to summarize a client call, be specific about what you want extracted: *"Summarize the business commitments made in this call, excluding the social conversation at the beginning."* This prevents Copilot from generating summaries that over-index on social content and under-represent the business substance.
```

---

### Teams Channel Strategy for High-Performance Teams

Advanced Copilot use in Teams works best when your channel structure is intentional. A chaotic channel architecture — too many channels, inconsistently used, with important content scattered across DMs and group chats — undermines the intelligence Copilot can provide.

**Recommended Channel Architecture for Helm Bank Compliance Teams:**

| Channel | Purpose | Copilot Use |
|---------|---------|-------------|
| General | Team-wide announcements, non-urgent updates | Monthly summaries of channel activity |
| BSA-AML Operations | Day-to-day monitoring discussions, alerts, SARs | "What typologies have been flagged this month?" |
| Regulatory Correspondence | All examiner communications, letters, responses | "Summarize all OCC correspondence from 2025" |
| Audit and Findings | Audit findings, remediation tracking, evidence | "What findings are still open and past due?" |
| Training and Policy | Policy updates, training completion, certifications | "Who has not completed the Q3 training module?" |
| Latin America Desk | Correspondent banking, client discussions | "What correspondent concerns were raised this week?" |

Each of these channels becomes a searchable, Copilot-navigable knowledge base over time. The investment is in posting consistently — the return is an institutional memory that survives employee turnover and answers examiner questions in minutes rather than days.

---

### Hands-On Exercise 3: The Latin America Client Pitch

**Scenario:** A Miami-based family office with significant business operations in Colombia and Panama is considering Helm Bank for their US banking relationship. They have a 45-minute meeting scheduled for next week. You need to build a compelling pitch deck and prepare for the meeting with full intelligence support.

**Step 1 — Research Synthesis with Copilot (15 minutes)**

Query your relevant Teams channel for prior touchpoints: *"Summarize what we know about this prospect from our Teams channel conversations. What have they asked about? What concerns have they expressed?"*

If this is a cold prospect, ask Copilot in PowerPoint: *"Create a 10-slide pitch deck for a family office with operations in Colombia and Panama. The prospect values: (1) privacy and discretion, (2) speed of wire execution for cross-border transactions, (3) a banking partner who understands the Latin America business environment, (4) a relationship manager who speaks their language — literally and figuratively. Helm Bank's value propositions: bilingual staff, deep Latin America network, Miami location as a natural US entry point, international wire expertise, and a 35-year track record as a corridor bank. Include slides on: Helm Bank overview, Our Latin America story, Wire capabilities, Compliance partnership, Correspondent network, Team introductions, and a specific proposal for this client."*

**Step 2 — Personalize with Channel Intelligence (10 minutes)**

If you have a client record or prior conversation in your CRM or Teams channel, extract specific details and ask Copilot to incorporate them: *"Update Slide 7 to reference [specific industry] because this client's primary business is in [industry]. Adjust the language in Slide 3 to acknowledge that they have had previous US banking relationships that did not work out, and frame Helm Bank as a different kind of partner."*

**Step 3 — Presentation Coach Rehearsal (15 minutes)**

Rehearse the pitch with Presentation Coach. Pay particular attention to three questions: Do you sound like you know this client, or are you reading generic content? Is your opening story personal and specific, or generic? Does your closing ask for a clear, specific next step?

**Step 4 — Meeting Setup in Teams (10 minutes)**

Schedule the meeting in Teams. Create a pre-meeting Loop agenda and share it with your relationship manager. Enable meeting transcription. Prepare three Copilot prompts to use during the meeting if the conversation goes in unexpected directions.

**Step 5 — Post-Meeting Workflow (10 minutes after the meeting)**

After the meeting: run Intelligent Recap, extract action items into a Loop checklist, send the follow-up email with the Loop component embedded, and update your CRM with notes generated from the Recap.

**Expected outcome:** A fully prepared, personalized client pitch with a complete pre-to-post meeting intelligence workflow that can be replicated for every significant prospect meeting.

---

## Part Three: Integrating PowerPoint and Teams into a Unified Workflow

### The Presentation Intelligence Loop

The most sophisticated Copilot users in financial institutions have stopped thinking about PowerPoint and Teams as separate tools. They have built a continuous intelligence loop:

**Channel intelligence informs presentation creation.** Before building any important deck, query the relevant Teams channels for institutional context: What has been discussed? What questions have been raised? What data has been shared? This channel intelligence feeds your PowerPoint prompt and makes the resulting deck more grounded and specific.

**Presentations are shared in Teams for collaborative refinement.** Upload your draft deck to the Teams channel. Share the link. Ask team members to comment. Use channel Copilot to synthesize their feedback: *"Summarize all the feedback posted about the Q4 Board Deck in this channel."*

**Meetings refine the presentation narrative.** Use Teams meetings with Copilot transcription to rehearse the presentation with stakeholders. Intelligent Recap surfaces the specific slides that generated the most questions — these are your weak points.

**Post-meeting action items drive presentation updates.** The action items from your prep meetings, tracked in Loop, become the checklist for your final presentation revisions.

**Final presentation delivered, meeting captured.** When you deliver the presentation — to examiners, to the board, to a client — the meeting is recorded and Intelligent Recap generates documentation of the discussion. That documentation feeds back into the channel and into future presentations.

This loop does not just make individual presentations better. It builds an organizational intelligence capability that compounds over time.

```{figure} images/ch15-intelligence-loop-diagram.png
:alt: A circular flow diagram showing five stages: Channel Intelligence feeds Presentation Creation, which is refined through Collaborative Refinement in Teams, then delivered in a Meeting and captured by Intelligent Recap, which feeds back into Channel Intelligence. Each stage is labeled with the specific Copilot feature that powers it.
:width: 90%

The Presentation Intelligence Loop: a continuous workflow where Teams channel knowledge feeds PowerPoint creation, which is refined in Teams meetings, captured by Intelligent Recap, and fed back into the channel for the next cycle.
```

---

### Tab-Set: PowerPoint vs. Teams Copilot Capabilities

`````{tab-set}
````{tab-item} Copilot in PowerPoint
**Best For:**
- Creating structured presentations from source documents
- Slide-by-slide refinement and redesign
- Brand alignment within master templates
- Practicing delivery with Presentation Coach
- Converting Word reports and compliance summaries into visual presentations

**Key Prompts:**
- `"Create a [N]-slide presentation for [audience] on [topic] structured as [outline]"`
- `"Rewrite the title of every slide as a specific claim rather than a topic label"`
- `"This slide is too text-heavy. Reduce to 4 bullets of 12 words or fewer"`
- `"Using the file [/SharePoint document], create slides for sections [X], [Y], [Z]"`
- `"Add a dashboard slide with these [N] KPIs, using green/yellow/red indicators"`

**Limitations:**
- Cannot access external data sources directly — must paste or reference SharePoint files
- Brand alignment requires starting from an approved template
- Presentation Coach is a separate feature accessed via the Slide Show menu, not the Copilot panel

**Helm Bank Priority Uses:**
- OCC and FDIC examiner presentations
- Board of Directors quarterly decks
- Latin America client pitches
- Training and policy update decks for annual compliance reviews
````

````{tab-item} Copilot in Teams
**Best For:**
- Meeting intelligence and post-meeting documentation
- Navigating channel history to surface institutional knowledge
- Extracting action items and decisions from recorded meetings
- Connecting meeting outputs to living Loop documents
- Catching up on missed meetings or long channel threads

**Key Prompts:**
- `"Summarize what has been discussed in this channel over the past [timeframe]"`
- `"What commitments were made in the [meeting name] meeting and who made them?"`
- `"What questions from the agenda have not been addressed in this meeting?"`
- `"Summarize all posts related to [topic] in this channel"`
- `"List every unresolved question or open item in this channel"`

**Limitations:**
- Cannot access DMs or private chats — only channels and meetings you have access to
- Channel intelligence is only as good as what has been posted in channels
- Intelligent Recap requires recording and transcription to be enabled *before* the meeting starts

**Helm Bank Priority Uses:**
- BSA Committee and Risk Committee meeting documentation
- Regulatory examination preparation and tracking
- Latin America deal pipeline management
- Internal training session follow-up and compliance certification tracking
````
`````

---

### Regulatory Readiness: The Copilot Advantage

For a bank like Helm Bank, regulatory readiness is not an occasional project — it is a permanent operational state. Examiners can arrive with little notice. Documentation requests can cover years of activity. The ability to quickly synthesize, present, and defend your programs is a core institutional capability that Copilot materially improves.

**Documentation Quality**

Intelligent Recap ensures that every significant meeting is documented with consistent structure and detail. The quality of your BSA Committee minutes, Loan Review records, and Risk Committee documentation will improve immediately when Recap is consistently used and its outputs are properly organized in SharePoint. This is not aspirational — it is mechanical. Turn on transcription, access Recap after the meeting, export to SharePoint. Done.

**Presentation Confidence**

Examiner presentations built with Copilot's structural prompting, refined through iteration, and rehearsed with Presentation Coach will be measurably better than those produced without these tools. Clearer structure. More evidence-based slide titles. Better pacing. These are not subjective improvements — they are the specific factors that examiners evaluate when assessing management competence.

**Response Speed**

When an examiner sends a document request or asks a follow-up question from a previous examination, your ability to search channel history with Copilot and generate a synthesized, presentation-ready response in hours rather than days is a genuine competitive advantage in the examination process.

```{admonition} Helm Bank Compliance Use Case: The 48-Hour Prep Window
:class: important
When Helm Bank receives an OCC or FDIC examination notice, the team typically has between 48 and 72 hours to prepare the initial management presentation and assemble the first tranche of requested documentation. With the workflows described in this chapter — channel intelligence synthesis, source-anchored presentation generation, and Intelligent Recap for prior meeting documentation — this preparation time can be cut by 40% or more. The human judgment that matters most — deciding what to emphasize, what to acknowledge directly, and where to demonstrate management's forward-looking commitment — can now be applied to a far more complete foundation in the same amount of time.
```

---

### The Quarterly Board Deck: A Deep Dive

The quarterly board presentation is one of the highest-stakes documents Helm Bank produces. It is reviewed by directors who are legally responsible for the bank's safety and soundness. It is scrutinized by regulators who may review board minutes. It must be both comprehensive enough to inform and concise enough to respect directors' time.

Copilot transforms the board deck workflow in three specific ways.

**First, aggregation from multiple sources.** A typical board deck draws on the risk report, the compliance update, the financial summary, the credit quality review, and the operational update — each maintained by a different department. Traditionally, assembling these into a coherent deck requires hours of coordination and copy-paste work. With Copilot, you can reference each source document and prompt: *"From this Q3 Risk Report and this Compliance Update, create five slides for the Board Deck that synthesize the most important risk themes, using language appropriate for board-level readers rather than operational staff."*

**Second, consistent framing.** Board decks benefit from consistent structural framing across quarters so directors can track trends. Use a Copilot prompt that references prior quarters: *"Here is the Q2 Board Deck risk section [paste titles]. Create the Q3 version using the same structural format but updated with this quarter's data [paste data]. Flag any significant changes from Q2."*

**Third, the CEO narrative page.** Most board decks include an opening letter or narrative from the CEO that frames the quarter's results. This is one of the most difficult pieces to write — it must be authoritative, honest, and forward-looking simultaneously. Copilot can generate a strong first draft: *"Write a 300-word opening narrative for the Q3 Board Deck. Tone: confident but candid. Key themes: solid performance in core business, continued investment in compliance infrastructure, and management's commitment to controlled growth in the Latin America corridor. We had one regulatory matter resolved this quarter [brief description]. We are on track with our three-year strategic plan."*

The CEO or Senior Management will revise and personalize — but starting from a structured 300-word draft saves significant time and creative energy.

---

### Building a Deal Closing Presentation

Helm Bank's relationship managers close deals — loans, treasury management relationships, international banking arrangements. The deal closing presentation is the last formal touchpoint before a prospect becomes a client. It must be compelling, specific, and decisively organized.

The anatomy of an effective deal closing presentation, prompted through Copilot:

*"Create an 8-slide deal closing presentation for [Prospect Name], a [company type] seeking [specific banking services]. The purpose of this presentation is to move from 'interested' to 'signed.' Structure: (1) Title slide — their name, their logo, our value proposition for them specifically, (2) What we heard — the three specific needs they have expressed to us, (3) Our solution — how Helm Bank directly addresses each need, (4) Our team — the specific people who will serve this relationship by name and role, (5) Implementation timeline — what happens in the first 30/60/90 days, (6) Pricing and terms — presented clearly, without jargon, (7) References and proof points — two or three relevant case studies or client outcomes we can cite, (8) The ask — a clear, specific decision requested. Tone: confident, specific, and client-centered. No generic banking language."*

The instruction "no generic banking language" is important. Copilot, like most AI systems, can default to industry jargon that sounds impressive but communicates nothing. Explicitly prohibiting it produces cleaner, more persuasive output.

---

## Chapter Summary

This chapter has moved through two powerful, interconnected domains: advanced Copilot in PowerPoint, and advanced Copilot in Microsoft Teams.

In PowerPoint, we explored four layers of sophisticated use: structural prompting that gives Copilot a complete architectural brief; source-anchored generation that grounds output in your actual content; slide-by-slide refinement that iteratively improves any deck; and brand alignment workflows that keep Copilot-generated content visually consistent with Helm Bank's identity. We introduced Presentation Coach as a rehearsal partner that turns raw presentations into polished, examiner-ready deliveries, and we built the narrative architecture framework — context, evidence, confidence — that turns generated slides into persuasive arguments.

In Teams, we went deep into Intelligent Recap as a documentation and intelligence tool for regulated financial institutions; Channel Copilot as a way to navigate months of institutional knowledge in seconds; and Loop integration as the connective tissue that keeps meeting outputs alive and actionable between meetings.

We integrated these two tools into a unified Presentation Intelligence Loop — a workflow where channel knowledge feeds presentation creation, collaborative refinement in meetings improves the deck, delivery is captured by Recap, and the output feeds back into the channel for the next cycle.

We applied every capability to the specific realities of Helm Bank: OCC and FDIC examiner presentations, BSA Committee documentation, Latin America client pitches, quarterly board decks, and deal closing presentations. The bank's 35-year history as a corridor institution, its deep Latin America relationships, and its federally supervised status all create specific documentation and presentation requirements that Copilot is now equipped to support.

---

## Your Homework

Before the next session, complete the following three assignments. Each is designed to build a real capability, not just demonstrate that you tried.

**Assignment 1 — The Structural Prompt Challenge**

Choose any presentation you have built in the last six months. Write a new structural prompt that includes: a specific audience description, the presentation's purpose stated in one sentence, the desired emotional arc of the presentation, a complete slide structure with each slide named, tone guidance, and visual constraints such as maximum bullets per slide. Feed this prompt to Copilot in PowerPoint and compare the output to your original. Note three specific improvements and one area where your human judgment still outperforms the AI output.

**Assignment 2 — Channel Intelligence Audit**

Pick one Teams channel your team uses regularly. Ask Copilot: *"Summarize the most important topics discussed in this channel over the past 60 days. Identify any open questions or unresolved issues."* Review the output carefully. How accurate is it? What would an OCC examiner be able to learn about your program from this channel if Copilot surfaced its contents? What does that tell you about your channel hygiene and documentation practices? Write a one-paragraph assessment and share it with your manager.

**Assignment 3 — Build Your Post-Meeting Loop**

At your next significant meeting — committee meeting, client call, or internal review — enable transcription and recording before the meeting starts. After the meeting, complete the full post-meeting workflow described in Exercise 2: access Intelligent Recap, verify and export the action items, create a Loop checklist in the relevant Teams channel, assign owners, and send the follow-up email with the Loop component embedded. Time yourself from the end of the meeting to the send of the follow-up email. This workflow, once practiced, should take under 20 minutes. Bring your time to the next session.

**Reflection Prompt — For Your Learning Journal:**

Think about the last time you were underprepared for a high-stakes presentation, or felt that your meeting documentation did not fully capture the commitments made. Write one paragraph describing how the tools and workflows in this chapter would have changed that experience. Be specific — name the Copilot feature, the prompt you would have used, and the measurable outcome you would have achieved differently.

---

```{admonition} Looking Ahead — Chapter 16
:class: tip
Chapter 16 moves into the frontier: Copilot Studio, custom agents, and building bank-specific AI tools that go beyond the standard Microsoft 365 interface. We will build a prototype Helm Bank compliance assistant that can answer policy questions, retrieve documentation, and generate first-draft regulatory responses — all grounded in Helm Bank's own content library. The tools in this chapter were designed by Microsoft. The tools in the next chapter will be designed by you.
```

---

*Chapter 15 | Week 5, Session B | The Essence of AI: A Microsoft Copilot Master Class for Helm Bank*

*© Helm Bank USA Training Program — For internal use only. Not for distribution outside Helm Bank.*
