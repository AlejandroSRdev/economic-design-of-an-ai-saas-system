# Scaling Simulation – Net Profit Across Different User Scales

---

# 1. Trial Cost Calculation

The trial lasts **2 days** and assumes the **Base user usage pattern**.

## 1.1 Base User Daily Usage Pattern

- generateHomePhrase: 1
- generateConversationalResponse: 7
- generateVerificationQuestion: 3
- evaluateVerificationResponse: 3
- weeklyHabitAnalysis: 0.14
- generateStepComment: 0.1667
- generateReprogrammingResult: 0.0333
- generateExecutionSummary: 0.7
- createThematicSeries: 0.14
- generateHabitTestResponse: 0.84
- createAction: 0.5
- generateConversationReport: 0.14

---

## 1.2 Trial Daily API Cost

Daily_API_cost_trial =
Σ (daily_usage_frequency × cost_per_call)

Daily_API_cost_trial ≈ 0.024367230 USD

Converted to EUR:
0.024367230 × 0.92 = 0.022415 €

---

## 1.3 Trial Cost Per User

Trial_cost_per_user =
Daily_API_cost_trial × trial_days

Trial_cost_per_user =
0.024367230 × 2
= 0.048734460 USD

Converted to EUR:
0.048734460 × 0.92 = 0.0448337 €

---

## 1.4 Total Trial Cost

Total_trial_cost =
Trial_cost_per_user × total_users

---

# 2. Net Profit Simulation at Different Scales

Assumptions:

- Conversion rate = 18%
- Plan distribution:
  - Mini = 65%
  - Base = 25%
  - Pro = 10%

Net profit per user:

- Mini: 0.8068 €
- Base: 3.4926 €
- Pro: 6.8451 €

(All values already include trial cost allocation.)

---

## 2.1 Scale: 500 Users

Converted users:
500 × 18% = 90

Plan distribution:
- Mini ≈ 59 users
- Base ≈ 23 users
- Pro = 9 users

Total trial cost:
0.0448337 × 500 = 22.42 €

Net profit:

Mini: 59 × 0.8068 = 47.60 €
Base: 23 × 3.4926 = 80.33 €
Pro: 9 × 6.8451 = 61.61 €

Total Net Profit:
47.60 + 80.33 + 61.61 − 22.42
= 167.12 €

---

## 2.2 Scale: 1,000 Users

Converted users:
1,000 × 18% = 180

Plan distribution:
- Mini = 117
- Base = 45
- Pro = 18

Total trial cost:
0.0448337 × 1,000 = 44.83 €

Total Net Profit:
= 329.95 €

---

## 2.3 Scale: 10,000 Users

Converted users:
10,000 × 18% = 1,800

Plan distribution:
- Mini = 1,170
- Base = 450
- Pro = 180

Total trial cost:
0.0448337 × 10,000 = 448.337 €

Total Net Profit:
= 3,298.45 €

---

## 2.4 Scale: 100,000 Users

Converted users:
100,000 × 18% = 18,000

Plan distribution:
- Mini = 11,700
- Base = 4,500
- Pro = 1,800

Total trial cost:
0.0448337 × 100,000 = 4,483.37 €

Total Net Profit:
= 32,984.42 €

---

## 2.5 Scale: 1,000,000 Users

Converted users:
1,000,000 × 18% = 180,000

Plan distribution:
- Mini = 117,000
- Base = 45,000
- Pro = 18,000

Total trial cost:
0.0448337 × 1,000,000 = 44,833.70 €

Total Net Profit:
= 329,844.09 €

---

# 3. Final Results Summary

- 10,000 users → 3,298.45 €
- 100,000 users → 32,984.42 €
- 1,000,000 users → 329,844.09 €

---

# Strategic Observation

The model demonstrates:

- Positive unit economics from small scale
- Linear scalability under stable conversion
- Controlled trial exposure
- Margin sustainability under low-cost pricing

The simulation validates that the economic structure remains viable across growth stages.