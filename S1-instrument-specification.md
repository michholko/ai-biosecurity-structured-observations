# S1 — Structured Observation Instrument: Specification

Supplementary to: Holko and Hu (2026), *Configuration, Proxy Failure, and the Changing Unit of Biosecurity Analysis.* Frontiers in Microbiology.

---

## Governing question

> Where does this paper locate biosecurity-relevant capability, vulnerability, risk, protection, and intervention — and what evidence supports those claims?

This question is intentionally broad. Some papers in scope are principally about locating risk; others are primarily about infrastructure, funding architecture, or governance mechanisms. The governing question is designed to make findings comparable across these without forcing any single framing.

---

## The nine observation dimensions

Every paper is coded on every dimension. Dimensions are non-exclusive: a single mechanism may legitimately appear under more than one (e.g., an information flow that is also a relationship and an intervention point).

**Null-observation rule:** absence is data. If a dimension is not meaningfully addressed by a paper, record that explicitly (e.g., "Intervention: not proposed — this is a diagnostic paper") rather than leaving the cell blank. A consistent pattern of nulls across papers on the same dimension is a reportable finding.

| Dimension | Question it answers |
|---|---|
| **Unit of observation** | What is actually being studied — an artifact, a facility, a workflow, a relationship, a decision process? |
| **Relationships** | Which entities interact in ways the paper treats as relevant to its central claim? |
| **Flows** | What information, instructions, materials, or actions pass between components? In what direction, and what is preserved, transformed, added, or lost as they move? |
| **Capability** | What becomes possible — what can now be done that matters for security? |
| **Perturbation** | What disrupts, defeats, or changes the system the paper describes? |
| **Buffers** | What currently limits or contains risk in the system, as the paper describes it? |
| **Intervention** | Where does the paper propose or demonstrate acting on the system to change an outcome? |
| **Observability** | What can actors in the system see or measure — and what remains hidden, difficult to detect, or unsafe to observe? |
| **System boundary** | What is included in the paper's analysis as "the system," and what is treated as external or out of scope? |

**Flow type tags (optional):** informational / computational / material / physical-action / institutional. Tag the flow type when it clarifies what is moving across an interface, particularly when a flow crosses from digital to physical domains.

**Human contribution rule:** for any system-level capability claim, identify the required human contribution explicitly. This prevents attributing to an AI system alone a capability that depends on human-AI-tool composition — a distinction with direct implications for how such capabilities are evaluated and governed.

---

## Evidence classification

Evidence classification describes **provenance of framing**, not strength of evidence. An E1/normative-policy claim and an E2/empirical claim are different kinds of statements, not stronger or weaker versions of the same thing.

### Evidence relation

- **E1 — Author-explicit.** The paper identifies the phenomenon in substantially the same terms as the coding. The framing is the authors', not a translation.
- **E2 — Analyst-coded.** The underlying facts and mechanisms are explicit in the paper, but the structured-observation dimension label or relational formulation is the analyst's translation. This is the expected code for most dimension entries — the act of representing a paper in structured-observation categories is almost always an analytic operation, even when every underlying fact is explicit.
- **E3 — Synthesized/inferred.** A claim about implication, trend, or generalization extending beyond what any single paper demonstrates. Must stay explicitly hedged in any write-up.

**Coding rule:** when in doubt between two evidence relations, code to the more conservative one. E2 is not a lesser form of evidence; it is an honest record of where the analyst's framing does work the authors' framing does not.

### Evidence basis (record separately from evidence relation)

Empirical / Modeled / Conceptual / Normative-policy / Review-derived

---

## The emergence test

Applied to any capability, vulnerability, risk, or protective effect characterized as system-level rather than component-level. A property qualifies as relationally emergent only if **all four** hold:

1. The property is not adequately attributable to any single component.
2. It depends on interaction, composition, delegation, information exchange, or feedback between components.
3. Altering the relevant relationship would materially change the property.
4. The property is observable or meaningful primarily at the level of the combined system — not within any one part.

**Coding rule:** a paper can satisfy (1), (2), and (4) while only asserting (3) as an organizing premise rather than demonstrating it against a specific case. Label this distinction explicitly: "argues for emergence as organizing principle" rather than "demonstrates emergent property." Both are legitimate contributions; they are not the same claim.

**The test applies to protective effects as well as risks.** A safeguard configuration that produces a protective property no single control achieves alone is a candidate for emergent protective effect, and should be coded as such — not forced into a risk framing.

---

## Process discipline: separating observation from synthesis

**Level 1 — Paper-level structured observation.** Code all papers across all nine dimensions before naming any cross-paper pattern. The following language is prohibited during Level 1: comparative rankings ("widest," "strongest," "only"), cross-paper comparisons ("unlike the other papers," "broader than"), and direct paper-to-paper cross-references that imply a finding. When a cross-paper observation surfaces naturally during coding, move it immediately to a separate synthesis-candidate scratch file rather than leaving it in the Level 1 entry.

**Level 2 — Cross-paper synthesis.** Only after all papers are coded at Level 1: ask what patterns appear across them. Test candidate propositions against a complete evidence matrix (all papers × all candidates), not against a selected subset. Require counterevidence: for each proposition, ask explicitly which papers provide a genuine counterexample in which the property is adequately attributable to a single component or does not depend on configuration.

The write-up should state plainly that cross-paper patterns were derived after observations were completed rather than specified as coding categories in advance. This claim must be true of the actual process, not just the prose.

---

## Known failure modes

**Confirmation pull.** If the analyst holds a prior theoretical commitment, the categories may be shaped to find confirming patterns. Guard against this by requiring counterevidence for every proposition and reporting genuine exceptions rather than interpreting them generously into the main finding.

**Corpus selection circularity.** If the corpus is hand-selected rather than call-selected, there is a risk of choosing papers because they are known in advance to fit the pattern. Fix the selection criteria explicitly before coding begins, and disclose the selection criteria in the write-up.

**Double-counting correlated observations.** Because dimensions are non-exclusive, a single mechanism may appear under multiple dimensions. These co-occurring entries are not independent evidence when building a cross-paper pattern: citing the same underlying mechanism under three dimension headings is one data point, not three.

**Treating a conceptual claim as an empirical one.** See the emergence-test coding rule. A paper arguing for emergence as the correct organizing principle is a different contribution from a paper empirically demonstrating a specific emergent property.

---

## What this instrument does not claim to be

Not a validated taxonomy. Not peer-reviewed as a methodology in its own right. Not demonstrated on a representative sample of any literature — corpora assembled by themed call or analyst selection are non-random by construction. The instrument's claim to usefulness rests on producing comparable, falsifiable observations across papers that share no common vocabulary — not on any specific pattern it surfaces in a given application.
