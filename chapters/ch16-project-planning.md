---
title: "Chapter 16: Week 5, Session C — Project Planning Workshop"
subtitle: "Design Your AI Transformation — From Workflow to Blueprint"
short_title: "Project Planning Workshop"
description: "A structured workshop where Helm Bank professionals select a real workflow to transform, map current and future states, identify Copilot touchpoints, define success metrics, and build a 30-day implementation roadmap."
label: ch-16-project-planning
tags: [project planning, AI transformation, workflow design, implementation roadmap, success metrics, Helm Bank, workshop, hands-on, change management, banking operations]
---

```{admonition} Download this Chapter as PDF
:class: tip
[Download PDF](https://github.com/liquid-books/ai-copilot-helmbank/raw/main/pdfs/ch16-project-planning.pdf)
```

# Chapter 16: Project Planning Workshop

## Design Your AI Transformation — From Workflow to Blueprint

---

> *"A vision without a plan is just a wish. A plan without a vision is just labor. At Helm Bank, we build both."*
>
> — Workshop Opening Principle

---

## Welcome to the Workshop

You have spent four weeks learning what Microsoft Copilot can do. You have seen it summarize documents, draft emails, analyze data, generate presentations, and help navigate complex regulatory language. You have practiced prompts. You have explored use cases. You have started to see the possibilities.

Now it is time to build something real.

This session is different from every other session in this program. There are no lectures. No demonstrations. No watching someone else use the tools. Today, *you* are the architect. You will select a workflow from your actual day-to-day work at Helm Bank, map it end-to-end, identify exactly where and how Copilot can transform it, and leave this room with a formal **AI Project Plan** — a document you could hand to your manager, your team, or the IT department and say: *"This is what I want to build, and here is how we do it."*

This is not a homework assignment. This is your prototype for transformation.

Every participant in this workshop brings something irreplaceable to the table: deep, firsthand knowledge of a real Helm Bank workflow. You know the steps, the shortcuts, the frustrations, the workarounds, and the moments where everything slows to a crawl. That knowledge is the raw material. This chapter provides the structure. What you build today is yours.

---

## Why Planning Before Implementation Matters

Every significant workplace transformation in banking history — from paper ledgers to digital cores, from branch-only to mobile-first — shared one characteristic among successful implementations: deliberate planning before deployment.

The organizations that skipped planning experienced what researchers at McKinsey called the "AI pilot trap": impressive demos that never scaled, enthusiastic early adopters followed by frustrated users, and tools that got blamed for problems that were actually process problems in disguise.

At Helm Bank, we have a particular obligation to get this right. Our clients — Latin American businesses and families who have trusted us as their bridge to the United States financial system since 1989 — depend on consistent, accurate, empathetic service. When we introduce AI into our workflows, we cannot afford haphazard rollouts. We need to be intentional.

**Planning serves four critical functions:**

**1. Clarity** — It forces you to articulate *exactly* what you are trying to improve, not just "make things faster." Vague goals produce vague outcomes. A plan that says "we want to save time on credit reviews" is useless. A plan that says "we want to reduce the time to draft each credit narrative from 90 minutes to 30 minutes by using Copilot to generate a structured first draft from the financial data inputs" is actionable.

**2. Alignment** — A written plan creates shared understanding among everyone involved. When your manager, your colleague, and the compliance officer all read the same document, they see the same future state. Without a plan, each person imagines a different version of "using AI in this workflow," and those divergent visions create confusion and conflict during implementation.

**3. Risk anticipation** — The act of planning surfaces objections, data concerns, and integration challenges *before* they become costly problems. It is far cheaper to identify a risk on paper than to discover it in production. The question "what could go wrong?" is best answered before you launch, not after.

**4. Measurement** — Without pre-defined success metrics, you cannot prove impact. And in banking, if you cannot prove impact, the initiative dies. The people who funded it will not fund the next one. The skeptics will have been proven right. Measurement starts with a baseline taken before the intervention — which means you must define your metrics now.

This workshop will guide you through a structured planning process built specifically for the Helm Bank context. By the end, you will have completed every section of your AI Project Plan.

---

## Workshop Overview and Timeline

This is a structured 180-minute working session. Here is the schedule:

| Time Block | Activity | Duration |
|---|---|---|
| 00:00 – 00:15 | Workflow Selection and Team Formation | 15 min |
| 00:15 – 00:45 | Current State Mapping | 30 min |
| 00:45 – 01:15 | Future State Design and Copilot Touchpoint Identification | 30 min |
| 01:15 – 01:35 | Success Metrics Workshop | 20 min |
| 01:35 – 01:55 | Risk and Resistance Analysis | 20 min |
| 01:55 – 02:30 | 30-Day Implementation Roadmap | 35 min |
| 02:30 – 03:00 | Team Presentations and Peer Feedback | 30 min |

You will work in small teams of 3 to 4 people, ideally with colleagues who share similar workflows or departmental context. Facilitators will circulate throughout to provide guidance, answer questions, and help you push past sticking points.

**What you need:**
- Your AI Project Plan template (provided in this chapter)
- Access to Microsoft Copilot on your Helm Bank device
- Knowledge of at least one workflow from your actual job
- Willingness to think critically and creatively about your work

---

## Section 1: Workflow Selection

Before you can plan an AI transformation, you need to choose *what* to transform. This seems obvious, but teams consistently stumble here. Some pick something too small — trivial gains, no real impact. Others pick something too large — it cannot be meaningfully improved in 30 days. The sweet spot is a workflow that is:

- **Recurring** — It happens regularly (daily, weekly, or monthly), so improvements compound across every future cycle
- **Time-consuming** — It takes meaningful effort, creating a real case for time savings
- **Document or data intensive** — It involves reading, writing, analyzing, or organizing information
- **Currently manual or semi-manual** — There is a human doing cognitive work that Copilot can augment
- **Measurable** — You can quantify either time, quality, or volume before and after

```{admonition} Workflow Categories at Helm Bank
:class: note

**Credit and Lending Operations**
- Monthly credit review compilation and packaging
- Loan modification letter drafting
- Covenant compliance monitoring summaries
- CAMELS scoring documentation and narrative preparation

**Regulatory and Compliance**
- Examiner response package preparation
- SAR narrative drafting and review
- BSA/AML policy review and update cycles
- CRA documentation and reporting packages

**Client Services and Onboarding**
- New client onboarding journey documentation
- KYC/CDD profile assembly and gap analysis
- Account opening communication sequences
- Wire transfer instruction confirmation workflows

**Treasury and Operations**
- Daily liquidity reporting narratives
- Correspondent banking reconciliation summaries
- Internal audit preparation materials
- Board report drafting and quarterly updates

**International Banking and Trade Finance**
- Letter of credit review and response drafting
- SWIFT message interpretation and routing documentation
- Cross-border transaction documentation packages
- Client portfolio update reports for international relationships
```

---

```{admonition} Workshop Exercise 1 — Choose Your Workflow
:class: important

**Time: 15 minutes | Individual brainstorm, then team decision**

**Step 1: Individual Brainstorm (5 minutes)**

On a blank sheet, write down every workflow you perform that involves:
- Reading and synthesizing documents
- Drafting written communications
- Gathering data from multiple sources and compiling it
- Preparing reports or packages for review
- Responding to requests that require research and writing

List at least 5 candidates. Do not filter yet — just list everything that comes to mind.

**Step 2: Score Your Candidates (5 minutes)**

Rate each workflow on the following criteria using a scale of 1 (low) to 3 (high):

| Workflow | Frequency | Time Cost | Document Intensity | Measurability | Total |
|---|---|---|---|---|---|
| [Workflow 1] | /3 | /3 | /3 | /3 | /12 |
| [Workflow 2] | /3 | /3 | /3 | /3 | /12 |
| [Workflow 3] | /3 | /3 | /3 | /3 | /12 |
| [Workflow 4] | /3 | /3 | /3 | /3 | /12 |
| [Workflow 5] | /3 | /3 | /3 | /3 | /12 |

**Step 3: Team Selection (5 minutes)**

Share your top-scoring workflow with your team. As a group, select ONE workflow to focus on for this workshop. You can choose one person's workflow or create a hybrid if multiple people share a similar process.

**Record your selection:**

> **Our chosen workflow:** _______________________________________________
>
> **Department / Function:** _______________________________________________
>
> **How often it occurs:** _______________________________________________
>
> **Who currently performs it:** _______________________________________________
>
> **Why we chose it:** _______________________________________________
```

---

## Section 2: Current State Mapping

You cannot improve what you have not clearly understood. Current state mapping is the discipline of documenting a workflow exactly as it exists today — not as it is supposed to work, not as it worked two years ago, but as it actually happens right now, with all its inefficiencies, workarounds, and human frustrations intact.

This exercise tends to surprise people. When you write it down step by step, you often discover:

- Steps that exist only because "that is how we have always done it"
- Information that is gathered and then never actually used
- Bottlenecks where work piles up waiting for one person's attention
- Handoffs that create lost context and miscommunication between teams
- Duplication — the same data entered into three different systems by three different people

These are your opportunities. These are where Copilot will help.

The goal of current state mapping is not to criticize the people who built the current process. Most workflows evolved organically over years, adapting to changing regulations, personnel, and systems. They made sense when they were created. Current state mapping is about seeing clearly what exists so you can design something better.

```{figure} ../images/ch16-current-state-template.png
:name: current-state-template
:alt: Current State Workflow Mapping Template showing step-by-step documentation structure
:align: center
:width: 90%

**Figure 16.1:** The Current State Mapping Template guides teams through documenting each step of their chosen workflow, capturing time estimates, tools used, pain points, and handoff points. Completed maps typically reveal 3 to 5 major improvement opportunities.
```

---

```{admonition} Workshop Exercise 2 — Map the Current State
:class: important

**Time: 30 minutes | Team activity**

Work together to complete the Current State Workflow Map below. Be specific and honest. This is internal planning — not a performance review. The goal is accuracy, not flattery.

**Part A: Workflow Header**

| Field | Your Answer |
|---|---|
| Workflow Name | |
| Trigger Event (what starts this workflow) | |
| End State (what does "done" look like) | |
| Primary Owner and Performer | |
| Other People Involved | |
| Systems and Tools Currently Used | |
| Total Estimated Time Per Cycle | |
| How Many Times Per Month Does This Run | |
| Total Monthly Hours Consumed (Time x Frequency) | |

**Part B: Step-by-Step Process Map**

For each step in your workflow, complete one row in the table. Aim for 8 to 15 steps. If you have fewer than 6 steps, you are probably combining what are actually multiple steps — break them apart. If you have more than 20, you may be working at too granular a level — group related micro-actions.

| Step # | Step Name | Who Does It | Tools Used | Est. Time | Pain Points and Frustrations |
|---|---|---|---|---|---|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| 6 | | | | | |
| 7 | | | | | |
| 8 | | | | | |
| 9 | | | | | |
| 10 | | | | | |
| 11 | | | | | |
| 12 | | | | | |

**Part C: Current State Pain Point Summary**

After completing your step map, identify your top 3 pain points — the steps or transitions that cause the most friction, delay, or frustration for the people who do this work:

1. **Greatest bottleneck:** _______________________________________________
2. **Most error-prone step:** _______________________________________________
3. **Biggest time sink:** _______________________________________________

**Part D: Stakeholder Impact**

Who is affected when this workflow runs slowly or has errors? Be honest about downstream consequences.

| Stakeholder | How They Are Impacted When This Workflow Breaks Down |
|---|---|
| Internal team doing the work | |
| Other departments that depend on the output | |
| Clients or customers | |
| Regulators or examiners | |
| Senior management | |
```

---

## Section 3: Designing the AI-Augmented Future State

Now comes the creative part. You have documented your current reality. Now you will design a better one — not by replacing your team with robots, but by giving your team an intelligent collaborator that handles the cognitive grunt work so humans can focus on judgment, relationships, and strategy.

The AI-augmented future state is not science fiction. It is a realistic vision of the same workflow with Copilot woven into the right steps. At Helm Bank, Copilot can assist with four fundamental categories of cognitive work:

**Reading and Synthesizing**
Copilot can read long documents, extract key information, compare multiple sources, and produce summaries in seconds. Tasks that took 45 minutes of careful reading can become 5-minute reviews of a Copilot-generated summary, with the human verifying and adjusting rather than doing the initial extraction from scratch. This is transformative for document-heavy banking workflows.

**Drafting and Writing**
Copilot can draft emails, memos, reports, letters, and narratives based on context and prompts. The human role shifts from writer to editor — a much more efficient mode of working. A credit review narrative that took 90 minutes to write from scratch takes 20 minutes when Copilot produces a structured draft that the analyst then refines with their professional judgment.

**Analyzing and Comparing**
Copilot in Excel can analyze data, identify trends, flag anomalies, and generate charts with natural language requests. "Show me the months where fee income dropped more than 10% compared to the prior month and highlight any that coincide with a new regulation taking effect" is a prompt — not an hour of formula work.

**Organizing and Structuring**
Copilot can take unstructured information — meeting notes, email threads, document collections — and impose structure. It can create tables, categorize items, suggest frameworks, and format outputs to match your existing templates. This is particularly powerful for compliance and regulatory workflows where consistent formatting is required.

```{figure} ../images/ch16-copilot-touchpoint-map.png
:name: copilot-touchpoint-map
:alt: Copilot Touchpoint Identification Framework overlaying AI intervention points on workflow steps
:align: center
:width: 90%

**Figure 16.2:** The Copilot Touchpoint Map overlays AI intervention points onto the current state workflow, showing exactly which steps are candidates for Reading and Synthesizing, Drafting and Writing, Analyzing and Comparing, and Organizing and Structuring assistance. Steps marked "Human Only" are those requiring regulatory judgment, client relationship management, or approval authority.
```

---

```{admonition} Workshop Exercise 3 — Design the Future State and Identify Copilot Touchpoints
:class: important

**Time: 30 minutes | Team activity**

**Part A: Future State Vision Statement**

Before diving into step-level detail, write a single paragraph describing what this workflow will look and feel like after Copilot integration. Be specific about outcomes — what will be different for the person doing the work, for the people receiving the output, and for the clients or colleagues downstream.

> **Our Future State Vision:**
>
> _____________________________________________________________
>
> _____________________________________________________________
>
> _____________________________________________________________
>
> _____________________________________________________________

**Part B: Step-by-Step Future State Map**

Return to your current state steps. For each step, decide how its character changes in the future state:

- **Stays the same** — Human does it, no meaningful Copilot involvement
- **Copilot assists** — Human leads; Copilot accelerates or enhances the step
- **Copilot leads** — Copilot does the initial work; human verifies and approves
- **Step eliminated** — Copilot handles the need upstream, making this step unnecessary

| Step # | Current Step Name | Future State Description | Copilot Involvement | Copilot Tool | Est. Time Saved |
|---|---|---|---|---|---|
| 1 | | | None / Assist / Lead / Eliminated | | |
| 2 | | | None / Assist / Lead / Eliminated | | |
| 3 | | | None / Assist / Lead / Eliminated | | |
| 4 | | | None / Assist / Lead / Eliminated | | |
| 5 | | | None / Assist / Lead / Eliminated | | |
| 6 | | | None / Assist / Lead / Eliminated | | |
| 7 | | | None / Assist / Lead / Eliminated | | |
| 8 | | | None / Assist / Lead / Eliminated | | |
| 9 | | | None / Assist / Lead / Eliminated | | |
| 10 | | | None / Assist / Lead / Eliminated | | |

**Copilot Tool Reference for Helm Bank:**
- **Copilot Chat** — Conversational Q&A, document analysis, research, brainstorming
- **Copilot in Word** — Drafting, rewriting, summarizing, reformatting documents
- **Copilot in Excel** — Data analysis, formula assistance, chart generation, trend identification
- **Copilot in Outlook** — Email drafting, thread summarization, scheduling assistance
- **Copilot in Teams** — Meeting summaries, action item extraction, channel search
- **Copilot in PowerPoint** — Presentation creation and design from outlines or documents

**Part C: Copilot Touchpoint Summary**

| Copilot Assistance Category | Steps Where It Applies | Primary Copilot Tool |
|---|---|---|
| Reading and Synthesizing | Steps: | |
| Drafting and Writing | Steps: | |
| Analyzing and Comparing | Steps: | |
| Organizing and Structuring | Steps: | |

**Part D: The Human Roles That Remain and Grow**

This section is critical for stakeholder buy-in. Document what humans will do *better* because of Copilot — not what they will stop doing.

| What Humans Will Focus On More | Why This Matters to Helm Bank and Our Clients |
|---|---|
| | |
| | |
| | |
| | |

**Estimated Total Time Savings Per Cycle:**

> **Current total time per cycle:** _____________________
>
> **Future total time per cycle:** _____________________
>
> **Time saved per cycle:** _____________________
>
> **Monthly time reclaimed (savings x frequency):** _____________________
```

---

## Section 4: Defining Success Metrics

Here is a hard truth about workplace AI initiatives: the ones that fail do not fail because the technology does not work. They fail because no one defined what "working" looked like before the project started.

Six months after launch, when someone asks "is this AI thing actually helping?" and no one can answer with data, the initiative quietly dies. The funding goes elsewhere. The champion moves on. The tool gets used by fewer and fewer people until it disappears entirely.

At Helm Bank, we measure success in three dimensions:

**Efficiency Metrics** — Did we save time? Did we process more volume with the same team? Did cycle times shrink? These are the easiest metrics to collect and the most persuasive for leadership.

**Quality Metrics** — Did error rates go down? Did output consistency improve? Did the number of revision cycles decrease? These metrics matter enormously in a regulated banking environment where accuracy is not optional.

**Experience Metrics** — Do employees feel less stressed about this workflow? Are clients receiving faster, clearer responses? Is the team more confident in the accuracy of their work? These are the metrics that determine whether the change sticks long-term.

A strong AI Project Plan includes metrics in all three categories, with baseline measurements (what it is today) and target measurements (what we want it to be in 30 and 90 days).

```{admonition} Measurement Principle for Banking Operations
:class: note

In regulated banking environments, quality metrics often matter more than efficiency metrics. A 30% time savings that comes with a 5% increase in errors is not a win — it is a liability exposure. Design your metrics to capture both sides of the equation. Speed without accuracy is dangerous. Accuracy without speed is unsustainable. The goal is genuinely both — and Copilot, when implemented thoughtfully, can deliver both simultaneously.
```

---

```{admonition} Workshop Exercise 4 — Define Your Success Metrics
:class: important

**Time: 20 minutes | Team activity**

**Part A: Baseline Measurement**

Before you can measure improvement, you need to know where you start. For each metric type, document your current baseline. If you do not have exact numbers, estimate and note clearly that it is an estimate. Estimates are acceptable for planning purposes — precise baselines should be collected during Phase 1 of your implementation.

| Metric Category | Specific Metric | Current Baseline | How You Will Measure It |
|---|---|---|---|
| Efficiency | Time per workflow cycle | | |
| Efficiency | Number of cycles per month | | |
| Efficiency | Total team hours consumed monthly | | |
| Efficiency | Time from trigger event to completion | | |
| Quality | Error rate or revision rate per cycle | | |
| Quality | Number of review and approval rounds | | |
| Quality | Compliance issue frequency | | |
| Experience | Team satisfaction with this workflow (1 to 10) | | |
| Experience | Client response time (if applicable) | | |
| Experience | Escalations or rework incidents per month | | |

**Part B: Target Setting**

For each core metric, set a 30-day and 90-day target. Be ambitious but realistic. A 10 to 25 percent improvement in 30 days is achievable with disciplined implementation. A 70 percent improvement in 30 days is not — and claiming it will undermine your credibility with stakeholders.

| Metric | Current Baseline | 30-Day Target | 90-Day Target |
|---|---|---|---|
| Time per cycle | | | |
| Total monthly hours consumed | | | |
| Error or revision rate | | | |
| Team satisfaction score | | | |
| Your custom metric 1 | | | |
| Your custom metric 2 | | | |

**Part C: Your Primary Success Statement**

Write one sentence that captures what success looks like for this project. This is your north star — the sentence you read aloud when you are tired and wondering if it is worth continuing.

> **Success looks like:** _____________________________________________
> by [date], as measured by _________________________________________.

**Part D: Early Win Indicator**

What is the first signal — within the first 5 to 7 days — that tells your team this approach is working? Early wins are critical for momentum. Name something observable, not theoretical.

> **We will know it is working when:** ___________________________________
```

---

## Section 5: Anticipating Resistance and Risk

No transformation succeeds without addressing the human dimension. Technology adoption in banking faces two types of resistance that must be anticipated and planned for, because the ones you do not anticipate are the ones that derail your project.

**Rational Resistance** arises from legitimate concerns: "What if Copilot makes an error in the credit narrative and we do not catch it?" "What data is Copilot sending to Microsoft's servers?" "Is this compliant with our data retention and privacy policies?" These concerns deserve serious, specific answers — not dismissal. A plan that cannot address rational concerns will not survive its first compliance review.

**Emotional Resistance** arises from fear and uncertainty: "Is this going to replace my job?" "I have done this workflow for 12 years — are they saying I have been doing it wrong?" "What if I cannot learn the new way fast enough?" These concerns deserve empathy and honest communication — not empty reassurance or corporate enthusiasm that ignores the real anxiety underneath.

At Helm Bank, our values of Empathy and Curiosity guide how we navigate these conversations. We acknowledge real concerns. We answer them honestly. We invite skeptics to be co-designers of the solution rather than passive recipients of a change handed down to them. The difference between a skeptic and a champion is often just one good conversation.

```{figure} ../images/ch16-risk-matrix.png
:name: risk-matrix
:alt: Risk Assessment Matrix mapping risks by Likelihood and Impact with mitigation priorities
:align: center
:width: 85%

**Figure 16.3:** The Risk Assessment Matrix maps identified risks by Likelihood (horizontal axis) and Impact (vertical axis). Risks in the upper-right quadrant — High Likelihood, High Impact — require formal mitigation plans. Risks in the lower-left can be monitored without active intervention. Teams use this framework to prioritize where planning energy should be focused.
```

---

```{admonition} Workshop Exercise 5 — Risk and Resistance Analysis
:class: important

**Time: 20 minutes | Team activity**

**Part A: Risk Identification**

Brainstorm everything that could go wrong with this implementation. Include technical risks, compliance risks, people risks, and process risks. List at least 8 risks without filtering. Brainstorm first, evaluate second.

| # | Risk Description | Type | Likelihood (H/M/L) | Impact (H/M/L) |
|---|---|---|---|---|
| 1 | | Technical / Compliance / People / Process | | |
| 2 | | Technical / Compliance / People / Process | | |
| 3 | | Technical / Compliance / People / Process | | |
| 4 | | Technical / Compliance / People / Process | | |
| 5 | | Technical / Compliance / People / Process | | |
| 6 | | Technical / Compliance / People / Process | | |
| 7 | | Technical / Compliance / People / Process | | |
| 8 | | Technical / Compliance / People / Process | | |

**Part B: Priority Risk Mitigation Plans**

For your top 3 highest-priority risks (High Likelihood combined with High or Medium Impact), develop a specific mitigation plan. Vague mitigations like "be careful" are not acceptable. Specific mitigations like "require a second analyst to verify all financial ratios extracted by Copilot before the package is submitted" are what we are building.

**Risk 1:**

| Field | Your Detail |
|---|---|
| Risk Description | |
| Why This Could Happen | |
| Mitigation Strategy | |
| Mitigation Owner | |
| Early Warning Sign to Watch For | |

**Risk 2:**

| Field | Your Detail |
|---|---|
| Risk Description | |
| Why This Could Happen | |
| Mitigation Strategy | |
| Mitigation Owner | |
| Early Warning Sign to Watch For | |

**Risk 3:**

| Field | Your Detail |
|---|---|
| Risk Description | |
| Why This Could Happen | |
| Mitigation Strategy | |
| Mitigation Owner | |
| Early Warning Sign to Watch For | |

**Part C: Stakeholder Resistance Map**

| Stakeholder Group | Likely Concern or Resistance | How You Will Address It | Who Has This Conversation |
|---|---|---|---|
| Direct colleagues on the team | | | |
| Department manager | | | |
| Compliance and Legal | | | |
| IT and Technology | | | |
| Senior leadership | | | |
| Clients (if applicable) | | | |

**Part D: Change Champion Strategy**

Identify one person outside your immediate team who would be a powerful advocate for this project. This should be someone who is respected across the organization, has used Copilot successfully, and can speak credibly to skeptics without sounding like a vendor pitch.

> **Our Change Champion:** _______________________________________________
>
> **Why they are the right person:** _______________________________________________
>
> **How and when we will engage them:** _______________________________________________
```

---

## Section 6: The 30-Day Implementation Roadmap

A plan without a timeline is a wish list. Your 30-day roadmap transforms the AI Project Plan from a document into a commitment. It answers the question every stakeholder will ask: *"So what exactly is happening and when?"*

The 30-day roadmap for a Copilot workflow transformation follows a proven three-phase arc:

**Phase 1 — Prepare (Days 1 to 7)**
Lay the groundwork before any live implementation. Confirm access, document current state baselines, align stakeholders, develop your initial prompt library, and run a first dry-run with Copilot on a non-critical sample of the workflow. The goal of Phase 1 is to arrive at Day 8 with everything you need to run a clean pilot.

**Phase 2 — Pilot (Days 8 to 21)**
Run the AI-augmented workflow in parallel with your existing process. Both methods produce output for the same work items. You compare quality, time, and experience. You refine your prompts based on what you learn. You collect feedback from everyone involved. You identify what works and what needs adjustment. The goal of Phase 2 is to arrive at Day 22 with evidence and confidence to commit to the new approach.

**Phase 3 — Integrate (Days 22 to 30)**
Transition the workflow to the AI-augmented version as the primary method. Document the new process officially. Train any team members not yet proficient in the new workflow. Measure your success metrics against the baseline. Prepare a short results summary. The goal of Phase 3 is to arrive at Day 30 with a documented, measured, and adopted new workflow — and a story you can tell to the rest of the organization.

```{figure} ../images/ch16-30day-roadmap.png
:name: 30day-roadmap
:alt: 30-Day Implementation Roadmap showing the Prepare Pilot Integrate arc with weekly task assignments
:align: center
:width: 95%

**Figure 16.4:** The 30-Day Implementation Roadmap shows the three-phase arc (Prepare / Pilot / Integrate) with specific task assignments across four weeks. The parallel workflow structure in Phase 2 is essential — it allows direct comparison between old and new methods without operational risk, and gives the team confidence before fully committing to the AI-augmented process.
```

---

```{admonition} Workshop Exercise 6 — Build Your 30-Day Roadmap
:class: important

**Time: 35 minutes | Team activity**

Using the phase structure below, assign specific tasks to specific people with specific dates. Vague tasks like "learn Copilot" are not acceptable. Specific tasks like "Draft the first credit summary narrative using Copilot, compare output to last month's human-written version, and document time differences" are what we are building. Every task needs an owner and a clear done-when criterion.

---

**PHASE 1: PREPARE (Days 1 to 7)**

| Day | Task Description | Owner | Done When |
|---|---|---|---|
| 1 to 2 | Confirm Microsoft 365 Copilot access for all team members | | All team members can open Copilot Chat on their Helm Bank device |
| 1 to 2 | Document current state baseline metrics: time per cycle, frequency, error rate | | Baseline numbers recorded in writing and agreed upon by team |
| 3 | Review Copilot data security and compliance guidelines with IT | | Written confirmation received that workflow data can be processed through Copilot |
| 3 to 4 | Develop initial prompt library: write and test at least 5 prompts specific to this workflow | | Prompts tested on real examples and documented with output quality notes |
| 5 | Brief manager and key stakeholders on the plan | | Manager has reviewed the plan and provided approval to proceed |
| 6 to 7 | Dry run: apply Copilot to one sample item from last month's workflow using your prompts | | Sample output reviewed, time documented, quality assessed |
| [Custom] | | | |
| [Custom] | | | |

**Phase 1 Milestone:** By the end of Day 7, we will have _______________________________________________ completed and be ready to begin parallel workflow.

---

**PHASE 2: PILOT (Days 8 to 21)**

| Day | Task Description | Owner | Done When |
|---|---|---|---|
| 8 | Launch parallel workflow: run AI-augmented and traditional methods side by side on the same work items | | First parallel cycle started; both methods producing output |
| 8 to 14 | Track time for each step in both versions using a simple log | | Time log complete for first full cycle with both methods documented |
| 10 | Team check-in: what prompts are working, what needs refinement, what was unexpected | | Updated prompt library documented with revisions |
| 14 | Mid-pilot review: compare quality of AI-assisted vs. traditional outputs | | Comparison documented with specific examples |
| 14 | Informal update to manager: 5-minute briefing on mid-pilot findings | | Manager briefed; any concerns or direction noted |
| 15 to 21 | Continue parallel workflow with refined prompts | | Second full cycle completed; time and quality data collected |
| 18 | Gather team feedback: brief structured conversation or short written survey | | Feedback documented from all team members |
| 21 | Pilot complete: compile all time, quality, and experience data | | Phase 2 summary memo drafted |
| [Custom] | | | |
| [Custom] | | | |

**Phase 2 Milestone:** By the end of Day 21, we will have documented evidence that _______________________________________________ and will be confident to transition to the AI-augmented method.

---

**PHASE 3: INTEGRATE (Days 22 to 30)**

| Day | Task Description | Owner | Done When |
|---|---|---|---|
| 22 | Transition: AI-augmented version becomes the primary method going forward | | Team agreement reached; old method retired for routine use |
| 22 to 24 | Document the new workflow officially: updated process map, prompt library, and guidelines | | Process document created and stored in team SharePoint |
| 23 | Train any team members not yet fully proficient in the new workflow | | All team members can execute the new process independently |
| 25 | Measure 30-day metrics against the pre-project baseline | | Metrics comparison table completed |
| 26 | Draft the 30-Day Results Summary in one-page format | | Results summary draft complete |
| 27 | Review results summary with manager and incorporate feedback | | Manager has reviewed and signed off |
| 28 to 29 | Final adjustments; polish the results summary for presentation | | Final version ready |
| 30 | Present results to department or senior leadership | | Presentation delivered; next steps agreed upon |
| [Custom] | | | |

**Phase 3 Milestone:** By Day 30, we will have presented _______________________________________________ with measured evidence and a recommendation for broader adoption.

---

**Roadmap Summary Box:**

> **Project Name:** _______________________________________________
>
> **Project Start Date:** _______________________________________________
>
> **Project Lead:** _______________________________________________
>
> **Team Members:** _______________________________________________
>
> **Manager / Executive Sponsor:** _______________________________________________
>
> **30-Day Goal (one sentence):** _______________________________________________
>
> **Scheduled Phase 1 Start:** _______________________________________________
>
> **Scheduled Pilot Launch:** _______________________________________________
>
> **Scheduled Integration Date:** _______________________________________________
>
> **Results Presentation Date:** _______________________________________________
```

---

## Three Worked Examples: Completed AI Project Plans

To help ground the template in Helm Bank's real operational context, here are three fully worked examples from different departments. These represent the kinds of projects that previous participants in this program have developed and implemented. Read through the example that is most relevant to your own workflow — it will help you see how abstract planning concepts translate into specific, actionable plans.

---

### Worked Example A: Monthly Credit Review Compilation

**Department:** Commercial Lending

**Workflow Selected:** Monthly credit review package assembly for the portfolio review committee

---

**Current State Summary**

Every month, the commercial lending analyst team spends approximately 18 hours per analyst assembling the monthly credit review packages for committee presentation. Each package requires: pulling the borrower's financial statements from the core banking system, downloading covenant compliance data from individual Excel trackers, reviewing the loan officer's relationship notes in Teams, cross-referencing the prior month's credit review narrative, and writing a 2 to 4 page narrative summarizing the borrower's financial health, covenant status, and any material changes since the prior review.

For a portfolio of 20 active credits, this consumes approximately 360 analyst-hours per month across the team. The most painful step is the narrative drafting — analysts describe it as "staring at a blank page with five browser tabs open, trying to synthesize everything into something coherent and well-written."

**Future State Vision**

Analysts use Copilot in Word to read and synthesize the financial statements and prior narratives, generating a structured first draft of each narrative. Copilot in Excel handles the covenant compliance comparison automatically. The analyst's role shifts from primary writer to expert reviewer — verifying Copilot's synthesis, adding qualitative judgment about relationship dynamics, and ensuring regulatory accuracy. Target: reduce total monthly team hours from 360 to under 180 while improving narrative consistency across the portfolio.

**Copilot Touchpoints**

| Step | Current Activity | Future State with Copilot | Tool |
|---|---|---|---|
| Financial statement pull | Manual extraction from core system and PDF organization | No change — data access not yet integrated | — |
| Covenant compliance check | Analyst manually compares actual ratios vs. covenant thresholds | Copilot in Excel: compare current ratios vs. covenants; flag breaches automatically | Excel |
| Prior review comparison | Analyst reads prior month's 3-page document manually | Copilot in Word: summarize prior narrative; highlight what has changed | Word |
| Relationship notes synthesis | Analyst reads Teams messages and call log entries | Copilot in Teams: extract key loan officer observations from channel history | Teams |
| Narrative first draft | Analyst writes full narrative from scratch over 60 to 90 minutes | Copilot in Word: generate structured draft from synthesized inputs using structured prompt | Word |
| Analyst review and edit | Analyst reads and heavily edits own draft | Human judgment role: verify accuracy, add relationship color, adjust tone | Human |
| Manager review package | Manager reads full narrative set before committee | Copilot in Outlook: summarize flagged items for manager attention with links to source | Outlook |

**Success Metrics**

| Metric | Current Baseline | 30-Day Target | 90-Day Target |
|---|---|---|---|
| Hours per credit review package | 18 hours | 9 hours | 7 hours |
| Total monthly team hours | 360 hours | 180 hours | 140 hours |
| Narrative revision rounds (manager feedback) | 2.3 rounds average | 1.5 rounds | 1.0 rounds |
| Analyst workflow satisfaction score | 4.2 out of 10 | 7.0 out of 10 | 8.0 out of 10 |
| Covenant compliance errors missed | 1.8 per month | 0.5 per month | 0 per month |

**Primary Risk and Mitigation**

*Risk:* Copilot misinterprets a financial ratio or covenant threshold, leading to an inaccurate narrative that passes manager review without correction.

*Mitigation:* All Copilot-generated financial data must be verified against source documents before submission. A two-item verification checklist is added to the review step: (1) confirm every ratio in the narrative against the statement, (2) confirm every covenant status against the tracker. This step adds 10 minutes per package but eliminates the risk category entirely.

**30-Day Results (Retrospective)**

In the first full month of implementation, the team reduced per-package time from 18 hours to 11 hours — a 39% reduction in the first cycle, before prompts were fully optimized. Manager revision rounds dropped from 2.3 to 1.4. Analyst satisfaction jumped from 4.2 to 6.8. Three analysts described the new workflow as "actually enjoyable" for the first time in their experience with credit reviews.

---

### Worked Example B: Examiner Response Package Preparation

**Department:** Compliance and Risk Management

**Workflow Selected:** Federal bank examiner information request response package assembly

---

**Current State Summary**

When federal examiners issue an information request during an examination, the compliance team must assemble responsive documentation, draft cover letters, prepare document indexes, and ensure every item is traceable to a specific numbered examiner request. This process currently takes 3 to 5 business days per request cycle, involves 4 compliance team members, and creates significant stress due to regulatory time pressure.

Much of the time is spent searching for existing policies across multiple SharePoint libraries, reformatting documents to match examiner presentation preferences, and drafting cover letter and index language from scratch each cycle. The team also struggles with gap identification — ensuring that everything the examiner asked for has actually been included before the package goes out.

**Future State Vision**

Copilot serves as the compliance team's research and writing assistant throughout the examiner response cycle. It parses the examiner request into a structured checklist, searches SharePoint for relevant policies, drafts cover letters using approved templates and current request details, generates the document index from the file list, and identifies gaps before submission. Target: reduce response cycle from 5 days to 2.5 days and eliminate index errors entirely.

**Copilot Touchpoints**

| Step | Future State with Copilot | Estimated Time Saved per Cycle |
|---|---|---|
| Parse examiner request | Copilot in Word reads the request, extracts numbered items into a structured checklist with tracking table | 45 minutes |
| Policy document search | Copilot Chat searches SharePoint for relevant policies using natural language queries for each checklist item | 2 hours |
| Gap identification | Copilot compares gathered documents against the checklist and flags any missing or incomplete items | 1 hour |
| Cover letter drafting | Copilot in Word drafts cover letter using the prior quarter's template and the current request specifics | 1.5 hours |
| Document index creation | Copilot in Word generates the index table automatically from the document list and examiner request numbers | 2 hours |
| Internal review memo | Copilot in Teams summarizes what was submitted, why, and what was excluded with rationale | 30 minutes |

**Total estimated time savings per cycle: 7 hours 45 minutes, reducing a 5-day cycle to under 3 days.**

**Success Metrics**

| Metric | Current Baseline | 30-Day Target | 90-Day Target |
|---|---|---|---|
| Business days per response cycle | 5 days | 2.5 days | 2 days |
| Team members required per cycle | 4 | 3 | 3 |
| Cover letter revision rounds | 3 rounds | 1 round | 1 round |
| Index errors found post-submission | 2.1 per cycle | 0 | 0 |
| Compliance team stress rating during exams | 8.5 out of 10 | 5.0 out of 10 | 4.0 out of 10 |

**Primary Risk and Mitigation**

*Risk:* Confidential examiner communication or sensitive client data is inadvertently processed through Copilot in ways that create data protection or privilege concerns.

*Mitigation:* Before launch, IT confirms in writing that Microsoft 365 Copilot operating within the Helm Bank enterprise tenant does not retain or train on prompt content. The team reviews Microsoft's Data Protection Addendum. Any documents marked Privileged and Confidential are excluded from Copilot processing and handled manually. This policy is documented and included in the new process guidelines.

---

### Worked Example C: New International Client Onboarding Journey

**Department:** Client Services and International Banking

**Workflow Selected:** New international client onboarding — document collection, KYC file assembly, and welcome communication sequence

---

**Current State Summary**

Helm Bank's international client onboarding process spans 3 to 6 weeks from initial inquiry to account activation. The process involves collecting 12 to 18 distinct documents (passports, corporate formation documents, source-of-funds declarations, beneficial ownership certifications, and more), assembling a complete KYC and CDD file, submitting for BSA officer review, receiving conditional approval, collecting any additional documentation requested, and finally activating the account and sending welcome communications.

Currently, 40% of new onboarding cases experience at least one delay caused by missing documents, miscommunications about requirements, or bottlenecks at the BSA review step. Each case requires an average of 7.2 hours of staff time spread across relationship managers, analysts, and compliance officers. Client satisfaction scores at the conclusion of onboarding average 6.8 out of 10 — far below Helm Bank's service standard.

**Future State Vision**

Copilot assists at every communication and documentation assembly point in the onboarding journey. It drafts the initial document request email customized to the client's type and country of origin (in both English and Spanish where appropriate), flags missing documents from the KYC checklist before the file reaches the BSA officer, summarizes the completed file for efficient BSA review, and generates the personalized welcome letter. Relationship managers remain the face of the relationship — warm, empathetic, and culturally attuned. Copilot handles the paperwork orchestration behind the scenes so relationship managers spend their time on the relationship, not the administration.

**Copilot Touchpoints**

| Onboarding Stage | Copilot Role | Tool | Human Role |
|---|---|---|---|
| Initial inquiry response | Draft personalized bilingual response introducing next steps | Copilot in Outlook | RM reviews, personalizes, sends within 2 hours |
| Document request letter | Generate customized checklist based on client entity type and country | Copilot in Word | Compliance reviews; RM sends with warm cover note |
| Document receipt tracking | Log received documents against checklist; flag remaining gaps | Copilot in Word | Analyst confirms completeness; follows up on gaps |
| KYC file assembly | Organize and categorize received documents; create structured cover sheet | Copilot in Word | Analyst verifies categorization and completeness |
| BSA officer review brief | Summarize client profile, risk factors, and document package in one page | Copilot in Word | BSA officer reviews summary; conducts deeper review where flagged |
| Conditional approval follow-up | Draft request for any additional items required by BSA review | Copilot in Outlook | RM reviews for tone and relationship sensitivity; sends |
| Account activation | Draft personalized welcome letter with account details and next steps | Copilot in Word | RM signs, personalizes with personal note, sends |
| 30-day relationship check-in | Draft relationship check-in email referencing onboarding topics | Copilot in Outlook | RM personalizes and sends |

**Success Metrics**

| Metric | Current Baseline | 30-Day Target | 90-Day Target |
|---|---|---|---|
| Average onboarding cycle time | 26 calendar days | 18 days | 14 days |
| Cases with at least one significant delay | 40% | 20% | 10% |
| Staff hours per onboarding case | 7.2 hours | 4.5 hours | 3.5 hours |
| Client satisfaction score at onboarding completion | 6.8 out of 10 | 8.5 out of 10 | 9.0 out of 10 |
| Document gaps not caught until BSA review | 2.3 per case average | 0.5 per case | 0 per case |

**Primary Risk and Mitigation**

*Risk:* Copilot-generated client communications contain inaccurate account details, incorrect regulatory language, or culturally inappropriate phrasing for Latin American clients.

*Mitigation:* All client-facing communications require mandatory human review before sending — this is a non-negotiable step in the new workflow. Template language is pre-approved by Legal and Compliance and used as the foundation for all Copilot drafts. Spanish-language outputs are reviewed by a native Spanish speaker before sending. The relationship manager's review step includes a specific checklist item for cultural appropriateness.

---

## Peer Review and Feedback Round

Once teams have completed their AI Project Plans, the workshop closes with a structured peer feedback session. Each team presents their plan in 5 minutes and receives 5 minutes of structured feedback from the full group. This is not a critique — it is a stress test. A plan that survives peer feedback is a plan that will survive the stakeholder conversation.

```{admonition} Peer Feedback Framework — STAR Method
:class: note

When giving feedback on another team's AI Project Plan, use this structured approach:

**S — Strength:** What is particularly strong, specific, or smart about this plan? Name it precisely.

**T — Tension:** Where do you see an unresolved conflict, assumption that has not been tested, or two parts of the plan that seem to pull in different directions?

**A — Addition:** What important element is missing, underdeveloped, or deserves more specific treatment?

**R — Reality-check:** Does the 30-day timeline feel achievable given this team's workload and the complexity of the workflow? What might cause it to slip?

Avoid vague feedback. "This looks good" is not useful. "Your risk mitigation plan for data privacy needs to name the specific Microsoft data protection clauses you are relying on — 'we checked with IT' is not sufficient for a compliance audience" is useful.
```

---

```{admonition} Workshop Exercise 7 — Team Presentation and Peer Feedback
:class: important

**Time: 30 minutes total (5 minutes presenting, 5 minutes receiving feedback, per team)**

**Your presentation must cover these five elements:**

1. **The workflow you chose and why it matters** (60 seconds) — What is the problem this workflow has right now, and why does solving it matter to Helm Bank?

2. **The most significant pain point in the current state** (30 seconds) — One specific, honest observation about what is broken or inefficient today.

3. **The most impactful Copilot touchpoint in your future state** (60 seconds) — Which single step will Copilot transform most dramatically, and how?

4. **Your primary success metric and your 30-day target** (30 seconds) — One number. What does success look like?

5. **The risk you are most concerned about and your mitigation plan** (60 seconds) — Do not hide it. Name your scariest risk and explain exactly how you will prevent or respond to it.

**Listening protocol during feedback:**
Do not defend your plan while feedback is being given. Take notes. Ask clarifying questions only. Defend nothing.

**Post-feedback team reflection:**

> **One concrete change we will make based on feedback:** _______________________________________________
>
> **One element we are keeping despite any pushback:** _______________________________________________
>
> **One thing we wish we had thought of before today:** _______________________________________________
```

---

## Before You Leave: Three Commitments

Your AI Project Plan is not a class assignment. It is a real plan for a real improvement at Helm Bank. Before you leave this session, make three concrete commitments. Write them down. Share them with your manager this week.

**Commitment 1: Start Date**

When will you begin Phase 1 of your 30-day roadmap? Not "soon." Not "after things settle down." A specific calendar date.

> **Our Phase 1 start date:** _______________________________________________

**Commitment 2: Manager Conversation**

When will you brief your manager on this plan? This conversation is required to gain the visibility, support, and resources your project needs to succeed.

> **Manager briefing scheduled for:** _______________________________________________
>
> **Who is leading this conversation:** _______________________________________________

**Commitment 3: Day 21 Check-In**

Before you leave the pilot phase and commit to full integration, your team must formally assess progress. Schedule this now.

> **Day 21 pilot review meeting scheduled for:** _______________________________________________
>
> **Who will attend:** _______________________________________________

---

## Chapter Summary

This workshop chapter marked the turning point in the Helm Bank Microsoft Copilot Master Class. You moved from learning about AI capabilities to building with them — selecting a real workflow from your actual job, mapping its current state with honest precision, designing an AI-augmented future state with specific Copilot touchpoints, defining measurable success criteria before implementation begins, anticipating resistance and risks with specific mitigation plans, and creating a week-by-week implementation roadmap with named owners and clear done-when criteria.

The three worked examples — Monthly Credit Review Compilation, Examiner Response Package Preparation, and New International Client Onboarding — demonstrated how these planning frameworks apply across Helm Bank's diverse operational landscape. Each example showed that AI transformation is not about eliminating human roles; it is about elevating human roles. When Copilot handles the cognitive drudgery, banking professionals can focus on what only humans can do: judgment, empathy, relationships, and the kind of contextual wisdom that no language model can replicate.

```{admonition} Key Takeaways from Chapter 16
:class: important

**1. Planning before implementation is not optional in banking.**
The cost of unplanned AI rollouts — in errors, compliance exposure, and lost trust — exceeds the cost of deliberate planning by orders of magnitude. Every hour spent planning today prevents ten hours of problem-solving tomorrow.

**2. Current state mapping requires radical honesty.**
The inefficiencies you document are your opportunities. Do not sanitize the current state to protect anyone's feelings. The more clearly you see what is broken, the more precisely you can design what is better.

**3. Copilot is an augmenter, not a replacer.**
Every strong AI Project Plan identifies what humans will do more of — and better — because Copilot handles the routine cognitive load. This framing is not just ethically important; it is strategically necessary for stakeholder buy-in.

**4. Metrics must be defined before implementation begins.**
You cannot prove impact if you did not measure the baseline. Collect your baseline numbers this week, before you touch Copilot in your workflow. This is non-negotiable.

**5. Resistance is information, not obstruction.**
The concerns your colleagues raise often reveal real risks in your plan. Listen carefully and respond specifically. The colleague who asks "what if Copilot gets the covenant ratio wrong?" is not being difficult — they are being thorough. Reward that.

**6. Thirty days is enough to prove the concept.**
You do not need six months and a major IT initiative to demonstrate that Copilot improves a workflow. A disciplined 30-day pilot with clear baselines and honest measurement is sufficient to make the case for broader adoption — and to build the organizational confidence to scale.
```

---

## Instructions for Next Session

**Session 17: Week 6, Session A — Results Showcase and Program Graduation**

In our next and final session, teams will present the early results of their AI Project Plans. This is not a status update — it is a showcase of what this cohort has built together.

**Your presentation will include:**

1. **The workflow you chose** and its significance to Helm Bank's operations
2. **What you learned in Phase 1** — what surprised you about planning versus doing
3. **Early metrics from your pilot** — even if preliminary, present what you have collected
4. **One moment where Copilot exceeded your expectations** — a specific example with before and after
5. **One moment where Copilot fell short** — what happened, how you adjusted, what you learned
6. **Your recommendation** for whether and how Helm Bank should scale this approach beyond your team

**Before Session 17, complete the following:**

- [ ] Begin Phase 1 (Prepare) activities — access confirmed, baseline measured, prompts drafted
- [ ] Run your dry-run sample and document the output quality
- [ ] Brief your manager on the plan and note their feedback
- [ ] Start Phase 2 (Pilot) parallel workflow if your timeline permits
- [ ] Collect time data for at least one cycle of the current state before Copilot
- [ ] Complete a team reflection: what are you most excited about? Most uncertain about?
- [ ] Build a 5-slide presentation using Copilot in PowerPoint — practice what you have learned

**Presentation format for Session 17:**
- 8 to 10 minutes per team
- Slides strongly encouraged — and use Copilot to build them
- Be honest about what has not worked yet. The teams that share their real struggles — and how they overcame them — will provide more value to their colleagues than the teams that present only polished success

This final session is a celebration of what this cohort has built and a launching pad for Helm Bank's broader AI transformation journey. Come prepared to share, to learn, and to inspire the colleagues who will follow in your path.

---

```{admonition} A Final Word from Your Workshop Facilitator
:class: tip

The workflow you chose today — the one you mapped, designed, measured, and planned — might seem like a small thing. One process. Maybe 18 hours a month. Maybe 5 business days per cycle. Maybe 40 onboarding cases a year.

But consider what it means at scale. If every professional who completed this program applies one workflow transformation, and if those transformations compound across the organization over time, what does Helm Bank look like in two years?

Analysts spending their time on relationship intelligence instead of narrative assembly. Compliance officers preparing for examinations instead of assembling binders. Relationship managers calling clients on day three of onboarding instead of day fifteen.

That is the vision. Your plan is one thread in that fabric.

Helm Bank was founded on the belief that international banking deserves the same quality and care as any other. Your AI project — however modest it might feel today — is an expression of that same belief: that our clients and our colleagues deserve our best thinking, not our most exhausted assembly-line labor.

Start Monday. Start well. We will see you at the showcase.
```

---

*End of Chapter 16 — Project Planning Workshop*

---

**Chapter 16 Quick Reference — AI Project Plan Completion Checklist**

Before leaving today's session, confirm your plan is complete:

- [ ] Workflow selected with clear trigger event and end state defined
- [ ] Current state mapped: all steps with owners, tools, time estimates, and pain points
- [ ] Future state designed: each step updated with Copilot role and specific tool
- [ ] Future state vision statement written in plain language
- [ ] Total time savings estimated per cycle and per month
- [ ] Efficiency, quality, and experience metrics defined
- [ ] Current baselines documented (or marked for collection in Phase 1)
- [ ] 30-day and 90-day targets set for each metric
- [ ] Primary success statement written in one clear sentence
- [ ] Early win indicator identified
- [ ] At least 8 risks identified and categorized by type
- [ ] Top 3 risks have specific mitigation plans with named owners
- [ ] Stakeholder resistance map complete with response strategies
- [ ] Change champion identified and engagement plan drafted
- [ ] Phase 1 tasks assigned with owners and done-when criteria
- [ ] Phase 2 tasks assigned with owners and done-when criteria
- [ ] Phase 3 tasks assigned with owners and done-when criteria
- [ ] Phase 1, 2, and 3 milestones clearly defined
- [ ] Phase 1 start date committed and written down
- [ ] Manager briefing scheduled
- [ ] Day 21 team check-in scheduled
- [ ] Peer feedback received and one concrete change identified

**If every box is checked, your plan is ready. If not — stay, finish, and leave with a complete document. This is the most important work you will do in this program.**
