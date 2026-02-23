# Token Estimation Method and Prompt Weighting Strategy

## The Problem Observed

During early usage simulations, an inconsistency appeared.

Certain features generated:

- Short, simple outputs (from the user's perspective)
- But required large prompt contexts internally

This produced an asymmetry:

- The user perceived low complexity
- The system incurred relatively high token consumption

If energy were calculated using full token count (prompt + output at 100%),  
some actions would feel disproportionately expensive.

This would create:

- Perceived unfairness
- Confusion about cost logic
- Reduced trust in the system

---

## Design Decision

To address this, energy deduction was not computed as:


energy = ceil((tokens_prompt + tokens_response) / 100)


Instead, prompt tokens were weighted at 30%:


tokens_effective = tokens_response + (tokens_prompt * 0.30)
energy = ceil(tokens_effective / 100)


---

## Rationale Behind the 30% Prompt Weight

The decision was grounded in product coherence rather than technical purity.

Key considerations:

1. **User-Perceived Value**  
   Users primarily associate value with output quality, not internal context size.

2. **Fairness Perception**  
   A short answer should not feel as expensive as a long analytical response, even if it required large contextual prompts.

3. **Internal Context Stability**  
   Some features required stable contextual memory or structured instructions, increasing prompt tokens without increasing visible output complexity.

4. **Controlled Margin Protection**  
   Prompt tokens still impact cost, so they were not ignored — but discounted to reflect their lower perceived user value.

---

## Why 30% Specifically?

The weighting was chosen as a calibrated compromise:

- 0% would ignore real cost exposure.
- 100% would over-penalize context-heavy features.
- 30% preserved cost sensitivity while aligning energy deduction with perceived output complexity.

This created a more coherent relationship between:

- Visible response length
- Energy consumption
- User understanding
- Internal cost reality

---

## Strategic Implication

This weighting mechanism illustrates a core principle of the system:

> Economic abstraction must align technical cost with perceived product value.

The goal was not to mirror provider billing exactly.

The goal was to build a sustainable and psychologically coherent economic layer.