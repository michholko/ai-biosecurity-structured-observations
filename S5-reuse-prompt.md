# S5 — Reuse Prompt

Supplementary to: Holko (2026), *Configuration, Proxy Failure, and the Changing Unit of Biosecurity Analysis.* Frontiers in Microbiology.

This prompt can be used with an AI assistant to generate a first-pass structured observation for a new paper. **Always review and correct the AI-generated output against the primary source before using it.** AI assistants may misread, paraphrase imprecisely, or fill in dimensions from general knowledge rather than the paper's actual content. The output is a starting draft, not a citable observation.

---

## Instructions for use

1. Copy the prompt below.
2. Replace `[PAPER TEXT OR ABSTRACT]` with the full text of the paper you are coding, or with its abstract plus key methods and results sections if full text is unavailable.
3. Paste into an AI assistant capable of long-context document analysis.
4. Review every cell of the output against the primary source. Correct evidence relations — many E1 codes will need to be downgraded to E2 where the AI has assigned the paper's framing to a dimension category the authors didn't use.
5. Move any cross-paper observations the AI suggests to your synthesis-candidate scratch file. Do not include them in your Level 1 entry.

---

## The prompt

```
I am applying a structured observation instrument to the following paper as part of a systematic synthesis of AI-biosecurity research. Please generate a structured observation using the schema below.

PAPER:
[PAPER TEXT OR ABSTRACT]

INSTRUMENT:

The instrument asks nine questions about the paper. For each dimension, provide:
- A 1-3 sentence observation drawn directly from the paper's content
- An evidence relation tag: E1 (the paper identifies this in substantially these terms), E2 (the underlying facts are explicit but the dimension framing is yours as analyst), or E3 (inferred beyond what the paper demonstrates)
- An evidence basis tag: empirical / modeled / conceptual / normative-policy / review-derived
- If a dimension is not meaningfully addressed, record that explicitly — absence is informative

The nine dimensions:

1. UNIT OF OBSERVATION: What is actually being studied — an artifact, a facility, a workflow, a relationship, a decision process?

2. RELATIONSHIPS: Which entities interact in ways the paper treats as relevant to its central claim?

3. FLOWS: What information, instructions, materials, or actions pass between components? In what direction, and what is preserved, transformed, added, or lost as they move? Tag flow type if useful: informational / computational / material / physical-action / institutional.

4. CAPABILITY: What becomes possible — what can now be done that matters for security? For any system-level capability claim, identify the required human contribution explicitly.

5. PERTURBATION: What disrupts, defeats, or changes the system the paper describes?

6. BUFFERS: What currently limits or contains risk in the system, as the paper describes it?

7. INTERVENTION: Where does the paper propose or demonstrate acting on the system to change an outcome?

8. OBSERVABILITY: What can actors in the system see or measure — and what remains hidden, difficult to detect, or unsafe to observe?

9. SYSTEM BOUNDARY: What is included in the paper's analysis as "the system," and what is treated as external or out of scope?

EMERGENCE TEST: If the paper makes any claim about a capability, vulnerability, risk, or protective effect that appears to be a property of a composed system rather than a single component, apply the following test and report the result:
- Is the property adequately attributable to a single component? (If yes, it is not emergent.)
- Does it depend on interaction, composition, delegation, or feedback between components?
- Would altering the relationship between components materially change the property?
- Is the property observable or meaningful primarily at the level of the combined system?
State clearly whether the paper demonstrates emergence, argues for emergence as an organizing principle, or makes no emergence claim.

IMPORTANT RULES:
- Base every observation on what the paper actually states, not on general knowledge about the topic.
- Where you are uncertain whether the paper addresses a dimension, say so rather than filling in from general knowledge.
- Do not compare this paper to other papers. All cross-paper observations should be noted separately and not included in this coding.
- Do not name patterns across multiple papers. This is a single-paper coding pass.
- Use E1 sparingly: it means the paper uses substantially this framing itself, not just that the underlying fact is in the paper.
```

---

## After generating the output

- Check every E1 tag: did the paper actually use that framing, or did the AI translate it into the instrument's categories? Downgrade to E2 if it is the latter.
- Check the system boundary: AI assistants often code a narrower boundary than the paper actually draws.
- Check the flows dimension: AI assistants often focus on information flows and miss material and physical-action flows.
- Check the human contribution field under Capability: AI assistants often attribute to an AI system alone capabilities that the paper describes as human-AI composition.
- Move any cross-paper comparisons the AI generated to your synthesis-candidate scratch file.
- Verify any specific factual claims (statistics, findings, author statements) against the primary source before treating them as coded observations.
