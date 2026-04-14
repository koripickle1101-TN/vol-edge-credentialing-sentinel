CREDENTIALING SENTINEL | ENROLLMENT & VERIFICATION LOGIC

OBJECTIVE: Maintain 100% provider data integrity to eliminate "Non-Participating Provider" denials.

1. PRIMARY SOURCE VERIFICATION (PSV) WORKFLOW
The system executes automated triggers for the following:
- NPDB (National Practitioner Data Bank): Query on initial and every 2 years.
- OIG/SAM Exclusion: Monthly automated scan for debarment.
- STATE LICENSE: Real-time verification against Tennessee Department of Health.

2. ENROLLMENT AGING LOGIC
Tracks Payer Enrollment timelines to predict "Go-Live" dates for new providers:
- Medicare (855I/R): 60-90 Days
- Medicaid (TennCare): 30-60 Days
- Commercial Payers: 90-120 Days

3. COMPLIANCE STANDARDS
Logic is aligned with NCQA (National Committee for Quality Assurance) standards for Credentialing and Re-credentialing cycles.

LOGIC TRIGGER EXAMPLE:
IF License_Expiry < 60 Days THEN Trigger: "RE-CREDENTIALING_SPRINT"
IF CAQH_Attestation == Outdated THEN Trigger: "SYSTEM_HOLD_CLAIMS"
