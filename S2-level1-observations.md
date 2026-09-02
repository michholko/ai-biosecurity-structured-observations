# Level 1 Structured Observations — LOCKED August 30, 2026

**Status: LOCKED.** No further changes to observations. If a factual coding error is identified after this date, it is documented as a named correction with a reason rather than a silent edit. Synthesis (Level 2) was conducted on the basis of this locked document.

All fourteen papers in Corpus A and Corpus B have been coded. A5 (Holko) excluded from corpus by design — used as analytic lens only. Framework v2 applied throughout.


Revised per independent review. Changes applied throughout:
- "Information flows" renamed to "Flows" (now covers information, instructions, materials, physical actions)
- E1/E2 distinction sharpened: E2 is the expected code when dimension framing is the analyst's translation even if underlying facts are explicit; E1 reserved for cases where the paper identifies the phenomenon in substantially the same terms
- All cross-paper comparative statements removed and moved to the separate Candidate Synthesis Observations file
- Human contribution identified explicitly where system-level capability claims appear
- Paper-specific corrections noted inline

Coded per Section 6 process discipline: observation only. No cross-paper patterns named in this document.

---

# CORPUS A

## A1. Smith, Hanke, Moritz, Gillum & Pannu — Automated Laboratory Security Tiers

- **Unit of observation:** The integrated automated biological laboratory — a facility whose biosecurity-relevant properties emerge from the combination of computational direction, remote operation, and multi-instrument coordination. [E2, conceptual — "automated biological laboratory" is the analyst's unit label; the authors define facility tiers by combinations of these three properties]
- **Relationships:** Customer/user↔facility (order screening); employee↔IT/OT systems (insider threat pathway); attacker↔control systems (cyberattack pathway); individual facility↔order-splitting attacker across multiple facilities. [E2, conceptual]
- **Flows:** Protocol and instruction flows into automated systems (computational); physical samples and materials into the facility (material); IT/OT control signals between digital orchestration and physical instruments (computational→physical-action); shipped biological materials out of the facility (material); telemetry from instruments back to control systems (informational). The incoming-samples gap is explicit: no current requirement to sequence materials on arrival. [E1/E2 mixed — material and computational flows are the analyst's framing; the observational gap on incoming sequencing is E1, author-explicit]
- **Capability:** Latent capability — what the facility could produce if its systems were compromised, explicitly distinguished from declared/handled-agent inventory. [E1, conceptual — authors use this term directly]
- **Perturbation:** Malicious external orders; insider access exploitation; cyberattack on control systems; non-adversarial protocol error/miscalibration. [E1, conceptual]
- **Buffers:** Tacit knowledge requirements for protocol establishment; human oversight (authors note this degrades as automation scales); sector's current small size; cost barriers to legitimate access. [E2, conceptual — authors describe these factors without calling them "buffers"]
- **Intervention:** Automated Security Tier (AST) classification system, tiering facilities by risk level keyed to latent capability rather than declared inventory alone. [E1, normative-policy]
- **Observability:** Explicitly poor — no requirement to sequence incoming materials; authors' own interviews characterize protocol-level screening as insufficient as the sole detection mechanism. [E1, empirical]
- **System boundary:** Single facility as primary unit of analysis; authors explicitly acknowledge the framework does not fully address split-order attacks in which multiple individually low-tier facilities collectively enable a higher-capability outcome. [E1, conceptual]

---

## A2. Hanke, Rath, Cicero, Inglesby & Pannu — Upstream risk-benefit review

- **Unit of observation:** The pre-development BAIM decision and review process, with the proposed model as the object being governed rather than the model itself. [E2, conceptual — the authors propose a process for deciding whether/how BAIM development should proceed; "unit of observation" as a decision-process rather than an artifact is the analyst's framing]
- **Relationships:** Developer↔institutional review body↔funder — the paper locates governance at this three-way relationship. [E2, normative-policy]
- **Flows:** Sensitive biological data → model training (informational); developer capability/risk disclosures → institutional/funder review (informational/institutional); review decisions → developers and funders (institutional); model/data/code/API access → downstream users, differentiated by access pathway (informational — the paper distinguishes open weights, data, code, APIs, and managed access because what can flow outward changes risk). [E1/E2 mixed — the access-pathway differentiation is E1; the flow framing is E2]
- **Capability:** Enhancing transmissibility, virulence, or immune evasion; circumventing existing screening via functional-homolog generation. [E1, conceptual]
- **Perturbation:** Open-weight release (irrevocable once distributed); fine-tuning reintroducing filtered capabilities; jailbreaking. [E1, conceptual]
- **Buffers:** Data filtering, likelihood suppression, managed access/trusted research environments, non-disclosure of misuse-relevant methodological detail. [E1, conceptual]
- **Intervention:** Pre-development risk-benefit review located at the funder-developer-institution relationship, before a model exists; proposed anonymized decision registry to make review reasoning comparable over time. [E1, normative-policy]
- **Observability:** Currently ad hoc — no standardized criteria; high inter-reviewer subjectivity ("reasonably anticipated" is doing unexamined work); proposed registry is specifically designed to make review reasoning observable and consistent over time. [E1, conceptual/normative-policy]
- **System boundary:** Wider than a single model — includes funders, IRBs, and international coordination bodies as constitutive parts of the governance system. [E2, normative-policy]

---

## A3. Siddiqui & Pannu — Glycol vapor pathogen disinfection

*Note: the independent review raised a genuine question about whether this paper should be in the coded corpus at all, given that its AI content is prospective rather than demonstrated. It is retained here as a partial-fit test of the instrument — a paper with limited AI content is a useful boundary case — but this should be disclosed in the write-up rather than smoothed over. Final decision on inclusion deferred to the author.*

- **Unit of observation:** The indoor built environment as an integrated system — room, HVAC, occupants — not the disinfectant compound alone. [E2, empirical]
- **Relationships:** Glycol vapor↔respiratory droplet↔pathogen structure, mediated by environmental parameters (humidity, temperature, ventilation, filtration). [E2, empirical]
- **Flows:** Airborne material flows (glycol vapor, respiratory droplets, inactivated pathogens) through indoor space (material); no current closed information/sensor loop — real-time AI-based sensing is described as conceptual future work, not implemented. [E1/E2 — the null on information flows is E1 author-explicit; the material flow framing is E2]
- **Capability:** Pathogen inactivation, highly class- and environment-dependent; AI-enabled real-time control is proposed but not yet demonstrated. [E1, empirical]
- **Perturbation:** Changes in relative humidity, temperature, ventilation/filtration rate; degradation byproducts under real heating conditions. [E1, empirical]
- **Buffers:** GRAS safety status of propylene glycol; occupational exposure limits derived from theatrical-fog literature (authors acknowledge this is an imperfect proxy). [E1, review-derived]
- **Intervention:** Deployment of glycol vapor as an ambient disinfection method; AI/ML-based real-time control proposed as future addition but not implemented. [E1, conceptual — proposed, not demonstrated]
- **Observability:** Weak — chamber-derived efficacy data does not reliably translate to occupied real-world buildings; authors explicitly call for AI/ML-based sensing to close this gap. [E1, empirical]
- **System boundary:** Single indoor space; population-level or building-to-building deployment not addressed. [E1, empirical]

---

## A4. Aveggio, Carter, Mukundan, Cameron & Guerra — Aligning innovation and security

- **Unit of observation:** The intervention/project architecture for AI-enabled biotechnology — data infrastructure, metadata standard, or benchmarking initiative — not a single tool or policy. [E2, normative-policy]
- **Relationships:** Funder↔developer↔security community, formalized via a four-part design pattern (CHALLENGE/STRUCTURE/APPROACH/COMMUNITY). The paper explicitly rejects innovation-vs-security as an unavoidable tradeoff and designs projects in which the two reinforce each other. [E2, normative-policy]
- **Flows:** Contextual metadata (provenance, versions, operations, inputs, user identity, chain-of-custody) flowing alongside AI-generated outputs and propagated across distributed workflows and teams (informational/institutional — Case Study 2); capability benchmark results flowing as shared, contestable information across the community rather than remaining private developer knowledge (informational/institutional — Case Study 3). [E2, conceptual]
- **Capability:** Capability benchmarking as a shared, contestable governance object; currently this information is private to developers. [E2, normative-policy]
- **Perturbation:** Underinvestment in security infrastructure; retrofitting security after a system is built — the STRUCTURE principle names this explicitly as a failure mode. [E1, conceptual]
- **Buffers:** Tiered access (APPROACH principle). [E1, normative-policy]
- **Intervention:** The full four-part design pattern applied at project-design stage, before deployment; Case Studies 2 and 3 as specific instantiations. [E1, normative-policy]
- **Observability:** Central concern — Case Study 3 targets the current lack of shared, standardized capability information; Case Study 2 targets traceability and provenance of tool use across distributed teams. [E2, conceptual]
- **System boundary:** Funders, publishers, institutions, and "the community" treated as constitutive actors. [E2, normative-policy]

---

## A5. Holko — Toward relational biosecurity

*Excluded from corpus per positionality decision. No entry.*

---

## A6. Feldman, Feldman & Anton — Know your scientist

- **Unit of observation:** The researcher-tool relationship situated within an institutional trust network. [E2, conceptual — "researcher-tool relationship" is the analyst's relational framing; authors describe a three-tier governance architecture but don't characterize it this way]
- **Relationships:** Institution↔researcher (verification and vouching, Tier I); researcher↔model/tool (use patterns monitored, Tier III); tool host↔monitoring layer↔institution (behavioral data distribution). [E2, conceptual]
- **Flows:** Three distinct flows: institution→tool host (identity and legitimacy information, institutional); researcher→model (requests and use, computational); host→monitoring layer and institution (output and longitudinal behavioral data, informational). The whole architecture depends on distributed information exchange across these three relationships. [E2, conceptual]
- **Capability:** Protein design and structure prediction tools where "reliable function prediction remains beyond reach" — authors explicit that content is often unknowable in advance, which motivates relocating governance to the behavioral/identity layer. [E1, empirical]
- **Perturbation:** A user whose declared purpose doesn't match access pattern; functionally dangerous sequences non-homologous to known threats (evading Tier II alone). [E1, conceptual]
- **Buffers:** Institutional accountability — an institution has skin in the game for researchers it vouches for; buffering through relationship rather than through technical control. [E2, normative-policy]
- **Intervention:** The full three-tier KYC framework, modeled on AML/KYC in finance and translated into biosecurity context. [E1, normative-policy]
- **Observability:** Authors argue content-based screening is observationally blind by construction and relocate observability to identity, behavioral pattern, and institutional context — layers where detection is actually achievable. [E2, conceptual]
- **System boundary:** Sector-wide trust network (institutions, model hosts, funders), not a single tool or laboratory. [E2, normative-policy]

---

## A7. Brackmann, Reiners, Hoogendoorn & Moser — Protein design and biological security

- **Unit of observation:** The AI-enabled protein-design and screening workflow — design models, output screening, structure-based detection, watermarking, and model-level safeguards as an integrated system. [E2, review-derived — the paper is a mini-review of this ecosystem; "unit of observation" as the workflow is the analyst's framing]
- **Relationships:** Sequence similarity is used as a proxy for functional similarity in existing screening; generative protein design weakens the reliability of that proxy by generating functionally relevant sequences with low sequence homology to known threats. [E2, review-derived — "decoupled" was the prior framing; this is more precise: the proxy relationship has become unreliable, not simply gone]
- **Flows:** Generated sequence/design → screening system → risk classification/access decision (computational→informational); potentially logged access and encrypted sequence logs at output. Screening pipeline is largely one-directional with no current feedback loop from screening results back into design-tool safeguards. [E2, empirical/review-derived]
- **Capability:** De novo protein generation for therapeutics and vaccines, dual-use by construction; authors cite SKYCovione as a real beneficial application to ground the dual-use framing empirically. [E1, empirical]
- **Perturbation:** A sequence engineered to be functionally hazardous but sequence-divergent from known toxins — the specific evasion mode enabled by AI-assisted design. [E1, empirical]
- **Buffers:** Layered mitigation — sequence screening plus structure-based detection plus watermarking plus model-level safeguards, explicitly defense-in-depth rather than a single control. [E1, conceptual]
- **Intervention:** Proposed improvements to layered screening; no single proposed fix, explicitly redundancy-based. [E1, normative-policy]
- **Observability:** The paper's core finding is an observability failure: homology-based screening cannot see functionally hazardous AI-designed sequences that are sequence-divergent from known threats. [E2, review-derived — "observability failure" is the analyst's framing; authors describe the limitation in technical terms]
- **System boundary:** AI-enabled protein-design and screening ecosystem as the analytical scope. [E2, review-derived]

---

## A8. Sawaya, Lo, Li, Hovde & Chain — Safely sharing dual-use genetic data

- **Unit of observation:** The genetic data pool — reads mixed across multiple samples — rather than any individual sample or sequence. [E2, empirical]
- **Relationships:** Read↔sample attribution is the relationship deliberately severed by the method; population-level signal↔individual-level attribution are deliberately decoupled. [E2, empirical]
- **Flows:** Genetic reads are deliberately transformed before sharing — reads from multiple samples are pooled, sample-linked metadata are removed, and the pooled dataset is transmitted in a form that preserves population-level information while disrupting sample-level attribution. The method explicitly changes what is preserved and what is lost as data moves through the sharing pipeline. [E1/E2 — pooling mechanics are E1; "what is preserved and lost" framing is E2, empirical]
- **Capability:** Full pathogen reconstruction from shared data — the capability the method is designed to deny while preserving epidemiological utility. [E1, empirical]
- **Perturbation:** A malicious actor with access to the pooled dataset attempting reconstruction. [E1, conceptual]
- **Buffers:** Molecular-cryptography-inspired pooling; the buffer is mathematical/statistical (theoretically proven privacy gain from pooling) rather than institutional or access-based. [E1, empirical/modeled]
- **Intervention:** The pooling method itself, applied at the data-sharing infrastructure stage before transmission. [E1, empirical]
- **Observability:** The paper deliberately decreases observability at the individual-sample level as the safety mechanism, while preserving it at the population level — a safety-through-selective-opacity approach. [E2, empirical — "observability" framing and the preservation/opacity distinction are the analyst's]
- **System boundary:** Data-sharing infrastructure across institutions and jurisdictions. [E2, conceptual]

---

## A9. Wang, Huot, Zhang, Jiang, Shakhnovich & Esvelt — Without safeguards, AI-biology integration risks accelerating future pandemics

- **Unit of observation:** The integrated AI-biology pipeline — protein language models coupled to automated experimentation — treated as a single accelerating system. [E2, conceptual]
- **Relationships:** The "evaluation bottleneck" locates risk in a mismatch between generation capability and validation capability — a rate-mismatch relationship between two connected parts of the same pipeline. [E2, conceptual — "evaluation bottleneck" is the authors' term; "rate-mismatch relationship" is the analyst's framing]
- **Flows:** A closed feedback loop: model-generated designs → experimental selection → synthesis/build → wet-lab measurement → experimental data → model training/update → new experimental selection. The authors are explicit that new experimental data update the model and drive the next cycle. This is a mixed informational-material-physical-action flow with feedback. [E1/E2 — the closed loop is E1 author-described; "mixed informational-material-physical-action" tagging is E2]
- **Capability:** Active-learning-driven protein fitness exploration at orders-of-magnitude higher throughput than manual work, with lowered expertise requirements. Human contribution: researchers remain involved in experimental setup and validation decisions, though the paper's concern is precisely that this human contribution is being compressed. [E1, empirical/modeled]
- **Perturbation:** A model generating a high-fitness, high-risk variant with no cheap way to distinguish plausible-and-wrong from plausible-and-right before physical synthesis. [E1, conceptual]
- **Buffers:** Largely absent — authors argue existing regulatory measures are globally insufficient for AI-specific risks at this pipeline speed. [E1, normative-policy — a genuine null on existing adequate buffers]
- **Intervention:** Not a specific proposed mechanism — the paper is primarily diagnostic; its contribution is identifying the structural problem rather than proposing a solution. [E1, normative-policy]
- **Observability:** Resolving uncertainty about what a generated design actually does may require synthesizing and expressing it — the act of generating the missing information is itself the hazardous step. Validation is not merely slow relative to generation; it is potentially unsafe in its own right. [E1, conceptual]
- **System boundary:** The full design-build-test-learn (DBTL) cycle as an integrated whole. [E2, conceptual]

---

## A10. Luhachack, Connell & Berger — From capability uplift to capability governance

- **Unit of observation:** The AI-biology capability stack — layered components spanning data, biological foundation models, agentic AI, build/test automation, and public health response — modeled on a computing stack. [E2, conceptual — the stack metaphor is the authors' framing; "unit of observation" is the analyst's]
- **Relationships:** Explicit in the paper: "no single model, database, or laboratory platform determines risk independently" and governance of interfaces across the stack "may be more strategic than focusing on a single layer." [E1, conceptual]
- **Flows:** Data → models → applications/agents → build/test systems → outputs/observations → governance signals; the if-then dashboard receives observable developments from across the stack and triggers proportionate governance responses. [E2, normative-policy — the full flow chain is the analyst's synthesis of the stack description; the dashboard concept is E1]
- **Capability:** AI-enabled capability uplift (ΔAI) across the DBTL cycle, as framed by the 2025 National Academies report this paper extends. [E1, conceptual/review-derived]
- **Perturbation:** Coupling between layers producing speed, scale, access, or autonomy that no single layer possesses. [E1, conceptual]
- **Buffers:** Genuine null — the paper is prescriptive throughout; it proposes governance strategies per layer but does not characterize what currently limits risk absent those proposals, except to note the build/test stage is "a major bottleneck" that the paper frames as eroding, not stable. [E1, conceptual — appropriately null]
- **Intervention:** Layered governance strategies per stack level (Table 1); an if-then dashboard (Table 2) linking observable developments to evaluation triggers and proportionate responses. [E1, normative-policy]
- **Observability:** The if-then dashboard is explicitly built to make stack-level emergent properties observable over time rather than certifying components once; authors acknowledge this depends on availability and interpretation of observable indicators. [E1, normative-policy]
- **System boundary:** The full DBTL cycle framed as a technical/computing-stack analogy, extended to include a public health and response layer. [E2, conceptual]

*Emergence test applied: clears criteria (1), (2), (4) on the paper's own terms — explicit that no single layer determines risk and that coupling is consequential. Criterion (3) — altering a layer relationship materially changes the capability — is asserted as organizing premise via the if-then table, not demonstrated empirically against a specific case. Code: argues for emergence as organizing principle rather than demonstrated emergent capability.*

---

# CORPUS B

## B1. Wittmann, Alexanian, Bartling, Beal, Clore, Diggans, Flyangolts, Gemler, Mitchell, Murphy, Wheeler & Horvitz — Strengthening nucleic acid biosecurity screening (Science, 2025)

- **Unit of observation:** The nucleic-acid synthesis screening pipeline as a choke point in AI-assisted protein engineering. [E2, empirical]
- **Relationships:** AI protein-design software↔synthesis-screening tools — the paper empirically tests whether the output of one can be engineered to evade the other. [E2, empirical]
- **Flows:** AI design output → nucleic-acid screening system → detection/non-detection decision → synthesis-provider response; patches iteratively developed from screening evaluation results feed back into safeguard design (computational→informational→institutional). [E1/E2 — the screening-pipeline flow is E2; the feedback flow from evaluation to patch development is E1, confirmed via the project's own public summary]
- **Capability:** Generating sequence-divergent variants of proteins of concern that evade detection by current screening tools. Functional retention — whether variants retain hazardous function — is inferred/predicted in the paper's framing rather than independently demonstrated as preserved hazardous function; this distinction must be preserved in any synthesis. [E1/E2 — evasion of screening is E1 empirical; functional retention claim must be coded E2, empirical, with the caveat stated]
- **Perturbation:** The AI-redesign step itself is the controlled perturbation — the thing that defeats the existing screening control. [E1, empirical]
- **Buffers:** Existing nucleic-acid screening tools — shown by this paper's own results to be inadequate against this specific perturbation. [E1, empirical]
- **Intervention:** Patches developed and deployed in collaboration with four commercial DNA synthesis companies, substantially improving detection of synthetic homologs likely to retain wild-type-like function. A completed, deployed intervention, not a proposal. [E1, empirical]
- **Observability:** Direct empirical demonstration that current screening tools cannot reliably detect AI-redesigned sequences — an observability failure at the interface between design and synthesis. [E2, empirical — "observability failure" framing is the analyst's]
- **System boundary:** The interface between AI-assisted protein design tools and nucleic-acid synthesis screening systems. [E2, empirical]

---

## B2. Bloomfield, Pannu, Zhu, Ng, Lewis, Bendavid, Asch, Hernandez-Boussard, Cicero & Inglesby — AI and biosecurity: the need for governance (Science, 2024)

- **Unit of observation:** The general-purpose biological AI model as a dual-use artifact — the same model that designs a benign viral vector could design a more pathogenic one. [E2, conceptual — "dual-use artifact" framing is the analyst's; authors describe the model's properties]
- **Relationships:** Developer↔government — the paper's central relationship is regulatory oversight. [E2, normative-policy]
- **Flows:** Not a central analytical focus of this short policy-forum piece; model capabilities and risk information flow between developers and government, but the paper describes this at a high level without mechanistic specification. [E1, normative-policy — appropriately limited null]
- **Capability:** Dual-use general-purpose biological capability at the model level. [E1, conceptual]
- **Perturbation:** Not modeled mechanistically; this is a governance argument, not a technical or empirical paper. [E1, normative-policy — appropriate null on mechanistic perturbation]
- **Buffers:** Voluntary developer commitments to evaluate biological models — explicitly argued to be insufficient on their own. [E1, normative-policy]
- **Intervention:** Government evaluation of advanced biological AI models with authority to impose safety measures if warranted. [E1, normative-policy]
- **Observability:** Not mechanistically addressed; the paper argues observability should be a government function without specifying how. [E1, normative-policy — appropriate null on mechanism]
- **System boundary:** Model-development and national-governance ecosystem, centered on developer-government relationships. [E2, normative-policy]

---

## B3. Cai, Jeyapragasan, Nedungadi, Yukich & Donoughe — ABLE (Agentic BAIM–LLM Evaluation) (NeurIPS 2025 workshop)

*Author-list correction: Kleinman and Bhasin are ABC-Bench co-authors, not ABLE's. Overlap across both papers: Cai, Nedungadi, and Donoughe.*
*Finding correction from prior entry: the paper's headline result is successful, directed tool orchestration on 7 of 8 subtasks toward an explicitly enhanced-pathogenicity goal — not primarily a refusal finding. Both results likely coexist across models, but competent tool use is the paper's more prominent contribution.*

- **Unit of observation:** The orchestrating LLM agent's ability to wield specialized biological AI models (ProteinMPNN, AlphaFold3) within a dual-use protein-engineering workflow. [E2, empirical]
- **Relationships:** Orchestrating agent↔BAIM tool — whether and how competently the agent can direct these specialized tools toward a stated goal. Human contribution: the paper is a controlled benchmark study; human contribution in the workflow itself is minimal by design (evaluating the agent, not human-AI collaboration). [E2, empirical]
- **Flows:** Goal/instruction → orchestrating LLM → tool calls and parameters → BAIM outputs → agent interpretation and next action. A computational/action flow through a composed agentic system — not simply information entering and leaving, but a chain of directed tool invocations. [E2, empirical]
- **Capability:** Competent multi-step tool orchestration toward a stated dual-use protein-design goal, achieving success on 7 of 8 low-level subtasks including correct ProteinMPNN use. This capability emerges from the combination of orchestrating LLM + specialized BAIMs + task context — not from any single component. [E1, empirical]
- **Perturbation:** The dual-use task framing (redesigning a viral protein toward enhanced pathogenic properties while maintaining structural stability) is the controlled experimental perturbation. [E1, empirical]
- **Buffers:** Not characterized — the paper measures capability, not what currently contains it. [E1, empirical — appropriate null]
- **Intervention:** Not proposed — this is a measurement instrument, not a governance proposal. [E1, empirical — appropriate null]
- **Observability:** Competent tool orchestration toward stated harmful goals is achievable and measurable at the subtask level — finer-grained than a binary refusal/non-refusal measure. [E2, empirical]
- **System boundary:** The agentic workflow (orchestrating LLM + two named BAIM tools) in a controlled benchmark environment. [E2, empirical]

*Emergence test: the capability to orchestrate these tools toward a stated goal appears at the level of the composed system rather than in any single component. Criterion (3) — altering the relationship between the orchestrating LLM and the BAIMs would change the capability — is plausible but not explicitly tested by varying that relationship experimentally. Apply once full results are confirmed: candidate for emergent capability.*

---

## B4. Weidener, Brkić, Jovanović, Ulgac & Meduri — RefusalBench

- **Unit of observation:** Frontier LLM safety-control behavior — specifically, whether model/API access-path systems discriminate across matched biological hazard/risk tiers — measured at the API access-path level rather than the model-weights level. [E2, empirical — "safety-control behavior" is the analyst's framing; authors describe refusal rate and risk-tier discrimination directly]
- **Relationships:** Provider access-path identity↔refusal behavior and risk discrimination — the paper's central empirical relationship, isolated via matched-triple design and logistic regression. [E2, empirical]
- **Flows:** Prompt in → model/API → refusal or response → three-judge council adjudication → risk-tier classification; positive-control calibration anchor tied to BSL tier ratings (informational throughout). [E2, empirical]
- **Capability:** Not biological capability directly — the benchmark measures safety-control behavior. High refusal rate is not itself a biosecurity capability; risk discrimination (Youden's J) is the relevant measured property. [E2, empirical — "safety-control behavior" is the analyst's framing applied to the paper's measurements]
  *Implication for agentic capability (E3):* refusal behavior can determine whether a multi-step agentic workflow proceeds at all, but downstream workflow completion is not tested within this study.
- **Perturbation:** Risk-tier escalation within otherwise identical matched-triple prompts — the controlled within-study perturbation. [E1, empirical]
- **Buffers:** The paper's subject is the (mis)calibration of refusal as a safety buffer, not what it protects; the buffer itself is under examination rather than characterized. [E2, empirical]
- **Intervention:** None proposed for biological risk directly; the paper's normative contribution is methodological — safety evaluations should report tier-discrimination metrics (Youden's J) alongside refusal rate as standard practice. [E1, normative-policy]
- **Observability:** The paper's central finding is a measurement-validity problem: refusal rate is a misleading proxy for risk-tier discrimination — high-refusing models can discriminate risk tiers poorly; well-discriminating models can have lower refusal rates. [E2, empirical — "misleading proxy" and the measurement-validity framing are the analyst's]
- **System boundary:** The model-API access path, explicitly distinguished from model weights — a boundary the paper defends directly based on consistent reason-code patterns. [E1, empirical]

---

## B5. Liu, Nedungadi, Cai, Kleinman, Bhasin & Donoughe — ABC-Bench (ICML 2026)

- **Unit of observation:** Agentic task success across three subtasks corresponding to parts of a possible pathway to hazardous DNA acquisition: liquid-handling robot control, DNA fragment design, and synthesis-screening evasion. [E1, empirical]
- **Relationships:** LLM agent↔physical laboratory instrument (robot) and LLM agent↔synthesis screening software — two empirically tested relationships, each tested under real conditions. Human contribution: a human experimental assistant was present and provided visual/state information and error messages during robot-control debugging; once the compiled script ran, execution proceeded without further modification. This human-mediated step must be preserved in any capability characterization — the workflow was LLM↔human experimental assistant↔robot↔biological material, not LLM→robot directly. [E1, empirical — the human mediator role is explicitly described in the paper]
- **Flows:** Task instruction → LLM-generated code → human relay and debugging → robot execution → biological material transformation (Gibson Assembly) → sequencing result → validation. This flow chain crosses informational, human-mediated, physical-action, material, and measurement stages — instantiating the digital→physical transition as an empirical fact rather than a described or modeled one. [E1/E2 — the flow stages are E1; the "digital-to-physical transition" characterization is E2]
- **Capability:** Actual task success including physical validation — not engagement or refusal, but completion, including confirmed successful DNA assembly by whole-plasmid sequencing. Models already match or exceed expert performance on certain subtasks per the paper's own impact statement. [E1, empirical]
- **Perturbation:** The benchmark tasks themselves, including a subtask specifically testing synthesis-screening evasion as a capability benchmark. [E1, empirical]
- **Buffers:** Synthesis screening is directly tested as a buffer within one subtask — giving this paper an empirical test of a named buffer's performance under realistic conditions. [E1, empirical]
- **Intervention:** Not primarily a governance proposal — a measurement instrument; intervention implications are downstream of the results, not proposed in the paper. [E1, empirical — appropriate null]
- **Observability:** Demonstrates that agentic capability can be validated end-to-end including a physical step, providing a methodology for observing capability that crosses the digital-physical boundary. [E2, empirical]
- **System boundary:** Crosses the digital/physical boundary empirically, with a human intermediary as a constitutive part of the system rather than an external observer. [E1, empirical]

---

*End of Level 1 pass (revised). No patterns named. All cross-paper comparative observations moved to the Candidate Synthesis Observations file. Next step per Section 6: Level 2 synthesis as a separate pass, treating prior Patterns A–E as hypotheses to be checked.*
