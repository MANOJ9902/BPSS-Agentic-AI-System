# BPSS Agent — Sample Question Answers

Pre-computed answers with full source citations from the dataset.

---

## Q1. Which candidate files are not yet ready for BPSS closure, and why?

**CAND-102 — Sofia Khan (ANALYST) — NOT READY**
Sources: `CAND-102_candidate_pack.docx`, `bpps_tracker_export.csv`, `document_inventory.csv`, `Analyst_Working_Notes.docx`, `Adjudication_Register.pdf`

- Tracker status is "Ready to Join" — the SOP explicitly states this is not equivalent to BPSS closure (`Screening_Operations_SOP.pdf`: "Ready to Join indicates business onboarding readiness and is not equivalent to BPSS closure").
- Criminality: basic disclosure PENDING as of 2026-02-05 (`CAND-102_candidate_pack.docx`).
- Employment history: unexplained gap 2024-04-01 to 2024-05-20 (49 days, exceeds 31-day threshold) — `employment_history.csv` row, evidence_status = "Unexplained".
- Address proof: utility bill dated 2025-10-01 is **126 days** before analyst review on 2026-02-04 — exceeds 90-day limit (`document_inventory.csv` ADDR-102-UB; `Analyst_Working_Notes.docx`).
- Exception: provisional start approved in Adjudication Register (2026-02-06) — this explicitly does not constitute BPSS closure.

**CAND-104 — Liam O'Connor (OPS) — NOT READY (incorrectly marked Clear)**
Sources: `CAND-104_candidate_pack.docx`, `BPSS_case_tracker.xlsx` tracker sheet, `document_inventory.csv`, `Analyst_Working_Notes.docx`, `Email_Approvals_and_Escalations.docx`

- Tracker shows status = Clear — this is incorrect (see Q4 for full analysis).
- Identity: address proof (ADDR-104-CT) has present_in_folder = **No** (`document_inventory.csv`). Analyst noted seeing a council tax letter on a video call but no copy was retained. An unretained document cannot satisfy the mandatory control.
- Employment history: period 2023-01 to 2024-07 evidenced by CV only — evidence_status = "Weak, No documentary corroboration" (`employment_history.csv`). Hiring manager email (Email_Approvals_and_Escalations.docx excerpt 2) is not an approved exception and explicitly excluded by policy.
- No entry for CAND-104 exists in the Adjudication Register.

**CAND-105 — Emma Roy (ANALYST) — NOT READY**
Sources: `CAND-105_candidate_pack.docx`, `bpps_tracker_export.csv`, `document_inventory.csv`, `employment_history.csv`

- All four mandatory controls are incomplete (tracker correctly shows Pending):
  - Identity: no address proof found in folder.
  - RTW: BRP expired 2024-12-31 (`document_inventory.csv` RTW-105-BRP valid_to = 2024-12-31); no replacement share code; expired BRP not acceptable per `Permitted_RTW_Evidence_Matrix.pdf`.
  - Employment: only 2024-06 onward covered — 18 months prior unaccounted for (`employment_history.csv`).
  - Criminality: no result file found.

**CAND-106 — Rohan Sen (CONTRACTOR-LTD) — OPEN (Risk Accepted, RTW gap unresolved)**
Sources: `CAND-106_candidate_pack.docx`, `Adjudication_Register.pdf`, `Permitted_RTW_Evidence_Matrix.pdf`

- Operational start approved in Adjudication Register (2026-02-01) — but the RTW requirement has not been formally waived, only deferred while the contractor legal position is clarified.
- RTW matrix: "Contractors personally performing services in the UK still require confirmation of lawful work eligibility unless legal counsel has documented a jurisdictional exemption." No such exemption is on file.

**READY FOR CLOSURE:**
- **CAND-101 (Aarav Mehta)**: all mandatory controls complete and evidenced — Clear justified.
- **CAND-103 (Nina Patel, INTERN)**: criminality not mandatory; expired passport acceptable with current student ID; all other controls complete — Clear justified.

---

## Q2. Control completion by candidate — full matrix

| Candidate | Identity | RTW | Employment | Criminality | Status |
|-----------|----------|-----|------------|-------------|--------|
| CAND-101 | ✅ | ✅ | ✅ | ✅ | **Clear** |
| CAND-102 | ⚠️ stale | ✅ | ❌ gap | ❌ pending | **Pending** |
| CAND-103 | ✅ | ✅ | ✅ | N/A (INTERN) | **Clear** |
| CAND-104 | ❌ unretained | ✅ | ❌ weak | ✅ | **Should be Pending** |
| CAND-105 | ❌ | ❌ expired | ❌ | ❌ | **Pending** |
| CAND-106 | ✅ | ❌ | ✅ | N/A (CONTRACTOR-LTD) | **Risk Accepted (open)** |

### CAND-101 — Aarav Mehta (ANALYST)
- Identity ✅: Passport ID-101-P valid to 2030 + bank statement ADDR-101-BS dated 2026-01-28 (14 days before review 2026-02-11 — FRESH). `document_inventory.csv` rows 0–1.
- RTW ✅: UK passport accepted. `CAND-101_candidate_pack.docx`.
- Employment ✅: Referee letters covering 2023-01 to 2026-01, no gap >31 days. `employment_history.csv` rows 0–1.
- Criminality ✅: Basic disclosure clear 2026-02-10. `document_inventory.csv` row 2 (CRIM-101).

### CAND-102 — Sofia Khan (ANALYST)
- Identity ⚠️: Driving licence valid (ID-102-DL) but utility bill ADDR-102-UB dated 2025-10-01 — **126 days** before review 2026-02-04, exceeds 90-day limit. `document_inventory.csv` row 4; `Analyst_Working_Notes.docx`.
- RTW ✅: eVisa share code RTW-102-SC valid 2026-02-03. `document_inventory.csv` row 5.
- Employment ❌: Gap 2024-04-01 to 2024-05-20 (49 days), evidence_status = "Unexplained". `employment_history.csv` row 3.
- Criminality ❌: Basic disclosure pending as of 2026-02-05. `CAND-102_candidate_pack.docx`.

### CAND-103 — Nina Patel (INTERN)
- Identity ✅: Passport ID-103-P expired 2025-11-01 is acceptable for identity corroboration only when supported by a second current photo ID. Student ID ID-103-SID valid to 2026-09-01 provides that. Address proof ADDR-103 dated 2026-02-20 (5 days before review — FRESH). `document_inventory.csv` rows 6–8; `BPSS_Screening_Policy_v3.pdf`.
- RTW ✅: Current share code confirms unrestricted right to work. `CAND-103_candidate_pack.docx`.
- Employment ✅: Education declaration accepted for full-time student. `employment_history.csv` row 5.
- Criminality N/A: INTERN role exempt per `BPSS_Screening_Policy_v3.pdf`.

### CAND-104 — Liam O'Connor (OPS)
- Identity ❌: Passport ID-104-P valid to 2029. Address proof ADDR-104-CT: present_in_folder = **No** — mentioned in analyst note but not retained. `document_inventory.csv` row 10; `Analyst_Working_Notes.docx`.
- RTW ✅: Irish passport accepted. `CAND-104_candidate_pack.docx`.
- Employment ❌: Period 2023-01 to 2024-07 — evidence_type = "CV only", evidence_status = "Weak, No documentary corroboration". Prior employer did not respond. Manager verbal confirmation excluded by policy. `employment_history.csv` row 6; `Email_Approvals_and_Escalations.docx` excerpt 2; `BPSS_Screening_Policy_v3.pdf`.
- Criminality ✅: Basic disclosure clear 2026-02-18. `document_inventory.csv` row 11 (CRIM-104).

### CAND-105 — Emma Roy (ANALYST)
- Identity ❌: Passport copy ID-105-P present (valid to 2032). No address proof found in document inventory — no row for CAND-105 of type Address. `document_inventory.csv`; `CAND-105_candidate_pack.docx`.
- RTW ❌: BRP RTW-105-BRP expired 2024-12-31. No replacement share code. "Expired BRP alone: not acceptable." `document_inventory.csv` row 13; `Permitted_RTW_Evidence_Matrix.pdf`.
- Employment ❌: Only 2024-06-01 onward evidenced (referee, valid). Prior ~18 months (2023-01 to 2024-05) not covered. `employment_history.csv` row 8.
- Criminality ❌: No result file found. `CAND-105_candidate_pack.docx`.

### CAND-106 — Rohan Sen (CONTRACTOR-LTD)
- Identity ✅: Passport ID-106-P valid to 2031 + bank statement ADDR-106-BS dated 2026-01-15 (16 days before review 2026-01-31 — FRESH). `document_inventory.csv` rows 14–15.
- RTW ❌: Recruiter note only — no individual eligibility evidence. RTW matrix requires individual confirmation for contractors performing UK services unless legal counsel documents a jurisdictional exemption. No exemption on file. `Permitted_RTW_Evidence_Matrix.pdf`; `CAND-106_candidate_pack.docx`; `Email_Approvals_and_Escalations.docx` excerpt 3.
- Employment ✅: Contract pack covers 2023-01 to 2026-01-15. `employment_history.csv` row 9.
- Criminality N/A: CONTRACTOR-LTD exempt per `BPSS_Screening_Policy_v3.pdf`.

---

## Q3. Policy exceptions — approved vs unapproved

### Formally approved (Adjudication Register only)

| Case | Decision | Approvers | Date | Scope |
|------|----------|-----------|------|-------|
| CAND-102 | Provisional start approved | Hiring Director + Screening Ops Lead | 2026-02-06 | Start work before DBS returned only |
| CAND-106 | Risk Accepted | Screening Ops Lead | 2026-02-01 | Operational start while contractor legal position clarified |

Authority: "Only entries in this register constitute formally approved exceptions. Email or manager approval outside this register should not be treated as authorized risk acceptance." — `Adjudication_Register.pdf`.

### Unapproved deviations

**CAND-104:** Hiring manager email (`Email_Approvals_and_Escalations.docx` excerpt 2 — "I spoke with Liam's previous team lead and am comfortable with his background. Please clear him") was treated by the analyst as authorisation to mark status = Clear. This email:
- Comes from a single approver (hiring manager only — not both Hiring Director and Screening Ops Lead as required by the emergency provision).
- Does not appear in the Adjudication Register.
- Is explicitly excluded by policy: "Analyst notes, email statements, or verbal manager confirmation alone do not satisfy mandatory controls."

This is an unapproved deviation. The Clear status on CAND-104 is unjustified.

**CAND-106 RTW assumption:** The recruiter email (`Email_Approvals_and_Escalations.docx` excerpt 3) claiming RTW is not needed for contractors is an assumption, not an approved exception. The Adjudication Register entry for CAND-106 approves an operational start — it does not waive the RTW requirement. The RTW gap remains open.

---

## Q4. CAND-104 — is closure justified?

**Conclusion: No. Closure is not justified. The Clear status is incorrect.**

**Policy requirement for identity** (`BPSS_Screening_Policy_v3.pdf`):
At least one government-issued photo ID **plus** proof of address dated within the last 3 months at time of review.

**Actual evidence:**
- Passport ID-104-P: present, valid to 2029. ✅
- Address proof ADDR-104-CT: present_in_folder = **No** (`document_inventory.csv` row 10). The analyst noted seeing a council tax letter during a live video call but no copy was retained (`Analyst_Working_Notes.docx`). An unretained document cannot be audited, verified, or cited. **Identity control is INCOMPLETE.**

**Policy requirement for employment history** (`BPSS_Screening_Policy_v3.pdf`):
Sufficient documentary or referee evidence to cover the previous 3 years. Unexplained gaps over 31 days must be accounted for.

**Actual evidence:**
- 2023-01 to 2024-07: CV only, evidence_status = "Weak, No documentary corroboration" (`employment_history.csv` row 6). Prior employer did not respond to verification request.
- 2024-08 to 2026-01: Referee, Valid (`employment_history.csv` row 7).
- Hiring manager email treated as employment confirmation — policy explicitly excludes this: "Analyst notes, email statements, or verbal manager confirmation alone do not satisfy mandatory controls." **Employment history control is INCOMPLETE.**

**Contradiction between tracker and evidence:**
- Tracker (`BPSS_case_tracker.xlsx` tracker sheet / `bpps_tracker_export.csv`): identity_complete = Yes, employment_complete = Yes, status_tracker = Clear.
- Underlying evidence: address proof not retained; employment gap covered only by CV + verbal manager confirmation.

**No approved exception exists.** CAND-104 has no entry in the Adjudication Register. The analyst's stated reason ("Marked clear to avoid delay") is not a recognised exception.

---

## Q5. Stale or expired documents

| Candidate | Document | Date | Review date | Age | Issue |
|-----------|----------|------|-------------|-----|-------|
| CAND-102 | Utility Bill ADDR-102-UB | 2025-10-01 | 2026-02-04 | **126 days** | ❌ Exceeds 90-day limit |
| CAND-103 | Passport ID-103-P | expired 2025-11-01 | 2026-02-25 | Expired | ⚠️ Acceptable only because current student ID ID-103-SID also present |
| CAND-105 | BRP RTW-105-BRP | valid_to 2024-12-31 | 2026-03-03 | Expired 15 months before review | ❌ Expired RTW evidence — no replacement on file |

Sources: `document_inventory.csv`; `BPSS_Screening_Policy_v3.pdf` ("Proof of address must be dated within 90 days of the analyst review date"; "Passports may be expired for identity corroboration only if supported by a second current photo ID"); `Permitted_RTW_Evidence_Matrix.pdf` ("Expired BRP alone: not acceptable").

All other address-proof documents are within the 90-day window: CAND-101 bank statement (14 days), CAND-106 bank statement (16 days). CAND-104's address proof is not retained — staleness cannot be assessed. CAND-103 address proof ADDR-103 dated 2026-02-20 is 5 days before review — FRESH.

---

## Q6. Escalation summary for Screening Operations Lead

**To:** Screening Operations Lead
**Subject:** BPSS Escalation — Top 3 Highest-Risk Open Cases
**Date:** 2026-03-03

---

### Priority 1 — CAND-105 Emma Roy (Analyst) | Risk: HIGH | Status: Pending

All four mandatory controls are incomplete as of the analyst review date 2026-03-03:

1. **Identity:** Passport copy present (valid to 2032) but no address proof found in the case folder.
2. **Right to work:** BRP RTW-105-BRP expired 2024-12-31 — over 14 months before review. Expired BRP does not satisfy the RTW evidence matrix. Candidate states an updated visa was emailed separately; this cannot be verified from the case folder (`Analyst_Working_Notes.docx`).
3. **Employment history:** Only the period 2024-06-01 onward is evidenced (referee, valid). The 18 months from approximately January 2023 to May 2024 are unaccounted for.
4. **Criminality:** No basic disclosure result on file.

**Action required:** Case must remain Pending. Do not approve a start date until at minimum items 2 and 4 are resolved. Obtain: (a) current address proof dated on or after 2025-12-03, (b) valid eVisa share code or equivalent, (c) documentary employment evidence for Jan 2023 – May 2024, (d) basic disclosure result.

---

### Priority 2 — CAND-104 Liam O'Connor (Ops Specialist) | Risk: MEDIUM-HIGH | Status: Incorrectly marked Clear

This case presents a compliance integrity risk: it has been closed as Clear in the tracker without satisfying two mandatory controls, with no approved exception in the Adjudication Register.

1. **Address proof not retained:** Analyst noted seeing a council tax letter on a video call but no copy was scanned into the case folder (`document_inventory.csv` ADDR-104-CT: present_in_folder = No; `Analyst_Working_Notes.docx`). Policy requires a retained document.
2. **Employment history incomplete:** The period January 2023 to July 2024 (18 months) is evidenced only by CV. The prior employer did not respond to the referee request. A hiring manager email was used to justify closure — this does not satisfy the mandatory control and does not appear in the Adjudication Register.

**Action required:** Reopen to Pending. Obtain: (a) a retained copy of address proof dated within 90 days of the original review date 2026-02-20 (i.e. dated on or after 2025-11-22), (b) documentary or referee evidence for Jan 2023 – Jul 2024. If business requires urgent resolution, escalate to Hiring Director and Screening Ops Lead jointly for a formal Adjudication Register entry.

---

### Priority 3 — CAND-106 Rohan Sen (Contractor-LTD) | Risk: MEDIUM | Status: Risk Accepted (open)

Operational start was approved in the Adjudication Register on 2026-02-01 while the contractor's legal position is clarified. However, the RTW evidence gap remains open.

The RTW evidence matrix (`Permitted_RTW_Evidence_Matrix.pdf`) states that contractors personally performing services in the UK still require confirmation of lawful work eligibility unless legal counsel has documented a jurisdictional exemption. No such exemption is on file. The recruiter's email assumption (`Email_Approvals_and_Escalations.docx` excerpt 3) does not constitute an exemption.

**Action required:** Obtain either (a) individual RTW evidence from Rohan Sen or (b) written legal counsel opinion documenting a jurisdictional exemption. Until one of these is received, the case cannot be closed.

---

## Q7. What is missing to clear CAND-105?

Sources: `CAND-105_candidate_pack.docx`, `document_inventory.csv`, `employment_history.csv`, `BPSS_Screening_Policy_v3.pdf`, `Permitted_RTW_Evidence_Matrix.pdf`

Four items are required before CAND-105 (Emma Roy, Analyst role) can be cleared. None can be satisfied by verbal claims or unretained emails.

**1. Address proof**
Required: a document confirming current address dated within 90 days of the analyst review date (review: 2026-03-03, so dated on or after 2025-12-03).
Currently: no address proof of any kind found in the case folder.

**2. Valid right-to-work evidence**
Required: a valid RTW document matching the permitted evidence matrix — typically an eVisa share code or equivalent current evidence.
Currently: BRP RTW-105-BRP expired 2024-12-31. Candidate stated an updated visa was emailed separately but no file is stored (`Analyst_Working_Notes.docx`). Unverifiable from current evidence. Expired BRP does not satisfy the RTW matrix.

**3. Employment history — January 2023 to May 2024 (approx. 18 months)**
Required: documentary or referee evidence covering the full prior 3 years, with any gap >31 days explained.
Currently: employment_history.csv shows coverage only from 2024-06-01. The 18 months prior are entirely unaccounted for.

**4. Criminality / basic disclosure result**
Required: basic disclosure returned (Analyst role is not INTERN or CONTRACTOR-LTD — criminality is mandatory per policy).
Currently: no result file found in the case folder.

---

## Q8. Contradictions between tracker and analyst notes

| # | Where | Tracker says | Reality | Source authority |
|---|-------|-------------|---------|-----------------|
| 1 | CAND-104 `status_tracker` | Clear | Should be Pending — two mandatory controls not satisfied | `document_inventory.csv`, `employment_history.csv`, `Analyst_Working_Notes.docx` |
| 2 | CAND-104 `identity_complete` | Yes | No — address proof ADDR-104-CT not retained in folder | `document_inventory.csv` row 10 (present_in_folder = No) |
| 3 | CAND-104 `employment_complete` | Yes | No — 2023-01 to 2024-07 evidenced by CV only; verbal manager confirmation excluded by policy | `employment_history.csv` row 6; `BPSS_Screening_Policy_v3.pdf` |
| 4 | CAND-102 `ready_to_join` | Yes | Ready to Join ≠ BPSS closure; case remains Pending | `Screening_Operations_SOP.pdf` |
| 5 | CAND-106 candidate pack | "RTW not applicable — contractor" | RTW matrix requires individual eligibility evidence for contractors performing UK services | `Permitted_RTW_Evidence_Matrix.pdf` vs `CAND-106_candidate_pack.docx` |

**Authority hierarchy** (`Screening_Operations_SOP.pdf`): "The tracker status field is operational and may lag detailed review notes by up to one working day. Where the tracker and adjudication register conflict, the adjudication register is the authority for exception approval." For evidence questions, the retained documents and analyst notes take precedence over tracker fields.

---

## Q9. Candidates marked "Ready to Join" with incomplete mandatory controls

| Candidate | Ready to Join | Incomplete mandatory controls |
|-----------|:------------:|-------------------------------|
| CAND-102 | Yes | Criminality (pending), employment gap (unexplained 49 days), address proof (stale 126 days) |
| CAND-104 | Yes | Identity (address proof not retained), employment history (CV only for 18 months) |

Sources: `bpps_tracker_export.csv` rows 1 and 3; `document_inventory.csv`; `employment_history.csv`; `Analyst_Working_Notes.docx`.

**CAND-102:** The provisional start is backed by an Adjudication Register entry (2026-02-06, approved by Hiring Director and Screening Ops Lead). This is a legitimate approved exception for starting work before the DBS is returned — but the case remains Pending and cannot be closed.

**CAND-104:** There is no entry in the Adjudication Register. The Ready to Join flag and the Clear status both represent unapproved deviations from policy. The hiring manager's email (`Email_Approvals_and_Escalations.docx` excerpt 2) is not an approved exception.

---

## Q10. Structured JSON summary per candidate

```json
[
  {
    "candidate_id": "CAND-101",
    "candidate_name": "Aarav Mehta",
    "role": "ANALYST",
    "status": "Clear",
    "control_completion": {
      "identity": "Complete",
      "right_to_work": "Complete",
      "employment_history": "Complete",
      "criminality": "Complete"
    },
    "missing_items": [],
    "risk_level": "Low",
    "supporting_evidence": [
      "ID-101-P: Passport valid to 2030 [document_inventory.csv row 0]",
      "ADDR-101-BS: Bank statement 2026-01-28, 14 days before review — FRESH [document_inventory.csv row 1]",
      "RTW: UK passport [CAND-101_candidate_pack.docx]",
      "Employment: Referee letters 2023-01 to 2026-01, no gap >31 days [employment_history.csv rows 0-1]",
      "CRIM-101: Basic disclosure clear 2026-02-10 [document_inventory.csv row 2]"
    ],
    "contradictions": []
  },
  {
    "candidate_id": "CAND-102",
    "candidate_name": "Sofia Khan",
    "role": "ANALYST",
    "status": "Pending (tracker shows 'Ready to Join' — not equivalent to BPSS closure per SOP)",
    "control_completion": {
      "identity": "Incomplete — address proof ADDR-102-UB stale by 126 days (2025-10-01, review 2026-02-04)",
      "right_to_work": "Complete",
      "employment_history": "Incomplete — unexplained gap 2024-04-01 to 2024-05-20 (49 days)",
      "criminality": "Incomplete — basic disclosure pending as of 2026-02-05"
    },
    "missing_items": [
      "Fresh address proof dated on or after 2025-11-05 (within 90 days of review 2026-02-04)",
      "Evidence or explanation for employment gap Apr-May 2024",
      "Basic disclosure result"
    ],
    "risk_level": "High",
    "approved_exception": "Provisional start approved (Adjudication_Register.pdf, 2026-02-06, Hiring Director + Screening Ops Lead) — start before DBS only, does not constitute BPSS closure",
    "supporting_evidence": [
      "ADDR-102-UB: Utility bill 2025-10-01, 126 days before review — STALE [document_inventory.csv row 4; Analyst_Working_Notes.docx]",
      "RTW-102-SC: eVisa share code valid 2026-02-03 [document_inventory.csv row 5]",
      "Employment gap: evidence_status=Unexplained [employment_history.csv row 3]",
      "Criminality: pending as of 2026-02-05 [CAND-102_candidate_pack.docx]"
    ],
    "contradictions": [
      "Tracker ready_to_join=Yes does not mean BPSS closure [Screening_Operations_SOP.pdf]"
    ]
  },
  {
    "candidate_id": "CAND-103",
    "candidate_name": "Nina Patel",
    "role": "INTERN",
    "status": "Clear",
    "control_completion": {
      "identity": "Complete — expired passport acceptable for corroboration with current student ID",
      "right_to_work": "Complete",
      "employment_history": "Complete — education declaration accepted for full-time student",
      "criminality": "N/A — INTERN role exempt per BPSS_Screening_Policy_v3.pdf"
    },
    "missing_items": [],
    "risk_level": "Low",
    "supporting_evidence": [
      "ID-103-P: Passport expired 2025-11-01 — identity corroboration only [document_inventory.csv row 6]",
      "ID-103-SID: Student ID valid 2025-09-01 to 2026-09-01 — current photo ID [document_inventory.csv row 7]",
      "ADDR-103: Address proof 2026-02-20, 5 days before review — FRESH [document_inventory.csv row 8]",
      "RTW: Share code confirms unrestricted right to work [CAND-103_candidate_pack.docx]",
      "Employment: Education declaration accepted [employment_history.csv row 5]",
      "Policy: criminality not mandatory for INTERN [BPSS_Screening_Policy_v3.pdf]"
    ],
    "contradictions": []
  },
  {
    "candidate_id": "CAND-104",
    "candidate_name": "Liam O'Connor",
    "role": "OPS",
    "status": "INCORRECTLY MARKED Clear — should be Pending; no approved exception exists",
    "control_completion": {
      "identity": "Incomplete — address proof ADDR-104-CT mentioned in analyst note but NOT retained in folder",
      "right_to_work": "Complete",
      "employment_history": "Incomplete — 2023-01 to 2024-07 (18 months) evidenced by CV only; verbal manager confirmation excluded by policy",
      "criminality": "Complete"
    },
    "missing_items": [
      "Retained copy of address proof (council tax letter seen on video call was not scanned)",
      "Documentary or referee evidence for employment period 2023-01 to 2024-07"
    ],
    "risk_level": "Medium-High",
    "approved_exception": "None — no entry in Adjudication_Register.pdf",
    "supporting_evidence": [
      "ID-104-P: Passport valid to 2029 [document_inventory.csv row 9]",
      "ADDR-104-CT: present_in_folder=No [document_inventory.csv row 10]",
      "Employment 2023-01 to 2024-07: evidence_type=CV only, evidence_status=Weak [employment_history.csv row 6]",
      "Manager email: not an approved exception [Email_Approvals_and_Escalations.docx excerpt 2; Adjudication_Register.pdf — no CAND-104 entry]",
      "CRIM-104: Basic disclosure clear 2026-02-18 [document_inventory.csv row 11]"
    ],
    "contradictions": [
      "Tracker identity_complete=Yes conflicts with document_inventory.csv present_in_folder=No for ADDR-104-CT",
      "Tracker employment_complete=Yes conflicts with employment_history.csv evidence_status=Weak for 2023-01 to 2024-07",
      "Tracker status_tracker=Clear is unjustified — no approved exception in Adjudication Register"
    ]
  },
  {
    "candidate_id": "CAND-105",
    "candidate_name": "Emma Roy",
    "role": "ANALYST",
    "status": "Pending",
    "control_completion": {
      "identity": "Incomplete — no address proof found in case folder",
      "right_to_work": "Incomplete — BRP expired 2024-12-31, no replacement share code in file",
      "employment_history": "Incomplete — only 2024-06 onward covered; 18 months prior unaccounted for",
      "criminality": "Incomplete — no disclosure result on file"
    },
    "missing_items": [
      "Address proof dated on or after 2025-12-03 (within 90 days of review 2026-03-03)",
      "Valid RTW evidence — current eVisa share code or equivalent",
      "Employment evidence for approx. Jan 2023 to May 2024",
      "Basic disclosure result"
    ],
    "risk_level": "High",
    "approved_exception": "None",
    "supporting_evidence": [
      "ID-105-P: Passport copy present, valid to 2032 [document_inventory.csv row 12]",
      "RTW-105-BRP: expired 2024-12-31 [document_inventory.csv row 13; Permitted_RTW_Evidence_Matrix.pdf]",
      "Employment: only 2024-06-01 onward evidenced [employment_history.csv row 8]",
      "Criminality: no file found [CAND-105_candidate_pack.docx]",
      "Candidate claims updated visa and police certificate emailed separately — unverifiable from case folder [Analyst_Working_Notes.docx]"
    ],
    "contradictions": []
  },
  {
    "candidate_id": "CAND-106",
    "candidate_name": "Rohan Sen",
    "role": "CONTRACTOR-LTD",
    "status": "Risk Accepted — operational start allowed; RTW gap still open pending legal clarification",
    "control_completion": {
      "identity": "Complete",
      "right_to_work": "Incomplete — no individual RTW evidence; recruiter assumption does not satisfy RTW matrix",
      "employment_history": "Complete",
      "criminality": "N/A — CONTRACTOR-LTD exempt per BPSS_Screening_Policy_v3.pdf"
    },
    "missing_items": [
      "Individual RTW evidence OR written legal counsel opinion documenting jurisdictional exemption"
    ],
    "risk_level": "Medium",
    "approved_exception": "Risk Accepted (Adjudication_Register.pdf, 2026-02-01, Screening Ops Lead) — operational start allowed while contractor legal position is clarified; RTW requirement not formally waived",
    "supporting_evidence": [
      "ID-106-P: Passport valid to 2031 [document_inventory.csv row 14]",
      "ADDR-106-BS: Bank statement 2026-01-15, 16 days before review — FRESH [document_inventory.csv row 15]",
      "RTW: Recruiter note only — RTW matrix requires individual eligibility evidence [Permitted_RTW_Evidence_Matrix.pdf; CAND-106_candidate_pack.docx]",
      "Employment: contract pack valid [employment_history.csv row 9]",
      "Policy: criminality not mandatory for CONTRACTOR-LTD [BPSS_Screening_Policy_v3.pdf]"
    ],
    "contradictions": [
      "Recruiter email assumes RTW not required for contractors [Email_Approvals_and_Escalations.docx excerpt 3]",
      "RTW matrix explicitly requires individual eligibility evidence for contractors performing UK services [Permitted_RTW_Evidence_Matrix.pdf]"
    ]
  }
]
```