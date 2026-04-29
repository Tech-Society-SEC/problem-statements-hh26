# Explanation

## The Problem

Machine learning models — gradient boosted trees, neural networks, ensemble stacks — have become the backbone of digital lending in India and globally. They can process hundreds of features and outperform traditional scorecards on predictive accuracy. But this power comes with a serious structural flaw: the model's internal reasoning is invisible.

When a borrower is rejected, the lender's system knows the decision was statistically sound but neither the applicant, nor the compliance officer, nor the regulator can trace exactly why. A credit score drops by 40 points and no one can explain which factor drove it.

## Why Explainability Matters in AI

In traditional software, a rule is explicit: "reject if income < ₹3L." In ML, the "rule" is a mathematical function learned from millions of data points — it cannot be read, quoted, or justified in plain language without an additional explainability layer. Explainable AI (XAI) is the discipline of building that layer: tools and techniques that translate model outputs into human-interpretable reasons. Without XAI, a lender deploying ML is essentially operating a decision-making process they themselves cannot fully audit.

The consequences of opaque AI in lending are severe: discriminatory outcomes go undetected, regulators cannot verify compliance, borrowers cannot exercise their right to contest, and lenders carry silent legal and reputational exposure.

## Your Challenge

You will build an AI-powered credit decisioning system with a full explainability and audit layer — one that can operate transparently under real-world regulatory scrutiny.

Your system must address three distinct audiences simultaneously:

- **The rejected applicant** receives a plain-language explanation of the primary factors that led to their rejection, with guidance on which factors are actionable (e.g., reduce debt-to-income ratio vs. credit history length which is time-bound).
- **The compliance officer / internal auditor** sees a per-decision audit trail: feature attribution scores (e.g., SHAP values), model confidence, which features exceeded decision thresholds, and a flag if any decision appears anomalous against the model's historical distribution.
- **The regulator** accesses an aggregate view: demographic fairness metrics across gender, age group, geography, and income band; model drift indicators over time; and exportable compliance reports conforming to RBI/GDPR/CFPB documentation standards.

## Core Technical Requirements

- The credit model must use a real ML algorithm (XGBoost, LightGBM, Random Forest, or a neural network). Logistic regression alone does not qualify.
- Explainability must be post-hoc and model-agnostic — using SHAP, LIME, or equivalent — not hand-coded rules retrofitted to look like ML explanations.
- Fairness testing is mandatory. You must measure and report disparate impact across at least two protected attributes using recognized metrics (e.g., demographic parity, equalized odds, or the 4/5ths rule from US EEOC guidelines).
- All explanations must be grounded in actual model feature weights. Explanations that are generated independently of the model (e.g., by a separate LLM making up reasons) are disqualified.
- The audit log must be tamper-evident — decisions, timestamps, feature inputs, and SHAP outputs must be stored in a structure that detects post-hoc modification.

## Suggested Starting Points

**Datasets:**

- UCI Credit Default
- Home Credit Default Risk (Kaggle)

**XAI Libraries:**

- SHAP (TreeExplainer / KernelExplainer)
- LIME
- InterpretML
- Captum (PyTorch)

**Fairness Toolkits:**

- Fairlearn
- AI Fairness 360 (IBM)
- What-If Tool (Google)

**Tamper-evident Logging:**

- Append-only logs with SHA-256 hash chaining
- Simple Merkle structure

---

### Note: This serves only as a reference example. Innovative ideas and unique implementation techniques are highly encouraged and warmly welcomed! 