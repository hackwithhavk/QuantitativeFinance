# Lab Notebook Hygiene and Project Handbook

## 1. Purpose

This handbook defines how the team documents, reviews, and preserves work for **Algorithmic Markets: AI and Quantitative Decision Systems**, a Principal Financial–funded student project planned for September 2026 through April 2027.

The goal is not to create paperwork for its own sake. A notebook entry should make it possible for another approved team member to understand:

1. What question was being investigated.
2. Why the question matters to the project.
3. What data, code, hardware, and assumptions were used.
4. What happened, including failures and unexpected results.
5. Whether the result is reliable enough for a workshop, demonstration, or follow-up.
6. What should happen next.

If a result cannot be explained from the notebook entry and its linked artifacts, it is not considered reproducible project work.

## 2. Project summary

The project will create an interactive educational platform where students explore how mathematical modeling, statistical analysis, machine learning, and computational systems are used to study financial data and support quantitative reasoning.

Planned activities include:

- Training student leaders on the Jetson edge-AI development kits and the project workflow.
- Building introductory examples with financial or simulated datasets.
- Teaching financial concepts such as time value of money, present value, discounted cash flow, NPV, IRR, amortization, risk-return tradeoffs, and scenario analysis.
- Demonstrating data cleaning, exploratory analysis, feature construction, predictive modeling, and time-series analysis.
- Comparing model outputs with simple baselines and clearly communicating uncertainty.
- Hosting recurring workshops, demonstrations, interdisciplinary events, and outreach programming.
- Maintaining reusable educational materials and documented examples for future semesters.

The expected direct reach is approximately 20–30 students during the academic year. The equipment and materials are intended to support recurring programming beyond a single event.

## 3. Funding and equipment baseline

The project proposal identifies a total requested amount of **$773.94**:

| Item | Quantity | Unit estimate | Subtotal | Intended use |
| --- | ---: | ---: | ---: | --- |
| NVIDIA Jetson Orin Nano Super Developer Kit | 2 | $249.00 | $498.00 | Edge-AI development, machine-learning demonstrations, time-series workflows, and embedded decision-system examples |
| Texas Instruments BA II Plus financial calculator | 6 | $45.99 | $275.94 | Time value of money, discounted cash flow, NPV, IRR, amortization, and quantitative decision-making exercises |
| **Total** |  |  | **$773.94** |  |

This table is the project’s planning baseline from the application. It is not by itself permission to spend, change quantities, or substitute products. Sanchin and Cail should document equipment decisions, quotes, purchases, custody, setup, and condition in the relevant notebook entries. Material funding changes should be documented by the project leads and included in the next funder check-in.

## 4. Scope

### 4.1 In scope

Work belongs in this repository when it supports at least one of the following project outcomes:

- A reproducible educational example involving financial data or a clearly labeled simulation.
- A workshop lesson, exercise, demonstration, or assessment.
- A documented experiment involving machine learning, time-series analysis, quantitative finance, or financial decision systems.
- A valuation, risk, or scenario-analysis example that explains assumptions and limitations.
- A Jetson setup, deployment, benchmarking, or edge-AI demonstration relevant to the educational program.
- A reusable data-preparation, visualization, modeling, or evaluation component.
- A project-management decision that affects scope, safety, funding alignment, equipment, workshops, or deliverables.
- An application, onboarding, mentoring, or review record needed to coordinate approved contributors.

### 4.2 Out of scope

The project does **not** authorize or support:

- Live trading, brokerage activity, or use of real money.
- Investment advice, individualized financial recommendations, or promises of returns.
- Presenting a classroom model as a production trading system or as a reliable market-prediction engine.
- Collecting, storing, or analyzing personally identifiable financial information, brokerage credentials, account numbers, or private client data.
- Publishing secrets, API keys, access tokens, passwords, or private data.
- Making claims that a model is accurate without documenting its test design, limitations, and uncertainty.
- Deploying software to production systems or external services without explicit approval from Sanchin and Cail.
- Expanding the project into unrelated software, hardware, or financial products without a recorded scope decision.

Any proposed work that appears to cross the boundary must be paused and raised with Sanchin and Cail before implementation.

## 5. Leadership and responsibilities

| Role | Person(s) | Responsibilities |
| --- | --- | --- |
| Funder check-in contact | Summer Malik | Performs periodic check-ins summarizing group progress for the funder. Summer is not responsible for day-to-day execution, project decisions, or contributor management. |
| Project leads and day-to-day owners | Sanchin and Cail | Lead the whole project: set and manage working scope, plan technical work, approve contributors, assign tasks, support contributors, review notebook entries, coordinate workshops, maintain shared standards, manage deliverables, and escalate organization-level issues when needed. |
| Contributor | Approved student applicant | Complete assigned work, create timely notebook entries, preserve evidence, disclose limitations and failures, follow data/security rules, and request review when work is ready. |
| Notebook reviewer | Sanchin, Cail, or an assigned approved reviewer | Check completeness, reproducibility, scope alignment, evidence, and educational clarity. A reviewer should not silently rewrite an experiment’s conclusions. |
| Workshop owner | Assigned lead or contributor | Prepare learning objectives, materials, setup instructions, safety notes, timing, exercises, and post-workshop observations. |

When responsibilities overlap, Sanchin and Cail decide the project’s working direction. The person who performs the work remains responsible for the first complete record. Review transfers quality control, not authorship. Summer’s check-ins are funder-facing progress summaries and do not replace the detailed entries created by the people doing the work.

### 5.1 Decision rights

- Sanchin and Cail own decisions about day-to-day execution, working scope, contributor assignments, technical methods, notebook review, workshops, and project deliverables.
- Sanchin and Cail own project-facing and sponsor-facing decisions within the approved scope. They provide the reviewed facts and milestones used in Summer’s periodic funder check-ins.
- Any proposed live financial integration, use of restricted data, material spending change, or public claim must be paused and reviewed by Sanchin and Cail before proceeding.
- Contributors may prototype freely within an approved task, but they must document the prototype and must not represent an unreviewed result as an official project result.
- If a decision is unclear, record the question in the notebook and escalate it before proceeding.

## 6. Repository structure

Use one directory per contributor for personal work and shared folders for materials that serve the whole team.

```text
.
├── readme.md
└── Lab Notebooks/
    ├── README.md                         # This handbook; source of truth
    ├── TEMPLATE.md                       # Copy for each notebook entry
    ├── APPLICATION_TEMPLATE.md           # Copy for applicant intake
    ├── Summer/                            # Summer’s entries
    ├── Sanchin/                           # Sanchin’s entries
    ├── Cail/                               # Cail’s entries
    ├── Raymundo/                           # Raymundo’s entries, if participating
    └── example/                            # Safe examples and reference material
```

Recommended additions as the project grows:

```text
Lab Notebooks/
├── shared/
│   ├── workshops/                         # Lesson plans and delivery notes
│   ├── datasets/                          # Metadata only; do not commit restricted data
│   ├── protocols/                          # Hardware and experiment procedures
│   └── decisions/                          # Scope and project decisions
└── archive/                               # Completed historical material; read-only by convention
```

### 6.1 Naming conventions

Notebook entries should use:

```text
YYYY-MM-DD_<owner>_<short-slug>.md
```

Examples:

```text
2026-09-08_sanchin_jetson-setup.md
2026-09-18_cail_baseline-time-series.md
2026-10-02_summer_workshop-scope-review.md
```

Use lowercase kebab-case for the slug. Keep the original date and entry file unchanged after creation. If an entry needs correction, add a dated correction note or a new linked entry; do not erase the historical record.

Artifacts should use the same experiment slug where possible:

```text
<date>_<slug>_raw-notes.md
<date>_<slug>_results.csv
<date>_<slug>_figure-01.png
```

## 7. Required notebook hygiene

### 7.1 One entry per meaningful work unit

Create an entry for any work that produces a decision, experiment, result, failure, setup change, workshop artifact, or reusable code. A meaningful work unit may be a single focused session or a short sequence of directly related sessions.

Do not combine unrelated experiments into one vague entry. If the question, data, method, or conclusion changes materially, create a separate entry and link the entries together.

### 7.2 Write entries contemporaneously

Record work on the same day whenever possible. If notes are reconstructed later, say so explicitly and distinguish remembered context from recorded evidence.

Every entry must include:

- Author and date/time in Eastern Time.
- Status: `planned`, `in progress`, `complete`, `blocked`, `needs review`, or `archived`.
- A specific question or objective.
- Scope and success criteria.
- Links to relevant issue, task, workshop, or parent entry.
- Environment and materials used.
- Data provenance and transformation details.
- Code commit, notebook version, or exact procedure.
- Observations, outputs, and interpretation.
- Limitations, risks, and unresolved questions.
- Next action and responsible person.

### 7.3 Separate observation from interpretation

Use direct language:

- **Observation:** “The validation MAE was 0.42 on the held-out period.”
- **Interpretation:** “This is lower than the moving-average baseline, but the improvement may not generalize because the test period is short.”

Do not state an interpretation as though it were a measurement. Do not remove an inconvenient result because it makes the project look less successful. Failed approaches are useful evidence when they are documented clearly.

### 7.4 Preserve history

- Never rewrite a prior conclusion without recording what changed and why.
- Do not replace raw observations with cleaned-up summaries that hide the original result.
- Mark superseded entries as `superseded` and link to the replacement.
- Record corrections with the correction date, author, reason, and affected section.
- Treat committed notebook entries as the project record.

## 8. Standard entry workflow

Use this workflow for every experiment, setup task, or workshop artifact.

### Step 1: Define the work

Before starting, state the question, motivation, scope boundary, owner, expected output, and success criteria. If the work is exploratory, say what decision the exploration is intended to inform.

### Step 2: Record the starting state

Capture the relevant repository commit, hardware, software versions, dataset source, retrieval date, configuration, and assumptions. A reader should be able to reconstruct what was true before the work began.

### Step 3: Run the procedure

Record commands, settings, parameters, random seeds, deviations from the plan, and notable observations. If the full procedure is in code or another document, link it and summarize the exact invocation.

### Step 4: Preserve evidence

Link or attach the smallest useful set of outputs: tables, figures, logs, metrics, screenshots, or workshop observations. Give each output a meaningful name and explain what it demonstrates.

### Step 5: Interpret cautiously

Compare the result to a baseline or stated expectation. Identify uncertainty, possible leakage, confounding factors, data limitations, hardware limitations, and alternative explanations.

### Step 6: Review and close

Request review from Sanchin, Cail, or the assigned reviewer. Address comments in the entry or in a linked follow-up. Mark the entry `complete` only when required fields are filled and the reviewer agrees that the result is understandable and appropriately scoped.

## 9. Reproducibility standard

The minimum reproducibility record depends on the work type.

### 9.1 Analysis or modeling

Record:

- Dataset name, source, license or permitted use, retrieval date, and version/hash when available.
- Inclusion/exclusion criteria and all material cleaning steps.
- Target variable, features, forecast horizon, and train/validation/test split.
- Baseline method and why it is appropriate.
- Model name, version, hyperparameters, random seed, and stopping criteria.
- Evaluation metrics with definitions and units.
- Hardware, operating system, runtime, and relevant dependency versions.
- Results for each meaningful run, not only the preferred run.
- Known limitations, especially look-ahead bias, survivorship bias, leakage, non-stationarity, and small samples.

For time-series work, preserve chronological ordering. Do not randomly shuffle observations across time unless the method specifically requires it and the decision is explained.

### 9.2 Jetson or hardware work

Record:

- Kit identifier or a non-sensitive local label such as `jetson-01` or `jetson-02`.
- Date, operator, physical setup, power and peripheral configuration.
- JetPack, CUDA, Python, framework, and operating-system versions.
- Installation steps and any deviations or errors.
- Input size, batch size, precision, runtime settings, and other benchmark parameters.
- Temperature, power mode, latency, throughput, memory use, or other relevant measurements.
- Whether the result was run once or repeated, and how variability was handled.
- Safe shutdown, storage, and hardware-condition notes.

Do not include serial numbers, credentials, private network details, or photos containing personal information unless explicitly approved and necessary.

### 9.3 Workshop or event work

Record:

- Learning objectives written in terms of what participants should be able to explain or do.
- Intended audience and assumed prerequisites.
- Materials, setup, timing, facilitator, and equipment allocation.
- Dataset or simulation used and why it is appropriate for teaching.
- Activities, prompts, expected outputs, and answer keys where applicable.
- Accessibility and safety considerations.
- Attendance using approved aggregate counts only.
- What worked, what confused participants, and what should change.
- Follow-up owner and deadline.

## 10. Data, privacy, and security

This is an educational repository. Use public, synthetic, or explicitly approved data whenever possible.

### 10.1 Prohibited content

Never commit:

- Passwords, API keys, access tokens, private keys, or credentials.
- Brokerage logins, account numbers, transaction histories, or personal financial records.
- Student contact details, phone numbers, student IDs, or other unnecessary personally identifiable information.
- Confidential sponsor or partner information.
- Data whose license or permission does not allow the intended use.

If a secret or private record is accidentally exposed, stop using it, notify Sanchin and Cail immediately, remove it from active use, and document the incident without copying the secret into the notebook. Removing a line from the latest file is not sufficient if the secret entered version history.

### 10.2 Data provenance

For every dataset, record:

```text
Dataset name:
Source or URL:
Provider/owner:
License or permission:
Retrieval date:
Version, release, or hash:
Time period covered:
Geographic or population coverage:
Known limitations:
Transformations performed:
Output location:
```

If raw data cannot be stored in the repository, commit the metadata and a reproducible acquisition or preparation procedure where permitted. State exactly what a new contributor must obtain separately.

### 10.3 Financial and educational disclaimer

All financial examples, forecasts, backtests, valuations, and model outputs are for education and research demonstration only. They are not investment advice, a solicitation, a guarantee of performance, or evidence that a strategy will work with live money. Workshop materials must display this limitation wherever a reasonable participant could mistake a demonstration for a recommendation.

## 11. Modeling and evaluation expectations

Every model-based result must answer the following questions:

1. What is the baseline?
2. What exactly is being predicted or estimated?
3. What information would have been available at the time of the prediction?
4. How were data split and leakage prevented?
5. Which metric is being used, and why?
6. How sensitive is the result to assumptions, parameters, and the evaluation window?
7. What would make the result fail in a different market or dataset?
8. Is the result suitable only as a classroom demonstration, or is there a stronger reason to trust it?

Avoid language such as “the model predicts the market” or “the strategy works” unless the statement is narrowly defined, supported by evidence, and qualified with the relevant limitations. Prefer language such as “the model produced lower error than the stated baseline on this held-out sample.”

For valuation work, record the cash-flow assumptions, discount rate, terminal-value assumptions, timing convention, units, and sensitivity analysis. For risk work, define the risk measure, horizon, confidence level if relevant, and scenario construction.

## 12. Review gates

Use these gates to keep work moving while protecting quality.

| Gate | When it applies | Required evidence | Approver |
| --- | --- | --- | --- |
| Scope check | New project idea, new dataset, new external service, or material change | Objective, scope, expected cost/risk, and out-of-scope check | Sanchin and Cail |
| Technical check | New experiment, model, hardware procedure, or reusable code | Complete notebook entry, reproducible procedure, baseline, and limitations | Sanchin or Cail |
| Workshop check | Lesson, demo, or public-facing activity | Learning objectives, setup, safety/privacy notes, disclaimer, and facilitator plan | Assigned lead, with Sanchin/Cail approval |
| Release check | Official result, public material, sponsor-facing material, or final report | Reviewed entry, source links, accurate claims, and artifact inventory | Sanchin and Cail |

Review comments should be actionable. A reviewer may request a missing parameter, clearer claim, additional baseline, or better limitation statement. The author remains responsible for addressing the comment and recording material decisions.

## 13. Applications and onboarding

The project may accept students who want to contribute to research-style documentation, quantitative finance, AI, data analysis, hardware, workshop design, or project coordination. Prior finance experience is not required when the applicant can explain how they will learn and contribute responsibly.

### 13.1 Applicant process

1. Applicant submits a completed copy of [APPLICATION_TEMPLATE.md](APPLICATION_TEMPLATE.md).
2. Sanchin or Cail reviews the applicant’s interests, availability, relevant experience, and proposed contribution.
3. Sanchin or Cail conducts an orientation or short working session when needed.
4. Sanchin and Cail confirm acceptance, role, lead, and any access or equipment restrictions.
5. The contributor completes a small scoped onboarding task and creates the first notebook entry.
6. The lead reviews the entry and confirms that the contributor understands the hygiene standard.

Acceptance should be based on fit, reliability, learning goals, and willingness to document work—not on inflated claims of expertise.

### 13.2 Onboarding checklist

Before independent work, each contributor must:

- Read this handbook and the repository readme.
- Identify their lead and reviewer.
- Confirm the task’s scope and success criteria.
- Learn where to store code, notes, outputs, and workshop materials.
- Confirm that no secrets, private financial data, or unnecessary personal information will be used.
- Complete a small test entry using [TEMPLATE.md](TEMPLATE.md).
- Demonstrate how to link a notebook entry to a commit or artifact.
- Understand the educational-only financial disclaimer.

## 14. Communication and status

Each active work item should have one visible status:

- `planned`: approved or proposed, not started.
- `in progress`: active work is underway.
- `blocked`: progress requires a decision, resource, access, or clarification.
- `needs review`: author believes the entry is ready for review.
- `complete`: reviewed and accepted for its stated purpose.
- `superseded`: replaced by a newer entry; retain for history.
- `archived`: retained for reference and no longer active.

When blocked, record the blocker, the person who can resolve it, the date raised, and the next follow-up date. Do not hide blocked work by leaving the status unchanged.

Weekly or otherwise regular project updates should summarize:

- Completed entries and deliverables.
- Work currently in progress.
- Blockers and decisions needed.
- Equipment, budget, privacy, or safety concerns.
- Upcoming workshops or deadlines.
- Changes to scope or ownership.

## 15. Definition of done

An experiment, setup task, or workshop artifact is complete only when:

- The work is inside the approved scope.
- The notebook entry is complete and dated.
- Inputs, versions, assumptions, and procedure are recorded.
- Outputs are linked and named clearly.
- Results are compared with an appropriate expectation or baseline.
- Limitations and unresolved questions are stated.
- No prohibited data or secrets are present.
- Required review is complete.
- The next action is either assigned or explicitly marked not needed.

An official project deliverable is complete when Sanchin and Cail have reviewed and approved its content, scope, claims, and readiness for its intended educational use. Reviewed milestones and evidence can then be summarized in a periodic funder check-in.

## 16. Quick pre-commit checklist

Before committing any notebook or project artifact, ask:

- Can someone else identify the question and reproduce the procedure?
- Did I record the date, author, status, and repository commit?
- Did I identify the data source, license, retrieval date, and transformations?
- Did I state assumptions and distinguish observations from interpretation?
- Did I include a baseline or explain why one is not applicable?
- Did I document failures, uncertainty, and limitations?
- Did I check for secrets, private data, and unnecessary personal information?
- Is the financial disclaimer present wherever the output could be misunderstood?
- Did I assign a reviewer and next action?

If any answer is “no,” the entry is not ready for review.

## 17. Change log

Record material changes to this handbook below. Do not silently change a rule that could affect prior work.

| Date | Author | Change | Reason/decision |
| --- | --- | --- | --- |
| 2026-08-19 | Summer Malik | Initial team handbook created | Establish shared scope, project-lead responsibilities, application process, and notebook hygiene before accepting contributors |
