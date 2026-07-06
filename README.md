# US CDC EBS Toolkit

**Repository:** [github.com/dghpebsunit-ux/USCDC_EBSToolkit](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit)

A practical, modular toolkit for establishing, strengthening, and evaluating Event-Based Surveillance (EBS) as part of a country's Early Warning, Alert and Response (EWAR) system. This repository is maintained by the CDC Global Surveillance, Laboratory, and Data Systems Branch (GSLDSB) EBS Unit, Division of Global Health Protection (DGHP), and packages training materials, templates, and guidance for implementing EBS using a stepwise, multisectoral, One Health approach.

> **Scope note:** This toolkit focuses on EBS as a complement to Indicator-Based Surveillance (IBS). Both feed into epidemic intelligence and EWAR, but they serve different purposes — IBS is best suited to monitoring known, prioritized diseases against defined alert/outbreak thresholds; EBS is best suited to picking up unstructured, unexpected signals that IBS would miss.

---

## Table of Contents

- [Background](#background)
- [Core Concepts](#core-concepts)
- [Guiding Principles for Implementation](#guiding-principles-for-implementation)
- [Repository Structure](#repository-structure)
- [EBS Modalities](#ebs-modalities)
- [Signal Development](#signal-development)
- [Event Management](#event-management)
- [Monitoring & Evaluation](#monitoring--evaluation)
- [Getting Started](#getting-started)
- [References](#references)
- [Citation](#citation)
- [Contributing](#contributing)
- [License](#license)

---

## Background

Event-Based Surveillance is the organized collection, monitoring, assessment, and interpretation of largely unstructured, ad hoc information about health events or hazards that may pose an acute risk to human, animal, plant, or environmental health. EBS is one of two pillars of Early Warning (alongside IBS), and both are integrated through **epidemic intelligence** to support early detection, verification, risk assessment, and response.

This toolkit draws on and operationalizes established global and regional guidance, including:

- WHO's *[Early Warning Alert and Response in Emergencies: An Operational Guide](https://www.who.int/publications/i/item/9789240063587)* (2022)
- WHO's *[Early Detection, Assessment and Response to Acute Public Health Events](https://www.who.int/publications/i/item/WHO-HSE-GCR-LYO-2014.4)* (Interim EWAR/EBS Guide, 2014)
- The Africa CDC *[Event-based Surveillance Framework](https://africacdc.org/download/africa-cdc-event-based-surveillance-framework-2/)*, 2nd Edition (2023)
- CDC/GSLDSB EBS Unit training and implementation resources

---

## Core Concepts

EBS (and EWAR more broadly) follows a common workflow:

```
Detection → Triage → Verification → Risk Assessment → Alert → Response
```

| Step | Definition |
|---|---|
| **Signal** | Unverified information suggesting a potential acute health event |
| **Triage** | Filtering (removing duplicates/irrelevant info) and selection (matching against priority signal list) |
| **Event** | A signal that has been verified as authentic |
| **Alert** | A verified event that has been risk-assessed and requires a response |
| **Response** | Investigation, control measures, and/or communication triggered by an alert |

All signals — regardless of source — should be logged and managed through a **consistent, standardized workflow**, and every event should be resolved through **discard, monitor, or respond/investigate** outcomes.

---

## Guiding Principles for Implementation

EBS and broader EWAR implementation should be approached **stepwise**, not all at once. Key principles reflected throughout this toolkit:

1. **Strengthen before you expand.** Assess and reinforce existing surveillance and coordination structures before layering on new EBS modalities or geographic scope.
2. **Standardize across modalities.** Hotlines, media scanning, facility EBS, and community EBS (CEBS) should share a common signal list, triage logic, and reporting workflow wherever possible, to avoid fragmentation and ease comparison across sources.
3. **Start small if resources are limited.** Where funding or staffing is constrained, consider strengthening a **hotline** to capture community feedback before scaling up a full community health worker (CHW)-dependent CEBS network, which is more resource-intensive to sustain.
4. **Keep signals simple.** Signal definitions should be broad (sensitive, not specific), written in plain language, limited in number, and easy for non-specialists (including community members) to remember. Avoid heavy overlap with diseases/conditions already captured by IBS — EBS should focus on the unknown and unusual.
5. **Set clear thresholds for IBS.** Where indicator-based data is used, define explicit alert/epidemic thresholds (fixed value, moving average, or historical trend) per disease/condition so that signals are generated consistently.
6. **Build a functional event management backbone.** Every implementation — regardless of modality — needs a working signal/event log or Event Management System (EMS) that supports the full detection-to-response pipeline and connects directly to the team responsible for response.

---

## Repository Structure

This layout mirrors the modular design of the EBS Toolkit materials. Folder links point to the corresponding directory in the [GitHub repository](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit).

```
Module 1 - EWAR
    1.1-IHR-and-EWAR.pptx
    1.2-surveillance-frameworks.pptx

Module 2 - EBS Overview
    2.1-importance-of-ebs.pptx
    2.2-ebs-concepts-and-methods.pptx
    2.3-risk-assessment.pptx
    2.3.1-risk-assessment-case-study.pptx
    M2-cebs-signal-notebook.docx
    M2-cebs-febs-signal-register-key.docx
    M2-cebs-febs-signal-register.xlsx
    M2-ebs-sop-template.docx
    M2-ebs-signal-abstraction-form.docx
    M2-intermediate-level-ebs-event-log.xlsx
    M2-intermediate-level-ebs-event-log-key.docx
    M2-risk-assessment-guidance.docx

Module 3 - Considerations
    3.1-implementation-consideration.pptx
    3.2-one-health-and-cross-border-ebs.pptx
    3.2.1-one-health-case-study.pptx
    3.2.2-cross-border-case-study.pptx
    3.3-signal-development.pptx
    3.4-epidemics-and-pandemics.pptx
    M3-signal-development-guidance.docx

Module 4 - Hotlines
    4.1-hotline-ebs.pptx
    4.1.1-hotline-case-study.pptx
    4.1.2-hotline-case-study-handout.docx

Module 5 - Media Scanning
    5.1-media-scanning.pptx
    5.1.1-media-scanning-case-study.pptx
    5.1.2-eios-demo.pptx

Module 6 - Facility EBS
    6.1-facility-ebs.pptx
    6.1.1-healthcare-facility-case-study.pptx
    6.1.2-wastewater-facility-case-study.pptx

Module 7 - Community EBS
    7.1-community-ebs.pptx
    7.1.1-cebs-case-study.pptx

Module 8 - Data Management
    8.1-ebs-data-management.pptx
    8.1.1-case-study.pptx
    8.1.2-case-study-data.xlsx
    8.2-event-management-systems.pptx
    8.2.1-ephem-demo.pptx
    8.3-sit_spot-reports.pptx
    M8-situation-report-template.docx
    M8-spot-report-template.docx
    M8-ephem-general-overview.pptx

Module 9 - Monitoring and Evaluation
    M9-evaluation-materials
        M9-bottleneck-enabler-focus-group-calculator.xlsx
        M9-bottleneck-enabler-focus-group.docx
        M9-data-export-template.xlsx
        M9-ebs-evaluation-literature-review.xlsx
        M9-evaluation-guidance.docx
        M9-evaluation-guidance.pdf
        M9-evaluation-protocol-template.docx
        M9-initial-evaluation-checklist.docx
        M9-multi-sector-bottleneck-enabler-focus-group-calculator.xlsx
        M9-multi-sector-bottleneck-enabler-focus-group.docx
        M9-suggested-evaluation-tables.xlsx
        M9-ebs-evaluation-question-pool.xlsx
    9.1-me.pptx
    9.1.1-me-case-study.pptx
    9.1.2-me-case-study-data.xlsx
    9.2-supportive-supervision.pptx
    M9-supportive-supervision-checklist.docx
    M9-annual-planning-checklist.docx
    M9-weekly-report-template.docx
    M9-monthly-quarterly-monitoring-report.docx
    M9-yearly-monitoring-report-template.docx

Supplemental Documents
    ebs-toolkit-materials-list
    ewar-assessment-tool.docx
    ewar-ebs-assessment-tool.docx
    tot-planning-checklist.docx
    tot-week1-agenda.docx
    tot-adaptation-week2-agenda.docx
    tot-pre-post-test.docx
```

| Module | Description | Link |
|---|---|---|
| 01 | EWAR Background | [/M1-ewar/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M1%20-%20EWAR) |
| 02 | EBS Overview | [/M2-EBS-overview/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M2%20-%20EBS%20Overview) |
| 03 | Considerations | [/M3-considerations/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M3%20-%20Considerations) |
| 04 | Hotline | [/M4-hotlines/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M4%20-%20Hotline) |
| 05 | Media Scanning | [/M5-media-scanning/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M5%20-%20Media%20Scanning) |
| 06 | Facility EBS | [/M6-facility-ebs/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M6%20-%20Facility%20EBS) |
| 07 | Community EBS | [/M7-community-ebs/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M7%20-%20Community%20EBS) |
| 08 | Data Management | [/M8-data-management-and-ems/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M8%20-%20Data%20Management) |
| 09 | Monitoring and Evaluation | [/M9-monitoring-and-evaluation/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/M9%20-%20M%26E) |
| — | Supplemental Materials | [/supplemental-docs/](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/tree/main/Supplemental%20Docs) |

> **Note:** Training of Trainer (ToT) materials are available in English, French, and Spanish, and are organized around the same 9 topic areas listed above, each with knowledge checks and interactive case studies. Email the EBS Unit if access to the other materials is needed. 

---

## EBS Modalities

The toolkit supports four core modalities, which can be implemented incrementally:

- **Hotlines** — voice, SMS, USSD, or social-media-based reporting channels for community members and stakeholders. Recommended as a **low-cost entry point** for countries beginning EBS implementation.
- **Media Scanning** — manual or automated (e.g., EIOS-based) monitoring of official and unofficial media sources, both national and international/cross-border.
- **Facility EBS (FEBS)** — signal detection by clinicians, laboratory staff, veterinarians, and other facility-based professionals, across human health, animal health, laboratory, and environmental facility types.
- **Community EBS (CEBS)** — detection and reporting by community health workers (CHWs), community animal health workers (CAHWs), and key informants (teachers, religious leaders, traditional healers, etc.).

Each modality follows the same detection → triage → verification → risk assessment → alert steps, adapted to the sources and workforce involved.

---

## Signal Development

Good signals are:

- **Sensitive rather than specific** — designed to catch the unexpected, not to duplicate known/notifiable disease lists.
- **Simple and memorable** — usable by non-specialists, including community members, without medical jargon.
- **Limited in number** — enough to be comprehensive without overwhelming reporters or the response system.
- **Non-redundant with IBS** — avoid linking EBS signals to conditions already tracked via routine indicator-based thresholds.
- **Reviewed periodically** — revised as risk profiles, outbreaks, and context change.

See `/M3 - Considerations/M3 - Signal Development Guidance.pdf` for universal and modality-/sector-specific example signal lists (human health, animal health, laboratory, environment, points of entry, congregate settings).

---

## Event Management

Every EBS implementation needs a functional signal/event tracking mechanism, whether a simple paper logbook or an electronic Event Management System (EMS):

- Logs must capture, at minimum: unique identifier, source, location, date of onset/detection/reporting, description, verification/risk-assessment outcomes, and response status.
- The system should support **secondary triage** during verification and enable **feedback loops** back to reporters at every level (community → local → intermediate → national).
- Where possible, connect the EMS to the team responsible for coordinating and executing response, so that alerts translate into timely action rather than sitting in a queue.

See `/M8 - Data Management/` for EMS considerations, including interoperability with IBS and cross-border/multisectoral data-sharing needs.

---

## Monitoring & Evaluation

M&E should be built into EBS design from the start, not added retroactively. Recommended components:

- Input, process/activity, output, outcome, and impact indicators (results-chain model)
- Routine monitoring (e.g., timeliness of verification, risk assessment, and notification) integrated into existing reporting workflows
- Periodic internal and external evaluations (formative, process, and summative)
- Supportive supervision visits with structured checklists
- An EBS scorecard for tracking programmatic maturity across surveillance, data systems, laboratory linkage, preparedness/response, legislation, financing, workforce, and structure

See `/M9 - M&E/` for indicator tables, evaluation plan templates, and scorecards.

---

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dghpebsunit-ux/USCDC_EBSToolkit.git
   cd USCDC_EBSToolkit
   ```
2. **Assess current capacity.** Use the EWAR/EBS assessment tools in `/Supplemental Docs/` to identify existing surveillance strengths and gaps before adding new components.
3. **Form a multisectoral technical working group.** Include human health, animal health, environment, and other relevant sectors to define priority events and a shared signal list.
4. **Choose a starting modality.** If resources are constrained, prioritize strengthening a hotline before scaling up CHW-dependent CEBS.
5. **Draft or adapt SOPs.** Start from the EBS SOP template and signal registers in `/M2 - EBS Overview/`.
6. **Set up an event log/EMS.** Ensure it links reporting sites to the team responsible for verification, risk assessment, and response.
7. **Train and supervise.** Use the ToT materials and supportive supervision checklist to build and sustain workforce capacity.
8. **Monitor and evaluate continuously.** Integrate M&E indicators from day one rather than retrofitting them later.

> Materials are organized to be used in workshops, self-paced learning, or facilitated training environments. See open [Issues](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/issues) for known gaps or planned additions, and [Releases](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/releases) for versioned toolkit snapshots.

---

## References

- WHO. *[Early Warning Alert and Response in Emergencies: An Operational Guide.](https://www.who.int/publications/i/item/9789240063587)* Geneva: World Health Organization; 2022.
- WHO. *[Early Detection, Assessment and Response to Acute Public Health Events: Implementation of Early Warning and Response with a Focus on Event-Based Surveillance (Interim Version).](https://www.who.int/publications/i/item/WHO-HSE-GCR-LYO-2014.4)* Geneva: WHO; 2014. (WHO/HSE/GCR/LYO/2014.4)
- Africa CDC. *[Event-based Surveillance Framework](https://africacdc.org/download/africa-cdc-event-based-surveillance-framework-2/)*, 2nd Edition. Addis Ababa: African Union/Africa CDC; 2023.
- Mercy K, Salyer SJ, Mankga C, Hedberg C, Zondo P, Kebede Y. [Establishing an early warning Event Management System at Africa CDC.](https://doi.org/10.1371/journal.pdig.0000546) *PLOS Digital Health.* 2024;3(7):e0000546.
- Crawley AW, Mercy K, Shivji S, Trowbridge D, Lofgren H, Manthey C, Kebede Tebeje Y, Clara AW, Landry K, Salyer SJ. [An Indicator Framework for Monitoring and Evaluation of Event-based Surveillance Systems.](https://doi.org/10.1016/S2214-109X(24)00034-2) *Lancet Global Health.* 2024;12(4):e707–e711.
- Mercy K, Salyer SJ, Aliddeki D, Tibebu B, Osman F, Amabo FC, Kwagonza Warren L, Ibrahim Buba M, Kebede Y. [Evaluating event-based surveillance capacity in Africa: use of the Africa CDC scorecard, 2022–2023.](https://pubmed.ncbi.nlm.nih.gov/37719793/) *Prev Med Rep.* 2023 Sep 9;36:102398.
- Ghai RR, Wallace RM, Kile JC, Shoemaker TR, Vieira AR, Negron ME, Shadomy SV, Sinclair JR, Goryoka GW, Salyer SJ, Behravesh CB. [A generalizable one health framework for the control of zoonotic diseases.](https://doi.org/10.1038/s41598-022-12619-1) *Sci Rep.* 2022;12:8588.
- Balajee A, Salyer SJ, Greene-Cramer B, Sadek M, Mounts AW. [The practice of event-based surveillance: concept and methods.](https://www.tandfonline.com/doi/full/10.1080/23779497.2020.1848444) *Global Security: Health, Science and Policy.* 2021;6(1):1–9.

For questions about the CDC EBS Toolkit materials specifically, contact the GSLDSB EBS Unit at **GSLDSEBS@cdc.gov**.

---

## Citation

If you use or adapt materials from this toolkit, please cite it as:

> US CDC. *EBS Toolkit* [Internet]. 2024. Available from: https://github.com/dghpebsunit-ux/USCDC_EBSToolkit

BibTeX:

```bibtex
@misc{cdc_ebs_toolkit,
  author       = {{US CDC}},
  title        = {EBS Toolkit},
  year         = {2024},
  publisher    = {GitHub},
  url          = {https://github.com/dghpebsunit-ux/USCDC_EBSToolkit}
}
```

---

## Contributing

Contributions, translations, and country-adapted examples are welcome via pull request to [dghpebsunit-ux/USCDC_EBSToolkit](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit). Please open an [issue](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/issues) describing proposed changes before submitting a pull request, especially for changes to signal lists, thresholds, or SOP templates, since these should be reviewed by public health/surveillance subject matter experts before adoption.

## Contact

Maintained by the CDC GSLDSB EBS Unit:

- Emily Weston — csi7@cdc.gov
- Stephanie Salyer — wig9@cdc.gov
- General mailbox — GSLDSEBS@cdc.gov

For questions about this repository specifically, open an issue at [github.com/dghpebsunit-ux/USCDC_EBSToolkit/issues](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit/issues).

## License

[EBS Toolkit](https://github.com/dghpebsunit-ux/USCDC_EBSToolkit) © 2024 by [US CDC/CGH/DGHP/GSLDSB/SET/EBS Unit](https://example.com) is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

Materials adapted from WHO and Africa CDC publications may carry their own licensing/attribution requirements (e.g., CC BY-NC-SA 3.0 IGO for WHO materials) — verify and retain original attribution notices when redistributing derived content.
