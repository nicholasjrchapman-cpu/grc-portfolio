# Reference templates

Three fill-in-the-blank starting points for GRC documentation — a policy, a risk assessment, and a control mapping. Skip straight to whichever you need.

!!! tip "Don't need these?"
    These are optional. To remove them: delete `docs/templates.md`, then remove the `Templates` line from the `nav:` section in `mkdocs.yml`.

- [Policy template](#policy-template)
- [Risk assessment template](#risk-assessment-template)
- [Control mapping template](#control-mapping-template)

---

## Policy template

### Purpose
_What risk or requirement does this policy exist to address? One or two sentences._

### Scope
_Who and what systems does this policy apply to? Be specific — "all production AWS accounts," not "the cloud."_

### Policy statement
_The actual rule. Write it the way it would be tested in an audit — clear enough that a control owner can't misread it._

### Roles & responsibilities

| Role | Responsibility |
|------|-----------------|
| Policy Owner | |
| Control Owner | |
| Reviewer | |

### Enforcement
_How is this policy technically or procedurally enforced? Link to the automation or process, not just the intent._

### Exceptions
_Process for requesting and approving exceptions, and who signs off._

### Review cycle
_How often is this reviewed, and by whom. (e.g., "Annually, or upon material change to scope.")_

### Related controls
_Map this to the frameworks it satisfies — SOC 2, ISO 27001, NIST CSF, etc._

---

## Risk assessment template

### Asset description
_What is being assessed — the system, data flow, or process. Include what data it touches and where it lives._

### Threat scenarios

| # | Threat | Likelihood (1-5) | Impact (1-5) | Risk Score | Notes |
|---|--------|-------------------|---------------|------------|-------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

**Scoring key:** Risk Score = Likelihood × Impact. 1-6 = Low, 7-14 = Medium, 15-25 = High.

### Existing controls
_What's already in place that reduces likelihood or impact for each threat above?_

### Residual risk
_After existing controls, what's left? This is the number that should drive the remediation plan._

### Remediation plan

| Action | Owner | Target Date | Status |
|--------|-------|--------------|--------|
| | | | |

### Sign-off
_Who reviewed and accepted this assessment, and when._

---

## Control mapping template

Maps one control across the frameworks you're tracking, so you can show — not just claim — cross-framework fluency.

### Control description
_What is this control actually doing? Written in plain language before you map it to any framework's jargon._

### Framework mapping

| Framework | Control ID | Control Language |
|-----------|------------|-------------------|
| SOC 2 | | |
| ISO 27001 | | |
| NIST CSF | | |
| PCI DSS | | |

### Evidence type
_What counts as proof this control is operating — a screenshot, a config export, a log query result, an approval trail._

### Testing frequency
_How often is this control tested, and is that testing manual or automated?_

### Gaps identified
_Where do the frameworks disagree, or where does your current evidence fall short of what an auditor would expect?_
