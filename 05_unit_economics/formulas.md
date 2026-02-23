# Unit Economics Model – Arvi (3 Plans)

---

# 1. Trial Cost Modeling

The trial cost was approached in two stages:

1) A theoretical probabilistic model  
2) A simplified operational model (final implementation)

Understanding the distinction between both is essential.

---

## 1.1 Theoretical Probabilistic Model (Conceptual)

Initial modeling attempted to simulate mixed behavioral distribution during trial:

E_lambda = f_casual · e_casual
         + f_moderate · e_moderate
         + f_intensive · e_intensive

Where:

- f_* = fraction of users per behavioral segment
- e_* = relative energy consumption level per segment

Total trial energy:

E_trial = 270 · E_lambda

Trial cost:

Trial_cost = E_trial · (cost_per_energy_unit / 100)

This model assumed probabilistic distribution of behavioral profiles during the trial.

It provided statistical elegance but introduced:
- Behavioral uncertainty
- Sensitivity to assumed fractions
- Risk of cost underestimation

---

## 1.2 Applied Operational Model (Final Decision)

The probabilistic model was replaced with a deterministic conservative approach:

Trial_cost_per_user = Daily_API_cost_base · 2

Where:

- Trial duration = 2 days
- Assumed usage pattern = Base user profile

Total trial cost:

Total_trial_cost = Trial_cost_per_user · total_users

### Strategic Rationale

- Trial users typically explore actively.
- Underestimating trial cost creates structural financial risk.
- Deterministic modeling simplifies scaling projections.
- It introduces built-in margin protection.
- It removes dependency on uncertain behavioral distribution.

This change was deliberate and risk-aware.

---

# 2. Net Price

Net_price = Gross_price · 0.79 · 0.97

Where:

- 0.79 = VAT removal (21%)
- 0.97 = Stripe fee (3%)

---

# 3. Daily API Cost per User

Daily_API_cost = Σ (function_calls_i · cost_per_call_i)

---

# 4. Monthly API Cost per User

Monthly_API_cost = Daily_API_cost · 30

---

# 5. Net Profit per User

Net_profit_per_user = Net_price − Monthly_API_cost − Trial_cost_per_user

---

# 6. Net Profit per Plan

Net_profit_plan =
    (Net_price · plan_users)
    − (Monthly_API_cost · plan_users)

---

# 7. Total Net Profit

Total_net_profit =
    Net_profit_mini
  + Net_profit_base
  + Net_profit_pro
  − Total_trial_cost

---

# 8. Conversion Distribution

Converted_users = total_users · conversion_rate

Plan_users_i = Converted_users · plan_distribution_i

Where:

- conversion_rate = 18%
- plan_distribution:
    - Mini = 65%
    - Base = 25%
    - Pro = 10%

---

# Structural Principle

The economic model prioritizes:

- Margin protection
- Controlled trial exposure
- Predictable scaling
- Sustainable low-cost subscription economics