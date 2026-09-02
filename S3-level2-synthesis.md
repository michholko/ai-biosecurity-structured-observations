# Level 2 Synthesis — Testing Five Candidate Propositions

Conducted per Section 6 process discipline: Level 1 is locked. Candidates 1–5 are tested against it with explicit counterevidence requirements. Prior Patterns A–E are not the starting frame — they are checked at the end as secondary hypotheses.

One procedural note: the coding and synthesis across this project have been conducted with AI assistance throughout. The observations are grounded in full-text reads of all 14 papers, but the interpretive judgments below are the analyst's and should be checked against primary sources before submission.

---

## Candidate 1 — Configuration dependence

**Proposition tested:** Biosecurity-relevant capability, vulnerability, and protection are not fully attributable to individual components; they depend on how components are configured and interact.

### Evidence matrix

| Paper | Evidence for configuration dependence | E-level | Evidence basis | Genuine counterexample? |
|---|---|---|---|---|
| AST (A1) | Latent capability depends on integration of computational direction + remote operation + multi-instrument coordination; split-order attack invisible to facility-level classification | E1 | conceptual | No |
| Hanke (A2) | Governance located at funder-developer-institution relationship, not at model | E2 | normative-policy | No — but capability itself framed as component-level |
| Siddiqui (A3) | Protective capability primarily assessed as property of compound + concentration; environmental parameters secondary | E1 | empirical | **Partial counterexample** — protective capability is predominantly component-level |
| Aveggio (A4) | Security and innovation as co-designed project properties, not component properties | E1 | normative-policy | No |
| KYS (A6) | Protective capacity from institution + researcher + tool-host configuration; no single tier sufficient | E2 | conceptual | No |
| Brackmann (A7) | Defense-in-depth — layers are complementary but described as redundant rather than non-additive; borderline | E1 | conceptual | Borderline — redundancy ≠ configuration-dependence strictly |
| Sawaya (A8) | Privacy property achieved by pooling configuration, not by any single sample or method in isolation | E1 | empirical | No |
| Wang (A9) | Risk from mismatch between generation and evaluation rates — property of the pipeline relationship | E1 | conceptual | No |
| Luhachack (A10) | Explicit: "no single layer determines risk independently"; interfaces may matter more than any layer | E1 | conceptual | No |
| Bloomfield (B2) | Capability framed as model-level property; intervention relational (government-developer) | E1 | normative-policy | **Partial counterexample** — capability framed at component level even though intervention is relational |
| ABLE (B3) | Orchestration capability = LLM + specialized BAIMs + task context; not attributable to any one | E1 | empirical | No |
| RefusalBench (B4) | Risk discrimination = property of model/access-path configuration, not raw refusal behavior | E2 | empirical | No |
| Wittmann (B1) | Vulnerability = relationship between design-tool output and screening-tool limitation | E2 | empirical | No |
| ABC-Bench (B5) | Physical execution = LLM + human + robot + biological material; capability not attributable to AI alone | E1 | empirical | No |

### Finding

**Supported, with hedging.** 12 of 13 coded papers locate at least one biosecurity-relevant property in a configuration rather than a single component. Two partial counterexamples warrant explicit acknowledgment: A3 (Siddiqui & Pannu) assesses a compound's inherent properties as the primary analytic object — a genuine component-level treatment; B2 (Bloomfield et al.) frames *capability* as a model-level property even while proposing a relational intervention. Neither paper contradicts the proposition so much as it qualifies it: component-level analysis is not absent from the field, but it appears predominantly in papers examining either physical substances or model capabilities in isolation, rather than the AI-bio pipeline as a whole.

**Revised proposition for the commentary:** Across the coded corpus, biosecurity-relevant capability, vulnerability, and protection are most often characterized as properties of configurations and interactions among components rather than properties of any single component alone — though component-level analysis remains present, particularly for physical disinfection and model-capability assessments.

---

## Candidate 2 — Proxy–target decoupling

**Proposition tested:** Across technically distinct settings, established security proxies may become less reliable indicators of the underlying properties they are intended to govern as AI-enabled systems change the relationship between proxy and target.

### Evidence matrix

| Paper | Proxy in use | Target property | Mechanism of decoupling | E-level | Evidence basis |
|---|---|---|---|---|---|
| AST (A1) | Declared/handled inventory | Latent production capability | Automated integration creates capability beyond declared scope | E1 | conceptual |
| Brackmann (A7) | Sequence homology to known threats | Biological function/hazard | AI-designed proteins can retain hazardous function with low sequence similarity | E1 | review-derived |
| KYS (A6) | Content/output characteristics | Intent, behavior, context | Biological function not reliably inferable from output alone | E1 | empirical |
| RefusalBench (B4) | Refusal rate | Risk discrimination | High refusal rate and accurate risk discrimination empirically uncorrelated across providers | E1 | empirical |
| Wang (A9) | Computational prediction of fitness | Actual biological behavior | Ground-truth validation may require physical synthesis — itself the hazardous step | E1 | conceptual |
| Wittmann (B1) | Sequence similarity | Functionally relevant synthetic homolog | AI redesign produces sequence-divergent variants that evade screening | E1 | empirical |

**Papers not engaging with proxy-target measurement validity (null on this dimension):**
A2, A3, A4, A8, A10, B2, B3, B5 — none of these argue existing proxies are reliable; they simply don't address measurement validity.

### Counterevidence check

Is there any paper arguing that an existing proxy reliably tracks its target in the face of AI-enabled system changes? **No paper in either corpus makes this argument.** The papers that don't engage with the issue are silent rather than contradicting it. A2 (Hanke et al.) and A4 (Aveggio et al.) propose governance and benchmarking improvements that imply current proxies are insufficient — consistent with the proposition rather than contradicting it. ABLE (B3) and ABC-Bench (B5) develop new measurement instruments, implying current ones are inadequate.

### Finding

**Strongly supported.** Six papers, across different technical domains and disciplinary registers, independently describe a case in which an established security proxy has become or is becoming an unreliable indicator of its target property. None cite each other on this specific point; the convergence is across independently produced findings. All six instances are E1 (author-explicit on the underlying finding, even if "proxy-target decoupling" is the analyst's cross-domain label). No paper in the corpus contradicts the proposition.

**The mechanism is specific and worth stating precisely:** in each case, the proxy fails not because it was poorly chosen at the time of design, but because AI-enabled systems change the *relationship between proxy and target* — generating designs, capabilities, or behaviors that satisfy the proxy condition while evading the target property. This is distinct from ordinary measurement error.

**Revised proposition for the commentary:** Across six technically distinct settings, established security proxies — declared inventory, sequence homology, refusal frequency, content characteristics, computational fitness predictions — have become or are becoming unreliable indicators of the properties they are intended to govern. In each case, the mechanism is not measurement imprecision but AI-enabled disruption of the proxy-target relationship itself.

**Relationship to Patterns A–E check:** this finding substantially incorporates original Pattern A (convergent failure mode) and enriches it — Pattern A described the surface phenomenon (screening built on a proxy that doesn't hold), this finding names the underlying mechanism (proxy-target relationship disrupted by AI-enabled systems) and adds three more domains (RefusalBench, Wang, KYS) not in Pattern A.

---

## Candidate 3 — Selective observability

**Proposition tested:** Security depends not simply on increasing information availability, but on determining what information should be observable, to whom, at what resolution, and at what stage of a workflow.

### Evidence matrix — three observability configurations

**Configuration A: More observability needed — current gaps**

| Paper | Gap identified | E-level |
|---|---|---|
| AST (A1) | Incoming biological materials not sequenced; protocol-level screening insufficient | E1, empirical |
| KYS (A6) | Content/output observable; behavioral pattern and institutional context not currently monitored | E1, empirical |
| Luhachack (A10) | Stack-level capability indicators not currently tracked; if-then dashboard proposed to fill gap | E1, normative-policy |
| RefusalBench (B4) | Refusal rate observable; risk discrimination not currently measured as standard | E1, empirical |
| Wang (A9) | Biological behavior of AI-generated designs not safely observable before physical synthesis | E1, conceptual |

**Configuration B: Selective/reduced observability as safety mechanism**

| Paper | Mechanism | E-level |
|---|---|---|
| Sawaya (A8) | Deliberate destruction of sample-level attribution while preserving population-level signal | E1, empirical |

**Configuration C: Controlled information flow within governance structures**

| Paper | Mechanism | E-level |
|---|---|---|
| Hanke (A2) | Sensitive capability information should flow within review/governance structures, not publicly | E1, normative-policy |
| Aveggio (A4) | Provenance/metadata flows within distributed workflow — tracked but not unrestricted | E2, conceptual |

### Counterevidence check

Does any paper argue for maximal transparency without qualification? **No.** A4 (Aveggio et al.) comes closest — capability benchmarking as shared community information — but frames this within a structured governance context, not as unrestricted disclosure. B2 (Bloomfield et al.) proposes government evaluation authority, which implies controlled rather than open information flows.

### Finding

**Supported, with an important refinement.** The corpus does not divide cleanly into "papers that want more observability" and one exception (Sawaya). A more accurate characterization is that the corpus implicitly assumes calibrated observability — observability structured by purpose, recipient, resolution, and workflow stage — without making this assumption explicit. Three different configurations appear: observability gaps that need closing (5 papers), deliberate opacity as safety mechanism (1 paper), and controlled flow within governance structures (2 papers). No paper argues that maximizing information availability is equivalent to maximizing security.

**A second-order observation (E3 — synthesized):** the implicit norm of calibrated observability may be more consequential than any of its specific instances, because it suggests that "transparency" and "security" are not synonymous — a proposition with direct relevance to bioethics and governance design. Who has legitimate claim to know what, at what resolution, decided by whom, is a question this field is answering implicitly without having asked it explicitly.

**Revised proposition for the commentary:** Security in AI-enabled biosecurity contexts requires calibrated observability — determining what information should be visible, to whom, at what resolution, and at what workflow stage — rather than simply maximizing information availability. This norm appears implicitly across the corpus in at least three distinct configurations, without having been stated as a principle.

---

## Candidate 4 — Interface-level intervention

**Proposition tested:** Many proposed or demonstrated safeguards operate not on the underlying AI or biological component itself, but at interfaces through which capability is accessed, translated, combined, observed, or acted upon.

### Evidence matrix

| Paper | Intervention point | Interface type | Component-level intervention present? |
|---|---|---|---|
| Hanke (A2) | Developer–institution–funder relationship, pre-development | Relational/institutional | No |
| Siddiqui (A3) | Glycol vapor compound deployed in indoor space | Physical/component | **Yes — primary component-level intervention** |
| Aveggio (A4) | Project-design architecture; funding mechanisms | Institutional | No |
| KYS (A6) | Researcher–institution–tool relationship; behavioral monitoring | Relational/institutional | Partly (Tier II content screening) |
| Brackmann (A7) | Layered screening across design/screening interfaces; model-level safeguards also proposed | Mixed | **Yes — model-level safeguards proposed alongside interface-level** |
| Sawaya (A8) | Data-sharing transformation point | Technical/informational | No |
| Luhachack (A10) | Interfaces across capability stack; if-then dashboard across layers | Technical/governance | No |
| Bloomfield (B2) | Government–developer regulatory relationship | Regulatory/relational | No |
| Wittmann (B1) | Design-tool/screening-tool interface; patches deployed at screening layer | Technical | No |
| ABLE (B3) | No intervention proposed — measurement paper | n/a | n/a |
| RefusalBench (B4) | Metric reform — evaluating at access-path level | Meta-level | No |
| ABC-Bench (B5) | No intervention proposed — measurement paper | n/a | n/a |
| AST (A1) | Facility capability/configuration classification | Operational | Partly — tiering operates at facility level rather than interface per se |
| Wang (A9) | No specific intervention proposed — diagnostic paper | n/a | n/a |

### Counterevidence check

Papers proposing intervention at the component itself (model weights, a specific compound, a single piece of equipment):
- **A3 (Siddiqui & Pannu):** clear component-level intervention — the compound's properties are the safety mechanism
- **A7 (Brackmann et al.):** model-level safeguards proposed alongside interface-level screening — genuinely mixed
- **A1 (AST):** operates at facility-level classification, which is closer to configuration-level than interface-level strictly

### Finding

**Supported with important caveats.** Of the 11 papers that propose interventions, 8 locate the primary intervention at an interface, relationship, or configuration level rather than the component itself. The three partial counterexamples are meaningful: A3 is a genuine component-level intervention (physical disinfection); A7 proposes a mix (model safeguards + interface screening); A1 operates at a facility configuration level that is intermediate between component and interface. The finding should not be overstated as "interventions are never component-level" — the more defensible version is "proposed interventions are disproportionately located at interfaces and relationships, rather than exclusively at the underlying artifacts."

**A distinction worth preserving in the commentary:** papers that describe a risk at the component level (B2 Bloomfield) still tend to propose interface-level or relational interventions (government-developer regulation). This split — component-level diagnosis, interface-level remedy — appears in several papers and is itself worth noting.

**Revised proposition for the commentary:** Across the coded corpus, proposed and demonstrated safeguards are disproportionately located at interfaces, relationships, and configuration points — the developer-funder relationship, the researcher-institution link, the design-screening interface, the data-sharing transformation — rather than exclusively at the underlying AI models, biological agents, or laboratory instruments. Component-level intervention persists in the corpus (particularly for physical disinfection and model-level safeguards) but is not the dominant pattern.

---

## Candidate 5 — Compositional protection (speculative)

**Proposition tested:** Protective capacity, like hazardous capability, may be compositional — emerging from interacting safeguards rather than from any single control.

### Evidence matrix — applying all four emergence criteria

| Paper | Candidate compositional protective effect | Criterion 1 (not single component) | Criterion 2 (interaction-dependent) | Criterion 3 (altering relationship changes protection) | Criterion 4 (system-level property) | Clears all 4? |
|---|---|---|---|---|---|---|
| KYS (A6) | Three-tier combination — institutional verification + content screening + behavioral monitoring | Yes — Tier II explicitly insufficient alone | Yes — tiers described as complementary | **Not demonstrated** — asserted as design principle | Yes | No — clears 1, 2, 4 |
| Brackmann (A7) | Layered/defense-in-depth safeguards | Yes — no single layer sufficient | Redundant rather than non-additive — unclear | Not tested | Possibly | **No** — redundancy ≠ emergence |
| Aveggio (A4) | Innovation + security infrastructure + community participation | Yes | Yes — co-designed | Not tested empirically | Yes — at project level | No — clears 1, 2, 4 |
| Wittmann (B1) | Design-tool testing + screening + feedback/patching cycle | Yes | Yes — feedback loop between components | Arguably yes — removing the feedback would remove the improvement, but not tested by varying it | Yes | Closest to clearing all 4, but criterion 3 is inferred not demonstrated |

### Finding

**Not demonstrated in the strong sense; negative finding is informative.** No paper in the coded corpus clearly demonstrates a protective effect that meets all four emergence criteria — specifically, no paper varies the relational configuration experimentally and shows that altering a relationship between safeguard components materially changes the protective property. The closest case is Wittmann et al.'s patching cycle (B1), where the feedback loop between design-tool testing and screening update seems necessary to the improvement — but this isn't tested by removing the feedback.

**The negative finding itself is noteworthy and should be stated:** the corpus describes AI-enabled biological risks as increasingly system-level and configuration-dependent (Candidates 1 and 2 above), while proposed safeguards are more often described as layered/redundant (additive) rather than compositional (non-additive). Risk is already being characterized as emergent; protection has not yet been. This gap may be a productive research direction for Volume II rather than a flaw in the current literature.

**Revised statement for the commentary:** While AI-enabled biological risks are increasingly characterized as configuration-dependent in this literature, the protective responses documented here are more often described as layered or defense-in-depth — that is, as redundant rather than compositional. Whether protective properties can emerge from configurations of safeguards in a way analogous to how capabilities emerge from configurations of tools remains an open empirical question, and a candidate research direction.

---

## Boundary-dependence test

**Question tested:** Does changing the system boundary materially change what capability, risk, or intervention becomes visible?

### Evidence

| System boundary used | What becomes visible | What becomes invisible | Paper |
|---|---|---|---|
| Single model | Model-level capability/safeguard | Pipeline behavior; relational context | B2 (Bloomfield) |
| Agentic workflow (LLM + tools) | Orchestration capability | Physical execution; human contribution | B3 (ABLE) |
| Agentic workflow + human + robot | Physical execution; human dependency | Population-level effects | B5 (ABC-Bench) |
| Single facility | Latent production capability | Split-order attack across facilities | A1 (AST) — authors acknowledge this |
| Multiple facilities | Aggregate capability from split-order | Within-facility compliance | A1 (AST) — authors note the gap |
| Institutional ecosystem | Identity/accountability intervention | Computational mechanism | A6 (KYS), A4 (Aveggio) |
| Full capability stack | Interface governance as strategic point | Within-component properties | A10 (Luhachack) |
| Data pool (not individual sample) | Population-level signal | Individual-sample attribution | A8 (Sawaya) |

### Finding

**Boundary choice is substantively consequential, not merely methodological.** At least three papers provide within-paper or within-corpus evidence that boundary expansion or contraction changes what becomes analytically visible:

1. AST (A1) explicitly names its own boundary limitation — the facility-level tier system cannot see a split-order attack that no single node crosses — demonstrating within one paper that the boundary choice determines the visible risk.
2. ABC-Bench (B5) crossing the digital/physical boundary to include physical robot execution reveals a human-mediated step that would be invisible in a purely computational analysis — and that human step is constitutive of the capability.
3. KYS (A6) extending the boundary to include institutional relationships makes identity-based intervention visible where content-based analysis alone could not.

**This finding has methodological implications for the commentary itself:** the structured-observation instrument's "System boundary" dimension is not merely descriptive — it is a diagnostic tool for identifying what each paper's analytical choices render visible or invisible. This is worth stating explicitly in the write-up.

---

## Secondary check: What survives of Patterns A–E?

Patterns A–E were the original draft synthesis from the pre-systematic pass. Checking each against the Level 2 findings:

| Original pattern | Status after Level 2 | Disposition |
|---|---|---|
| Pattern A — Convergent failure mode (three papers, same proxy decoupling) | **Subsumed and strengthened** — Candidate 2 (proxy-target decoupling) extends this to 6 papers across more domains and names the mechanism more precisely | Retire Pattern A; replace with Candidate 2 |
| Pattern B — Relocating intervention to relationships | **Subsumed and qualified** — Candidate 4 (interface-level intervention) covers this but with counterexamples acknowledged | Retire Pattern B; replace with Candidate 4 |
| Pattern C — Expanding the unit of analysis | **Reframed** — boundary-dependence test is a more precise version of this observation, focused on what becomes visible at each boundary rather than "bigger is better" | Retire Pattern C; replace with boundary-dependence test |
| Pattern D — Evaluation bottleneck | **Subsumed** — Wang et al.'s specific finding is now captured under Candidate 2 (proxy-target decoupling) and Candidate 3 (calibrated observability) | Retire Pattern D as standalone; retain Wang et al. as primary evidence in Candidates 2 and 3 |
| Pattern E — Counter-pattern (Sawaya) | **Promoted** — now the pivot of Candidate 3 (selective observability); no longer a mere counter-example but the key paper distinguishing "more observability" from "calibrated observability" | Promote into Candidate 3; no longer treated as a counter-pattern |

**Summary:** None of Patterns A–E are wrong, but all five are either subsumed, qualified, or reframed by the Level 2 findings. The Level 2 findings are more precise (Candidate 2 names a mechanism, not just a phenomenon), more defensible (counterexamples explicitly acknowledged), and more interesting (the negative finding on Candidate 5 is more useful than a forced positive would have been).

---

## The synthesis statement for the commentary

The following is the candidate intellectual payoff of the Level 2 pass, stated as a proposition for the commentary to argue and defend:

> **AI-enabled biosecurity is increasingly a problem of system configuration:** capabilities, vulnerabilities, protective effects, and the reliability of the signals used to govern them depend on how components are arranged, what flows across their interfaces, and where analytical boundaries are drawn — not on the properties of any single component alone.

Three consequences follow for the field:

1. **Evaluation** should assess composed systems and workflows, not only individual models, tools, or facilities.
2. **Safeguards** are disproportionately effective when located at consequential interfaces — relationships, access points, transformation stages — rather than exclusively at the underlying artifacts.
3. **Governance** should address observability and information/material/action flows as first-class objects, not only regulate access to artifacts, because what can be seen — and by whom, at what resolution — determines what can be governed.

And then relational biosecurity is the theoretical interpretation of these observations — not the premise used to generate them. That sequencing is the methodological contribution: the field is already behaving as though this proposition were true; the structured-observation instrument makes it possible to show that, across independent papers using different vocabularies, the same underlying structure keeps appearing.
