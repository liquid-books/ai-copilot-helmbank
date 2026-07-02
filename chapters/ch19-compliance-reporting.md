---
title: "Chapter 19: Week 6, Session C — Copilot for Compliance & Reporting"
subtitle: "AI in the Most Regulated Room in the Bank"
short_title: "Copilot for Compliance"
description: "How Helm Bank compliance professionals use Microsoft Copilot for BSA/AML documentation, SAR drafting, OFAC workflow support, exam preparation, regulatory tracking, and board reporting — with a rigorous human-in-the-loop framework and the verification discipline applied to every compliance output."
label: ch-19-compliance-reporting
tags: [compliance, BSA, AML, SAR, OFAC, regulatory, exam preparation, board reporting, human-in-the-loop, Microsoft 365, Helm Bank, banking compliance, FinCEN, OCC, FDIC, audit]
---

```{admonition} Download this Chapter as PDF
:class: tip
[Download PDF](https://github.com/liquid-books/ai-copilot-helmbank/raw/main/pdfs/ch19-compliance-reporting.pdf)
```

# Chapter 19: Copilot for Compliance & Reporting

## The Weight of the Room

It is 4:47 PM on a Thursday in Helm Bank's Brickell Avenue compliance suite. Carolina Vasquez, BSA Officer, has been at her desk since 7:00 AM. On her left monitor: a transaction monitoring alert queue with forty-one items that need disposition before the weekend. On her right monitor: a draft Suspicious Activity Report that has been open since Tuesday, its narrative section still reading *[TO BE COMPLETED]*. Tomorrow at 9:00 AM, the OCC examination team arrives for a two-day review of the bank's BSA/AML program. The examiner's information request list runs to sixty-three line items.

Carolina is not panicking. She has been doing this for eleven years, four of them at Helm Bank, and she knows that compliance work is ultimately about precision and documentation, not speed. But she also knows that the margin for error in this room is approximately zero. A SAR filed with a factual error is a problem. A SAR filed late is a worse problem. A SAR not filed at all, when one should have been, is a federal issue. An exam package delivered with gaps or inconsistencies is an invitation for findings.

She opens Copilot in Microsoft 365.

Not to let AI make decisions. Carolina would no sooner delegate a compliance judgment to an AI than she would ask it to sign the SAR on her behalf. But she knows, from six months of disciplined practice, exactly what Copilot can and cannot do in this environment. And right now, at 4:47 PM on the Thursday before an OCC exam, what it *can* do is exactly what she needs.

This chapter is about that distinction: the precise, disciplined, human-supervised application of Microsoft Copilot to the highest-stakes workflows in banking. Helm Bank operates at the intersection of two regulatory universes — the rigorous US federal compliance framework and the complexity of Latin American correspondent banking relationships. The compliance team is small, the volume is large, and the standard is exacting. Copilot does not lower that standard. Used correctly, it helps the team meet it.

---

## Why Compliance Is Different

Every chapter in this book has emphasized human oversight. In compliance, we do not merely emphasize it — we enshrine it as an organizational and legal imperative.

The Bank Secrecy Act, the USA PATRIOT Act, OFAC regulations, and the guidelines issued by FinCEN, the OCC, and the FDIC all impose **personal liability** on compliance officers and, in certain circumstances, on bank executives. When a Suspicious Activity Report is filed, a human being signs it. When an OFAC match is cleared, a human being makes that determination. When a policy states that the bank has adequate controls, a human being attests to that fact. No AI system — however sophisticated — can assume this legal and ethical responsibility.

Copilot's role in compliance is therefore categorically different from its role in drafting a marketing email or summarizing a meeting. In those contexts, an error is embarrassing. In compliance, an error can trigger regulatory action, civil money penalties, or referrals to the Department of Justice.

Helm Bank's compliance program serves a bank that:

- Processes international wire transfers connecting the United States to Latin American correspondent banks across more than a dozen countries
- Maintains customer relationships with international businesses, high-net-worth individuals from the Latin American corridor, and US entities engaged in cross-border commerce
- Operates under OCC examination authority as a federally chartered institution
- Files Suspicious Activity Reports with FinCEN on a regular basis as part of its anti-money laundering obligations
- Screens transactions against OFAC sanctions lists daily, given the geographic risk profile of its customer base

This context matters. The risk environment that Helm Bank compliance operates in is more complex than a typical community bank. The volume of Latin American wire activity, the nature of the international correspondent relationships, and the elevated country risk profile all create a compliance environment where precision is not optional.

With that foundational understanding established, here is what Copilot genuinely does well in the compliance environment — and what Helm Bank professionals have learned to do with it.

```{figure} ../images/ch19-compliance-framework.png
:name: compliance-framework
:alt: The Helm Bank Compliance AI Framework showing human decision points at every stage
:width: 85%

**Figure 19.1** — The Helm Bank Compliance AI Framework. Copilot operates exclusively in the documentation and synthesis layers. Every regulatory determination, filing decision, and attestation remains with qualified human compliance professionals.
```

---

## The Microsoft Compliance Architecture: Due Diligence Before Deployment

Before discussing any specific workflow, Helm Bank compliance professionals need to understand the technical environment in which Copilot operates. This is not a formality — it is due diligence that the compliance team itself conducted before approving Copilot use in regulatory workflows.

### Data Residency and Sovereignty

Helm Bank operates under **Microsoft 365 E3 with the Compliance Add-On**, which provides the following data handling assurances:

All data processed by Microsoft 365 Copilot remains within the **Microsoft 365 service boundary**. Copilot does not transmit document content to OpenAI or any external AI provider for processing when used within M365 applications. The underlying AI model is hosted within Microsoft's infrastructure and governed by Microsoft's contractual commitments.

Helm Bank's Microsoft 365 tenant is provisioned in the **United States data region**, meaning all data at rest and in transit is processed within US data centers. This matters for a bank that handles customer financial information subject to US banking privacy regulations.

Customer data — including any document content that Copilot processes to generate a response — is **not used to train Microsoft's foundational AI models**. This is a contractual guarantee in the Microsoft Online Services Terms and the Microsoft Data Protection Addendum. The bank's IT Security and Legal teams reviewed and confirmed this commitment before compliance workflows were authorized for Copilot use.

As an international bank serving the Latin America–US corridor, Helm Bank has specific data sovereignty considerations for certain customer populations. The confirmed US data residency of the Microsoft 365 tenant satisfies the bank's data handling requirements for compliance documentation workflows.

### Audit Logs and eDiscovery

Every Copilot interaction within Microsoft 365 is logged in the **Microsoft Purview Unified Audit Log**. This has two critical implications for compliance work:

First, if a regulator or examiner asks how a particular document was drafted, Helm Bank can produce a complete record of Copilot prompts and outputs that contributed to that document. The audit trail for Copilot use is built into the platform.

Second, Copilot interactions are subject to **Microsoft Purview eDiscovery** searches, meaning they can be preserved, searched, and produced in legal proceedings or regulatory investigations. The bank's Legal and Compliance teams confirmed that existing litigation hold and eDiscovery procedures cover Copilot activity logs.

Copilot outputs stored in SharePoint, OneDrive, Teams, or Outlook are subject to the bank's existing **data retention policies** as configured in Microsoft Purview Compliance. A document drafted with Copilot assistance and saved to the Compliance SharePoint site is subject to the same seven-year retention policy as any other compliance document.

### Information Barriers and Sensitivity Labels

Helm Bank has configured **Microsoft Purview Information Protection** with a tiered sensitivity label system. Documents labeled **CONFIDENTIAL — COMPLIANCE** or **RESTRICTED — SAR** carry the following protections:

- Encryption at rest and in transit using AES-256
- Restriction from sharing outside the compliance team SharePoint group without explicit authorization from the CCO
- Protection against screenshots and copy/paste to unauthorized applications on managed devices
- Access logging in the Microsoft Purview audit trail whenever the document is opened, modified, or shared

When Copilot drafts content that references labeled documents in the user's Microsoft 365 environment, the output inherits the highest sensitivity label of any source document. This is not a per-session configuration — it is enforced automatically by the Purview Information Protection engine.

```{admonition} Compliance Governance Requirement
:class: important
Before any compliance professional uses Copilot for work product that will be submitted to regulators or used in regulatory filings, confirm with the IT Security and Legal teams that:

1. The Microsoft 365 tenant is correctly configured for US data residency.
2. Audit logging for Copilot interactions is enabled in Microsoft Purview.
3. Copilot outputs are covered by the bank's document retention policies.
4. The sensitivity label taxonomy covers compliance document classifications.
5. The team understands what metadata will accompany any document produced in an eDiscovery context.

This is a one-time organizational confirmation, not a per-document check. The compliance team completed this review in Q1 of the Copilot deployment year. New compliance staff should confirm the review has been completed before using Copilot on regulatory work.
```

---

## BSA/AML Narrative Drafting: Where Copilot Earns Its Keep

The Bank Secrecy Act requires financial institutions to maintain a robust Anti-Money Laundering program with written policies, procedures, controls, and comprehensive documentation. The documentation burden is enormous — and it is precisely where Copilot provides legitimate, substantial value for Helm Bank's compliance team.

### What "Narrative Drafting" Actually Means

When compliance professionals at Helm Bank talk about BSA/AML narratives, they are referring to several distinct document types, each with different audiences and requirements:

**Transaction monitoring narratives** are the written explanations of why a particular alert from the bank's transaction monitoring system was dispositioned as a true positive (requiring escalation) or false positive (closed with or without notation). These are internal records reviewed by quality assurance and potentially by examiners.

**Case narratives** are the documented investigation records for escalated alerts, including the full account history review, transaction pattern analysis, counterparty research, adverse news findings, and rationale for the ultimate filing decision — SAR or no SAR.

**Program narratives** are sections of the bank's BSA/AML Program document that describe how specific controls operate, why risk-based decisions were made, and how the program addresses identified risks. These are reviewed by examiners as core program documentation.

**Policy justification narratives** are written rationale for policy decisions, exceptions, or risk appetite positions. When Helm Bank's BSA Officer makes a program design choice — for example, setting a specific dollar threshold for enhanced due diligence on wire transfers from certain countries — that choice must be documented with clear reasoning.

All of these require clear, factual, professional writing. None of them require creative writing or subjective judgment in the prose itself — the judgment has already been made by the compliance professional; the narrative is its documentation. This is exactly what Copilot is suited for.

### The Alert Disposition Workflow

Helm Bank's transaction monitoring system generates alerts that analysts review and document in the bank's case management platform. Each disposition requires a narrative. Here is the complete workflow showing where Copilot fits:

**Step 1 — Alert Review (Human Only).** The analyst examines the transaction pattern, reviews the account profile and history, checks prior alerts and case history in the case management system, performs adverse news searches, and reaches a preliminary conclusion. Copilot has no role at this stage. The analyst must independently understand the alert before any documentation is drafted.

**Step 2 — Investigation Notes.** The analyst documents their investigation findings in plain language — what they looked at, what they found, and what conclusion they reached. These notes are the authoritative record of the investigation.

**Step 3 — Template Setup.** The analyst opens a Word document using the Helm Bank alert disposition template. The template is stored in the Compliance SharePoint site and includes required fields: account number (masked per policy), alert type, alert date, rule triggered, disposition recommendation, and narrative section.

**Step 4 — Copilot Narrative Draft.** With the investigation complete and documented, the analyst prompts Copilot to structure the narrative from their investigation notes.

**Step 5 — Verification Review.** The analyst reads the draft line by line, comparing every factual claim to the investigation record. Any inaccuracy is corrected before the document is saved.

**Step 6 — Analyst Attestation.** The analyst saves the document with the CONFIDENTIAL — COMPLIANCE sensitivity label, applies their credentials in the required attestation field, and submits through the case management system. The narrative belongs to the analyst — not to Copilot.

### Approved Prompt Templates for Alert Disposition

The following prompt templates have been reviewed and approved by Helm Bank's BSA Officer for use in alert disposition documentation:

**For structuring alerts:**
```
Write a disposition narrative for a cash structuring alert for inclusion
in our BSA case management system. Key facts: [describe the transaction
pattern in plain language — number of transactions, amounts, timeframe].
Account profile: [describe the business type and account tenure].
Supporting rationale for disposition: [state your conclusion and reasoning].
Required tone: formal, factual, no speculation about intent.
Do not include any personally identifiable information or account numbers.
Base the narrative only on the facts I have provided.
```

**For velocity/rapid movement alerts:**
```
Draft a narrative for a transaction velocity alert disposition.
The alert flagged [number] transactions in [time period] totaling $[amount].
The customer's business type is [type]. Prior period comparison: [summary].
My investigation found: [your findings].
Disposition: [true positive / false positive / escalate to SAR review].
Rationale: [your reasoning].
Write in the style of a formal BSA case management record.
Use only the facts I have provided. Do not add information.
```

**For case summary narratives:**
```
I am documenting a closed BSA investigation case. Structure the following
facts into a formal case narrative with clearly labeled sections:
(1) Account Overview
(2) Alert Summary and Trigger
(3) Investigation Steps Taken
(4) Key Findings
(5) Disposition Rationale

Use formal compliance language suitable for regulatory review.
Do not add any information not contained in the notes I provide.
Do not state a compliance conclusion — I will add the disposition separately.

Investigation notes: [paste your documented investigation notes]
```

The final instruction in the case summary template — "do not state a compliance conclusion" — deserves emphasis. Copilot, when drafting an investigation narrative, may be inclined to summarize with a sentence like "Based on the above, the activity does not appear suspicious." That sentence is a compliance conclusion, and it must come from the human analyst, not from an AI. Removing that responsibility from Copilot — through explicit prompting — is essential.

```{admonition} Critical: Human Review Required
:class: warning
**Every BSA/AML narrative produced with Copilot assistance must be reviewed line by line by the analyst who will sign or submit it.**

The analyst is responsible for every factual claim in the narrative. Copilot cannot access the bank's core banking system, case management platform, or transaction monitoring database to verify figures. If the draft says "eight deposits over twelve days," the analyst must have counted eight deposits over twelve days independently. If the draft says "no prior SARs," the analyst must have confirmed that fact in the case management system.

AI-assisted does not mean AI-verified. The verification burden rests entirely with the human professional.
```

---

## SAR Documentation: The Highest-Stakes Writing in Banking

A Suspicious Activity Report is a federal document. Filed with FinCEN through the BSA E-Filing system, it triggers potential law enforcement attention, can inform financial investigations, and is subject to strict accuracy requirements under 31 CFR Part 1020.320. A materially false or misleading SAR implicates federal law. A SAR not filed when circumstances require it carries severe penalties.

Copilot's role in SAR documentation is the most carefully circumscribed of any compliance workflow in this chapter.

### What Copilot Can Help With in SAR Work

**Structure and completeness checking.** FinCEN's SAR form requires specific fields and a narrative section with minimum elements commonly referenced as the "five Ws": who was involved, what activity occurred, when it occurred, where it occurred, and why it is suspicious. Copilot can review a completed draft SAR narrative and identify whether any required elements appear to be missing — giving the analyst a structured completeness check before the BSA Officer review.

**Language clarity and consistency.** SAR narratives must be readable by law enforcement agents who may have no banking background. A technically accurate narrative filled with banking jargon may be difficult for an FBI financial crimes agent to use effectively. Copilot can make a jargon-heavy narrative clearer without altering the substance, when given the draft and asked specifically to improve readability without changing facts.

**Consistent formatting across SAR filings.** Helm Bank files SARs on a regular basis given its international wire volume and risk profile. Copilot can apply consistent structure and professional formatting across multiple SAR drafts, making the bank's filings more coherent and easier for FinCEN analysts to process.

**Continuing SAR support.** When a continuing activity SAR is filed — typically 90 days after an initial SAR on an ongoing suspicious pattern — the filing must reference the prior SAR and describe the continuation of activity. Copilot can help structure the "prior SAR reference" section and organize the updated activity description, given the analyst's documented investigation findings.

### What Copilot Cannot Do in SAR Work

```{admonition} Critical: Human Review Required
:class: warning
**The SAR filing decision is never an AI decision. This boundary does not move.**

Copilot must not be used to determine whether a SAR should be filed. The decision to file — or not to file — a Suspicious Activity Report is a legal determination made by a qualified BSA Officer or their authorized designee, based on facts reviewed by a human investigator who has personally examined the underlying records.

No AI system has the authority, legal standing, or accountability to make this determination. The BSA Officer's signature on a SAR is a personal attestation of accuracy and of the filing determination.

Additionally:
- Copilot cannot access FinCEN's BSA E-Filing system under any circumstances
- Copilot cannot verify customer or counterparty information against any external database
- Copilot cannot determine whether activity meets the legal standard for "suspicious activity"
- Copilot-assisted SAR narratives require review and approval by the BSA Officer before filing
- SAR confidentiality under 31 U.S.C. 5318(g)(2) prohibits disclosure of SAR existence to any unauthorized party — be mindful of what information you include in Copilot prompts
```

### The Helm Bank SAR Drafting Protocol

Helm Bank's BSA team follows a four-stage protocol for SAR documentation, approved by the BSA Officer and reviewed by external BSA counsel:

**Stage 1 — Investigation Complete (No Copilot).** The investigating analyst completes the full investigation: account review, transaction analysis, counterparty research, adverse news search, prior SAR history check, and escalation to the BSA Officer. All decisions — including the filing recommendation — are made at this stage by human investigators. The BSA Officer reviews the investigation and makes the final SAR filing determination. Copilot has no involvement in this stage.

**Stage 2 — Narrative Drafting (Copilot Permitted).** With the investigation complete and the filing decision made by the BSA Officer, the analyst may use Copilot to draft the SAR narrative. The analyst provides their complete investigation notes as input. The output is a draft only — it has no regulatory standing until reviewed and approved.

**Stage 3 — BSA Officer Review and Approval (No AI Substitution).** The BSA Officer reviews the draft SAR narrative against the underlying investigation record and case management documentation. Every factual claim is independently verified. The narrative is edited as needed. The BSA Officer's review is documented in the case file, including the date, reviewer, and any changes made.

**Stage 4 — Filing (Human Only).** The completed and approved SAR is filed through FinCEN's BSA E-Filing system by an authorized filer with BSA E-Filing credentials. No AI system has access to or involvement in this process. The filer's login and submission constitutes the official filing record.

```{figure} ../images/ch19-sar-protocol.png
:name: sar-protocol
:alt: The four-stage SAR drafting protocol showing Copilot involvement only in Stage 2 narrative drafting
:width: 90%

**Figure 19.2** — The Helm Bank SAR Drafting Protocol. Copilot's involvement is precisely bounded to narrative drafting assistance in Stage 2. The filing determination (Stage 1) and the BSA Officer's attestation (Stage 3) are exclusively human activities.
```

**Sample SAR narrative drafting prompt (to be used only after Stage 1 is complete):**
```
I need to draft the narrative section of a FinCEN Suspicious Activity Report.
The narrative must address the following elements in order:
1. Who was involved (use "Subject" and "Account Holder" — no real names or account numbers)
2. What suspicious activity occurred (specific transactions, patterns, amounts)
3. When it occurred (use month/year ranges, not specific dates unless necessary)
4. Where it occurred (institution name, geographic locations of transactions)
5. Why it is suspicious (describe the observable facts that form the basis —
   do not state conclusions about criminal purpose or intent)

Required: Write in clear, direct language suitable for a law enforcement audience
with no banking background. Do not use jargon. Do not speculate about motive.
Do not add any facts not in my investigation summary.

Investigation summary: [paste summary here — no PII, no account numbers]
```

---

## OFAC Screening: Workflow Support, Not Decision Support

The Office of Foreign Assets Control administers economic sanctions programs that prohibit transactions with designated individuals, entities, and geographic regions. For Helm Bank, operating at the intersection of US and Latin American banking, OFAC compliance is not a peripheral concern — it is a central daily practice integrated into every wire transfer, new account opening, and correspondent banking transaction.

The bank's transaction volume involving Latin American counterparties, its international correspondent relationships across the Caribbean and Central and South America, and the elevated OFAC risk profile of certain customer segments all make OFAC compliance a high-priority operational discipline.

### The Boundary That Does Not Move

OFAC screening decisions — specifically whether a potential match to the SDN list or another OFAC list is a true match or a false positive — are made by qualified compliance analysts using the bank's approved screening platform. Copilot is not a screening tool.

Copilot does not have access to the current OFAC SDN list. It cannot perform name-matching algorithms against current sanctions databases. It cannot account for aliases, transliterations, or vessel and aircraft identifiers used in OFAC designations. It does not have real-time awareness of new designations, which OFAC can publish on any business day. Its training data contains an outdated and incomplete representation of OFAC lists that is entirely unsuitable for compliance purposes.

This is not a limitation of Copilot's intelligence. It is a structural boundary driven by the nature of the task: OFAC screening requires access to current, authoritative lists maintained by the US Treasury Department, applied through approved and validated matching methodologies, with human review of all potential matches against the full case record. Copilot is not designed for this purpose and should not be used for it.

### Where Copilot Adds Value in OFAC-Related Work

**Drafting OFAC false positive documentation.** When the screening platform generates a potential match and the compliance analyst determines after review that it is a false positive, the analyst must document the basis for that determination. This documentation — including the match basis, the distinguishing factors reviewed, and the analyst's reasoning — benefits from clear, professional structure. Copilot can structure this documentation given the analyst's factual inputs.

**OFAC procedures manual maintenance.** The bank's OFAC screening procedures document requires regular updates as the screening platform evolves, new sanctions programs are established, or internal processes change. Copilot can draft updated procedure sections based on direction from the OFAC Compliance Officer.

**OFAC training content.** The OFAC compliance team conducts annual training for all customer-facing staff, including wire operations, new accounts, and relationship managers. Given Helm Bank's Latin American focus, training must address country-specific risk scenarios relevant to the bank's actual customer base. Copilot can help develop training scenarios, quiz questions, and explanatory materials — all reviewed by the OFAC Compliance Officer before use.

**OFAC-related correspondence.** When a wire transfer is placed on hold pending OFAC review, the bank may need to communicate with the originating institution or the beneficiary bank. Copilot can draft professional holding notices and information request letters based on templates pre-approved by Legal.

```{admonition} Critical: Human Review Required
:class: warning
**OFAC match dispositions are never delegated to AI.**

When the bank's screening system generates a potential match to an OFAC list, the disposition of that match follows the bank's approved OFAC procedures, reviewed by a qualified compliance analyst, with escalation to the OFAC Compliance Officer for true matches or genuinely ambiguous cases.

Do not ask Copilot to assess whether a name is on the SDN list or whether a potential match should be cleared. Copilot's response to such questions is unreliable and legally insufficient. OFAC match determinations require current, authoritative list data and qualified human judgment.
```

---

## Exam Preparation: Building the Package

The OCC, FDIC, and state banking regulators conduct periodic examinations of Helm Bank's compliance programs. Examination preparation — organizing information request responses, assembling documentation packages, and preparing management presentations — is one of the most time-intensive activities in the compliance calendar, and one where Copilot can provide genuine efficiency gains without touching any compliance determination.

### Managing the Information Request

When an examiner delivers an information request, it typically contains thirty to one hundred line items requesting policies, procedures, reports, management information system outputs, training records, and documentation samples. Organizing the response is a project management challenge as much as a compliance challenge.

**Copilot as IR Project Manager:**
```
I have an OCC examination information request with 63 line items.
I will paste the full IR list below. Please:
1. Organize the items into logical categories (e.g., Policies and Procedures,
   Training Records, Risk Assessment, Testing and Quality Assurance,
   Transaction Monitoring, Customer Due Diligence)
2. Identify which items require document production versus written explanation
3. Flag items that appear to overlap or that could be addressed
   by a single document with a note
4. Create a tracking table with columns: Item Number | Description |
   Category | Response Type | Assigned To | Due Date | Status

Leave the last three columns blank — I will populate those.

IR list: [paste the full list]
```

This prompt asks Copilot to organize a project list — not to assess the bank's compliance. That is appropriate use.

**Copilot for Policy Coverage Analysis:**

When the IR requests documentation of a specific control and the team needs to assess whether existing policies address the examiner's requirements, Copilot can help structure the initial comparison:

```
An OCC examiner is requesting documentation of our Customer Due Diligence
procedures covering the following specific requirements:
[paste the examiner's itemized requirements]

I have our current CDD Policy. Please compare the policy text I provide
to the examiner's requirements and identify:
1. Requirements that appear clearly addressed by current policy language
2. Requirements where policy coverage may be partial or ambiguous
3. Requirements that do not appear to be addressed

Important: Do not conclude that our policy is compliant or non-compliant.
List only where coverage appears present, partial, or absent — I will
make the compliance assessment.

Current CDD Policy: [paste relevant policy sections]
```

The output gives the compliance team a structured starting map for their own analysis. A human compliance officer then applies regulatory expertise and makes the actual adequacy assessment.

### Building the Exam Preparation Presentation

Management presentations before OCC examination arrivals brief senior leaders on examination scope, logistics, and the bank's posture. Copilot can draft these presentations efficiently given factual inputs:

```
Draft a PowerPoint outline for a 20-minute pre-examination management briefing.
Structure it with slides covering:
1. Examination overview — scope, examiner team, scheduling
2. Key focus areas identified by the examiner
3. Information request status (I will add the tracking table)
4. Program strengths — areas where our documentation and controls are strong
5. Recent program enhancements — improvements made since the last exam
6. Key messages and behavioral guidance for staff during the examination
7. Q&A and next steps

Tone: confident, factual, professional. Internal audience of senior management
and department heads. Use plain language — avoid compliance jargon where possible.
This is a preparation briefing, not a regulatory submission.
```

```{figure} ../images/ch19-exam-prep.png
:name: exam-prep-workflow
:alt: Helm Bank exam preparation workflow showing Copilot involvement at IR organization, policy gap mapping support, and presentation drafting
:width: 88%

**Figure 19.3** — Exam Preparation Workflow at Helm Bank. Copilot contributes at three phases: information request organization, policy coverage mapping support, and presentation drafting. All substantive compliance assessments and management representations remain with the BSA Officer and Chief Compliance Officer.
```

---

## Regulatory Change Management: Staying Current in a Moving Landscape

The regulatory environment for banking compliance changes continuously. FinCEN issues guidance updates on AML program expectations. The OCC publishes bulletins on examination priorities. The FDIC releases supervisory findings that signal emerging concerns. New sanctions programs activate without advance notice. Keeping current with regulatory change is a full-time responsibility within a compliance team that is already at full capacity.

Copilot can serve as a powerful tool for regulatory change management — with clear discipline about the temporal limitation that applies to all AI language models.

### The Temporal Limitation — Non-Negotiable

```{admonition} Important: Copilot's Knowledge Has a Training Cutoff
:class: warning
Microsoft Copilot's underlying language model was trained on data up to a specific cutoff date. Regulatory guidance, OFAC designations, enforcement actions, and rule changes issued after that date are unknown to Copilot — and Copilot may not reliably know its own cutoff date or the extent of its regulatory knowledge gaps.

**Never ask Copilot to summarize current regulatory requirements from its own knowledge.** Always provide the regulatory document as an attachment or pasted text, and ask Copilot to analyze only what you have provided.

Authoritative sources for current guidance:
- FinCEN guidance and advisories: fincen.gov/resources/statutes-and-regulations/guidance
- OCC bulletins: occ.gov/news-issuances/bulletins
- FDIC financial institution letters: fdic.gov/regulations/applications/notices
- Federal Register: federalregister.gov
```

### Copilot for Regulatory Document Analysis

When new regulatory guidance is issued, the compliance team's first task is understanding what it says and what it requires. Copilot can accelerate this initial analysis significantly when given the actual document:

**Workflow — New FinCEN Guidance Received:**

1. Download the official guidance document from fincen.gov
2. If PDF, use Word's PDF-to-Word conversion or paste key sections into a Word document
3. Use Copilot within that document to analyze the content

**Analysis prompt:**
```
Analyze this regulatory guidance document and provide:
1. A plain-language summary of the guidance's main points (one concise paragraph)
2. A numbered list of the specific requirements or supervisory expectations stated
3. Any requirements that appear to represent new or heightened expectations
   compared to standard BSA/AML program requirements
4. Any implementation deadlines or effective dates mentioned in the document
5. Key terms or definitions established in the guidance

Important: Summarize and quote only from this document. Do not supplement
with your general knowledge of BSA/AML requirements or other regulatory guidance.
Flag it clearly if any requirement is ambiguous in the document's own language.
```

4. Review the Copilot analysis against the source document — verify that all quoted requirements are accurately represented
5. Use the analysis as the starting point for the compliance team's impact assessment

**Regulatory Change Tracking:**

Helm Bank maintains a regulatory change log in SharePoint — a running record of new guidance, impact assessments, and implementation status. Copilot can format new entries consistently:

```
Add a new entry to our regulatory change tracking log with the following information:
- Source agency: [FinCEN / OCC / FDIC / Fed / State]
- Date issued: [date]
- Document title and reference number: [title]
- Brief description: [one-sentence description of the guidance]
- Summary of key requirements: [paste from your prior analysis]
- Preliminary impact assessment: [High / Medium / Low — I will determine this]
- Assigned compliance owner: [name]
- Implementation target date: [date]
- Current status: Open — Assessment in Progress

Format this as a new entry consistent with our existing log structure.
```

---

## Policy Document Maintenance: The Perpetual Revision Cycle

BSA/AML, OFAC, CDD, and related compliance policies require regular review and update. Helm Bank's policy governance framework requires annual reviews of all compliance policies, with off-cycle updates triggered by regulatory change, examination findings, or material program modifications. This generates a continuous stream of document drafting work throughout the year.

### Policy Section Revision

When a specific policy section requires update — for example, to reflect a new beneficial ownership threshold, an updated customer risk rating methodology, or a revised wire transfer monitoring threshold — Copilot can draft the revised section based on the compliance team's direction:

```
Draft a revised policy section updating our Customer Due Diligence Policy
to reflect the following changes determined by the BSA Officer:
1. Beneficial ownership collection threshold changed from 25% to 10%
   (effective 180 days from [date])
2. New triggering events added requiring updated beneficial ownership
   verification: ownership change, merger/acquisition, material relationship change
3. Beneficial ownership update timeframe: within 30 days of triggering event

The existing section language is: [paste current section]

Write the revised section in the same formal policy style and structure.
Preserve all language that is not affected by these specific changes.
Flag any places where the change creates apparent inconsistency with
adjacent policy language so I can review those sections separately.
```

### Cross-Policy Consistency Review

A persistent policy maintenance challenge is definitional inconsistency across documents. Copilot can help identify these inconsistencies efficiently:

```
I am pasting two compliance policy documents that should be consistent
with each other. Please identify:
1. Terms defined in one document but used without definition in the other
2. Terms that appear to be defined differently across the two documents
3. Procedural requirements in one document that appear to contradict
   requirements in the other
4. Reference numbers or policy citations that appear in one document
   but cannot be located in the current text

List each finding with the document name, section reference, and the
specific language creating the inconsistency.

Document 1 — BSA/AML Program: [paste]
Document 2 — Customer Due Diligence Policy: [paste]
```

### Policy Change Summary for Approval Record

When a policy is revised and submitted for approval through the bank's policy governance process, a summary of changes is required. Copilot can generate this automatically:

```
Compare the prior and current versions of this policy and produce a change summary:
1. Brief executive summary of the revision (2-3 sentences describing what changed and why)
2. Table of changes: Section Number | Change Type (Added / Deleted / Modified) |
   Description of Change
3. Identification of any sections that were renumbered or restructured
   (even if content was unchanged)

Prior version: [paste]
Current version: [paste]
```

---

## Audit Trail Documentation: Building the Evidentiary Record

Regulators and examiners verify compliance programs through documentation. The audit trail is the evidence that controls exist, function as designed, and have been consistently applied. Copilot can help compliance professionals build more complete, consistent, and professional audit trail documentation across several dimensions.

### Quality Assurance Testing Reports

Helm Bank's compliance testing function conducts quarterly QA reviews of BSA/AML alert dispositions, CDD file quality, and SAR decisions. Each review produces a testing report that becomes part of the permanent audit trail and is available for examiner review.

**QA Report Drafting Prompt:**
```
Draft a compliance quality assurance testing report based on the following
testing results. Use the section structure below exactly:

Section 1: Testing Scope and Methodology
Section 2: Sample Selection Criteria and Sample Size
Section 3: Testing Results Summary (including pass/fail rates)
Section 4: Exceptions Identified (description of each exception)
Section 5: Root Cause Analysis
Section 6: Recommendations
Section 7: Management Response [leave this section blank with a placeholder]

Tone: formal, objective, suitable for regulatory review.
Do not state that our program is compliant or non-compliant overall —
the report presents testing findings, not program conclusions.

Testing data and findings: [paste your testing documentation]
```

### Control Effectiveness Documentation

When preparing evidence of specific control effectiveness — for example, demonstrating that the bank's transaction monitoring thresholds are calibrated appropriately — Copilot can help structure the evidence package into a coherent narrative that organizes screenshots, reports, and explanatory text into a readable document.

```{admonition} Critical: Human Review Required
:class: warning
**Audit documentation submitted to regulators requires verification of every factual claim.**

When Copilot assists with audit trail documentation, the responsible compliance professional must verify against source systems:
- All statistics, metrics, and percentages
- All dates and time periods
- All procedural descriptions against actual current procedures
- All exception counts and descriptions against the actual exception records

A QA report that overstates the pass rate, understates exceptions, or mischaracterizes a finding — even as a result of AI drafting error — is a material misrepresentation. The compliance professional who signs or submits the report is responsible for its accuracy. Verify the numbers before the signature goes on the page.
```

---

## Board Reporting: Compliance in the Boardroom

Helm Bank's Board of Directors receives quarterly compliance reports presented by the Chief Compliance Officer. These reports present the state of the BSA/AML, OFAC, and overall compliance programs to directors who bring governance expertise but are not typically compliance specialists. The board must understand what they are reviewing well enough to fulfill their oversight obligations — which means the CCO must translate compliance complexity into clear executive communication.

This translation work — from technical compliance metrics to board-level narrative — is where Copilot provides some of its most valuable assistance in the compliance function.

### Quarterly Compliance Report Structure

A complete Helm Bank quarterly compliance report for the board includes:

1. **Executive Summary** — Program health, material developments, significant matters requiring board awareness
2. **BSA/AML Program Status** — Alert volumes and trends, disposition metrics, SAR filing activity (volume only, no case details — filings are confidential under federal law)
3. **Regulatory and Examination Activity** — Examinations completed or in progress, findings and remediation status, material regulatory correspondence
4. **Training and Awareness** — Completion rates by business unit, upcoming mandatory training requirements
5. **Policy and Procedure Updates** — Policies reviewed or updated, pending policy approvals
6. **Key Risk Indicators** — Compliance metrics plotted against established risk thresholds
7. **Issues and Remediation Tracker** — Open audit or examination findings, responsible parties, remediation deadlines, and status
8. **Forward Look** — Regulatory calendar, planned program enhancements, emerging risk areas

Copilot can draft all of these sections given factual inputs from the compliance team. The draft is reviewed, edited, and approved by the CCO before any board distribution.

**Board Report Executive Summary Prompt:**
```
Draft the executive summary section of a quarterly board compliance report
for an international bank focused on Latin American business.
Target length: 275-325 words.

Requirements:
- Written for board directors who are experienced business leaders
  but not compliance specialists
- Confident, professional tone — neither dismissive of challenges nor alarmist
- Clear about what is working well and what requires board awareness
- All regulatory acronyms spelled out on first use
- No compliance jargon — plain business English throughout

Key facts for this quarter:
- [Describe BSA/AML program status in plain language]
- [Describe any examination activity and current status]
- [Describe any significant compliance developments or issues]
- [State the CCO's overall program assessment: Satisfactory / Needs Attention]

Do not add facts I have not provided. Do not speculate about regulatory risk.
Do not include any information that could relate to a specific SAR or investigation.
```

```{figure} ../images/ch19-board-report.png
:name: board-report
:alt: Sample Helm Bank quarterly compliance board report structure with Copilot-drafted narrative sections
:width: 85%

**Figure 19.4** — Sample Helm Bank Quarterly Compliance Board Report. Copilot contributes narrative clarity and consistent formatting across all sections. The CCO provides all substantive compliance assessments and approves the report before board distribution.
```

---

## Hands-On Exercises

The following exercises are designed for Helm Bank compliance professionals. Complete them using your Microsoft 365 Copilot access in a **training environment only**. Do not use real customer data, real alert details, real SAR-related information, or any actual customer names or account numbers in any exercise.

---

### Exercise 19.1 — Alert Disposition Narrative Drafting

**Learning objective:** Practice applying the verification discipline to Copilot-assisted alert disposition narratives.

**Scenario (fictional — use exactly as written, do not modify):**
- Alert type: Transaction structuring
- Account type: Business checking, wholesale produce distributor, 6 years account history
- Alert trigger: Eleven cash deposits over 18 days, each between $8,200 and $9,700, totaling $97,350
- Investigation findings: Transaction pattern is consistent with the customer's established cash handling practices for retail market customers who pay cash on delivery. Reviewed 24 months of prior account history — same seasonal cash deposit pattern observed in prior years during agricultural peak season (Q4). Counterparties are documented in the customer's business records on file. No adverse news. No prior SARs on this account.
- Analyst disposition decision: False positive — close alert, document seasonal cash pattern, set enhanced monitoring flag for next Q4 review cycle.

**Your tasks:**
1. Write a Copilot prompt to produce a professional BSA alert disposition narrative based on the scenario above. Apply the prompt discipline principles from this chapter.
2. Run the prompt in Copilot (Word or Teams).
3. Read the output carefully. List every factual claim Copilot made in the narrative.
4. For each claim, note: Is it directly supported by the scenario facts I provided? Or did Copilot add or infer something?
5. Correct any inaccuracies or added information.
6. Write one sentence describing what you would do next in a real workflow before this narrative is finalized.

**Reflection:** Did Copilot stay within the facts you provided, or did it add plausible-sounding details? What does this tell you about the verification discipline required in compliance work?

---

### Exercise 19.2 — Regulatory Impact Analysis

**Learning objective:** Practice using Copilot to structure a regulatory gap analysis while maintaining human control of all compliance conclusions.

**Fictional guidance excerpt (use exactly as written):**
> "Financial institutions must collect and verify beneficial ownership information for any natural person who owns, directly or indirectly, 10% or more of a legal entity customer. This threshold replaces the prior 25% threshold. Verification of beneficial ownership must occur at the time of account opening and must be refreshed upon any triggering event, including: a change in the legal entity's ownership structure, a merger or acquisition, a change in the nature of the customer relationship as determined by the institution, or any red flag that calls into question the accuracy of existing ownership information. Financial institutions must update their Customer Due Diligence policies and procedures to reflect this guidance within 180 calendar days of issuance."

**Fictional current policy excerpt (use exactly as written):**
> "Helm Bank collects beneficial ownership information for legal entity customers where one or more natural persons hold 25% or more equity interest. This information is collected at account opening using the Beneficial Ownership Certification Form. Periodic review of beneficial ownership records occurs as part of the enhanced due diligence review cycle for customers rated high-risk under the bank's Customer Risk Rating methodology."

**Your tasks:**
1. Draft a Copilot prompt asking Copilot to compare the guidance requirements to the current policy and identify where gaps appear to exist. Include the instruction that Copilot should not conclude whether the policy is compliant.
2. Run the prompt.
3. Review the output. Did Copilot correctly identify the threshold change (25% to 10%)?
4. Did Copilot identify the triggering events requirement as a new element not covered by the current policy?
5. Did Copilot correctly note the 180-day implementation deadline?
6. Write three bullet points describing what you — as the compliance analyst — would do next if this were a real guidance document. (Hint: your list should involve legal review, BSA Officer sign-off, and a specific deliverable.)

---

### Exercise 19.3 — Board Report Executive Summary Drafting

**Learning objective:** Apply board-audience communication principles to compliance report drafting using Copilot, and practice the review discipline applied to high-stakes documents.

**Fictional Q3 compliance facts (use exactly as written):**
- BSA/AML program status: Satisfactory. Transaction monitoring alert volume increased 11% quarter-over-quarter, consistent with an increase in international wire volume from new correspondent banking relationships onboarded in Q2.
- SAR filings: Within the expected range for the bank's risk profile. [Do not include specific numbers — SAR filing volumes are bank-confidential.]
- Examination activity: No examinations completed this quarter. OCC Safety and Soundness and BSA examinations are scheduled for Q4, estimated to begin in November.
- Compliance training: Annual BSA/AML mandatory training completion rate is 96% as of September 30. Seven employees have not completed the training; individual follow-up is in progress with their managers. Completion target: October 31.
- Policy updates: Customer Due Diligence Policy updated in August to reflect new beneficial ownership threshold guidance. Approved by Board Risk Committee on August 19.
- Open issues: One open examination finding from the prior year OCC examination (transaction monitoring governance documentation). Remediation was completed September 15. The bank has submitted remediation documentation to the OCC for verification, which is pending.
- Forward look: OCC examination beginning November. Based on industry examination trends and recent OCC guidance, expected focus areas include beneficial ownership controls, international wire transfer monitoring, and correspondent banking due diligence documentation. Pre-examination preparation is underway.

**Your tasks:**
1. Draft a Copilot prompt to produce the executive summary section of the Q3 board compliance report. Specify the target audience (board directors), appropriate tone, target length (approximately 300 words), and content boundaries (do not include SAR-specific information; do not add facts not provided).
2. Run the prompt.
3. Read the draft from the perspective of a board director who is not a compliance specialist. Rate it on: (a) clarity — is it clear what the bank's compliance situation is? (b) appropriate confidence — is the tone balanced? (c) completeness — are all key facts from the scenario represented?
4. Make at least two specific edits to improve the draft based on your assessment.
5. List what the CCO must do with this draft before it is distributed to the board.

---

## The Verification Discipline: A Compliance Professional's Copilot Code

Across every workflow in this chapter, one principle has appeared consistently: the human reviewer must verify every factual claim in every Copilot output before that output becomes a compliance record. This is not generic AI caution — it is a compliance-specific operational requirement that flows directly from the legal and regulatory accountability that compliance professionals carry.

The following verification discipline has been adopted by Helm Bank's compliance team and applies to every use of Copilot in compliance workflows:

**Principle 1: No AI fact stands unverified.** If a Copilot draft states "twelve transactions totaling $97,000," the reviewer independently confirms twelve transactions and the aggregate amount from the source system. Numbers, dates, account details, and transaction descriptions are verified against primary source data — not accepted because they appear in the draft.

**Principle 2: Prompt construction is the first control.** The most effective way to prevent fabricated details is to instruct Copilot explicitly not to add them. "Base the narrative only on facts I have provided" and "do not add information not in my notes" reduce hallucination risk at the point of generation. This instruction is embedded in every compliance prompt template used at Helm Bank.

**Principle 3: Copilot drafts; humans conclude.** No Copilot output should include a compliance conclusion — that a customer is "not suspicious," an alert is "clearly a false positive," a program is "adequate," or that the bank is "in compliance" with a regulatory requirement. These are conclusions that require human professional judgment. If Copilot includes one, delete it and replace it with the analyst's own assessment.

**Principle 4: Sensitivity labels are not optional.** Every compliance document produced with Copilot assistance receives the appropriate Microsoft Purview sensitivity label before saving. CONFIDENTIAL — COMPLIANCE for internal work product; RESTRICTED — SAR for anything touching SAR-related materials. This is a data governance requirement, not a preference.

**Principle 5: Document the use of AI assistance.** Helm Bank's compliance policy requires that documents produced with AI drafting assistance include a notation in the version history or document metadata. This notation is preserved in the audit trail and ensures transparency in any future eDiscovery or regulatory review context.

**Principle 6: Regulatory submissions receive double review.** Any document that will be submitted to a regulator, filed with FinCEN, or presented to the board receives a final review by the BSA Officer or CCO in addition to the analyst's own review. AI-assisted drafting does not reduce the review requirements — it improves the quality of the draft that enters review, but the review process itself remains unchanged.

---

## What Copilot Must Never Do in Compliance

For absolute organizational clarity, the following table identifies compliance activities that must not involve Copilot or any AI tool. These boundaries are established by the BSA Officer and the Chief Compliance Officer and apply to all Helm Bank compliance staff.

| Activity | Reason AI Cannot Be Used |
|---|---|
| Deciding whether to file a SAR | Legal determination requiring human judgment and personal attestation; federal law applies |
| Clearing an OFAC potential match | Sanctions determination requiring current authoritative list data and human decision authority |
| Assigning a customer risk rating | Risk classification is a compliance determination subject to regulatory examination |
| Approving a policy as regulatory-compliant | Compliance determination requiring legal expertise and professional accountability |
| Signing or electronically submitting any regulatory filing | Submissions require authorized human signatories with legal accountability |
| Interpreting ambiguous regulatory language | Regulatory interpretation carries legal risk and requires counsel involvement |
| Determining whether an exception requires escalation | Escalation is a judgment call with potential legal and regulatory consequences |
| Attesting to the accuracy of any compliance statement | Attestations are personal — AI cannot attest on behalf of a human professional |
| Making any determination under BSA, OFAC, or AML regulations | All regulatory determinations are exclusively human activities |

---

## Chapter Summary

This chapter has covered the most rigorous application of Microsoft Copilot in the Helm Bank environment. The principles to carry forward are clear and non-negotiable:

**The hierarchy is clear and permanent.** Compliance professionals make all compliance decisions. Copilot assists with documentation, narrative drafting, document organization, policy structuring, and report preparation. This division of responsibility is not a current limitation that will be updated in the next software version — it reflects the legal and ethical structure of regulatory compliance.

**The Microsoft compliance architecture is the foundation.** US data residency, Purview audit logging of all Copilot interactions, automatic sensitivity label inheritance, and eDiscovery coverage of Copilot activity logs mean that Copilot use in compliance is traceable, auditable, and defensible. Confirm this architecture is correctly configured before any compliance workflow uses Copilot.

**Prompt discipline is the primary control.** The instruction to work only from provided facts, avoid conclusions, use formal professional language, and omit personally identifiable information belongs in every compliance prompt. These instructions are not courtesies — they are controls.

**Verification discipline is the secondary control.** Every factual claim in every Copilot output must be verified against primary source data by the human compliance professional who will sign, submit, or present the document. The verification burden is absolute.

**The value is real and material.** Carolina Vasquez left the office that Thursday at 6:15 PM — not at 9:00 PM as she had feared. The exam package was complete. The SAR narrative was drafted, reviewed, and approved. The alert queue had eleven items remaining, not forty-one. Copilot made no compliance decisions. But it gave Carolina two additional hours of her Thursday evening, and it gave the OCC examination team a more consistently documented, professionally structured set of records to review.

That is the right use of AI in the most regulated room in the bank. Disciplined. Bounded. Verified. Human.

---

## Key Terms

**Bank Secrecy Act (BSA)** — Federal law (31 U.S.C. §§ 5311-5336) requiring financial institutions to maintain records, file reports, and implement programs to assist government agencies in detecting and preventing money laundering, terrorist financing, and other financial crimes.

**Suspicious Activity Report (SAR)** — A report filed with FinCEN when a financial institution detects suspicious transaction activity that may involve money laundering, fraud, or other financial crime. SARs are confidential under federal law — their existence cannot be disclosed to any person involved in the suspicious activity.

**OFAC (Office of Foreign Assets Control)** — A bureau of the US Treasury Department that administers and enforces economic and trade sanctions based on US foreign policy and national security goals. The Specially Designated Nationals and Blocked Persons List (SDN list) is OFAC's primary sanctions list.

**AML (Anti-Money Laundering)** — The body of laws, regulations, and procedures designed to detect, prevent, and report the use of the financial system to launder the proceeds of criminal activity.

**FinCEN (Financial Crimes Enforcement Network)** — A bureau of the US Treasury Department that collects, analyzes, and disseminates financial intelligence to combat domestic and international money laundering, terrorist financing, and other financial crimes. FinCEN administers the BSA E-Filing system.

**Human-in-the-Loop** — A governance principle requiring that a qualified human professional makes all decisions of regulatory, legal, or ethical consequence. In compliance, this is not merely a principle — it is a legal requirement.

**Microsoft Purview** — Microsoft's portfolio of data governance, compliance, and risk management solutions, including Information Protection (sensitivity labels), the Unified Audit Log, Compliance Manager, eDiscovery, and Data Lifecycle Management. Purview is the compliance infrastructure underlying Copilot governance at Helm Bank.

**Continuing SAR** — A SAR filed approximately 90 days after an initial SAR to report that the suspicious activity described in the prior filing is continuing. FinCEN guidance requires continuing SARs when suspicious activity has not ceased.

**SAR Confidentiality** — Under 31 U.S.C. § 5318(g)(2), a financial institution and its officers, directors, employees, and agents may not disclose to any person involved in a suspicious transaction that a SAR has been filed or that a report has been prepared. This prohibition applies regardless of any tools or methods used in the SAR preparation process.

---

## Looking Ahead

Chapter 20 moves from the compliance suite to the executive suite — how Helm Bank's senior leadership uses Copilot for strategic planning, investor reporting, and cross-functional decision support. We will examine how the human-in-the-loop principles established in this chapter translate across different stakes and different audiences, and how Copilot supports institution-wide intelligence synthesis without becoming a substitute for executive judgment.

The compliance team has set the standard for disciplined AI use at Helm Bank. Chapter 20 shows how that discipline — adapted for the boardroom — applies at the highest level of the organization.

---

*Chapter 19 of "The Essence of AI: A Microsoft Copilot Master Class for Helm Bank" — Week 6, Session C. This chapter is intended for qualified compliance professionals at Helm Bank USA and does not constitute legal advice. All regulatory determinations must be made by qualified personnel in accordance with applicable law, regulatory guidance, and the bank's approved compliance program. Regulatory requirements referenced in this chapter reflect general program expectations; consult current official guidance for specific requirements applicable to your institution.*
