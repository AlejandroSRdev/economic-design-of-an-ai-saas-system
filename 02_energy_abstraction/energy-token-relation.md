# 02 — Energy Abstraction Layer

## Why Introduce an Internal Currency?

AI systems operate in tokens.  
Users do not.

Directly exposing token consumption creates:

- Cognitive friction
- Poor mental models
- Perceived randomness
- Lack of transparency

Tokens are a technical unit.  
They are not a product unit.

To bridge this gap, an internal abstraction layer was introduced:

> 1 Energy Unit = 100 Tokens

This abstraction transformed raw token consumption into a user-facing resource model.

---

## Product-Level Rationale

The goal was not only cost control, but clarity.

Instead of:
- “You have 14,327 tokens remaining”

Users see:
- “You have 72 energy units remaining”

This mirrors familiar mental models:
- Battery percentage
- Data limits
- Resource meters in games
- API quotas

The abstraction improves:

- Perceived control
- Predictability
- Transparency
- Plan differentiation

---

## Economic Implications

Energy serves as a decoupling mechanism between:

- Provider token cost
- Internal cost accounting
- Commercial plan design

This enables:

1. Independent pricing decisions  
2. Controlled usage ceilings per plan  
3. Flexible model substitution  
4. Margin protection independent of provider volatility  

By separating internal economic logic from raw token mechanics, the system avoids direct coupling between user perception and provider billing complexity.

---

## Design Principle

The energy abstraction was not created to gamify usage.

It was created to:

- Simplify complexity for users
- Preserve economic control internally
- Enable structured pricing tiers
- Protect against uncontrolled scaling

This layer became the foundation for plan design, trial modeling and unit economics simulation.