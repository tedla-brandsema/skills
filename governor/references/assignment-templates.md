# Governor assignment templates

Use these prompts to hand off a defined assignment to Governor or to an independent reviewer. Select the template for the next requested boundary.

| Template | Use when | Stop at |
| --- | --- | --- |
| [1. Planning](#1-planning) | The outcome is agreed and the approach needs to be planned | Reviewed plan for owner ratification |
| [2. Planning Revision](#2-planning-revision) | Review or owner feedback requires a change to the plan | Complete revised candidate for owner ratification |
| [3. Implementation](#3-implementation) | The owner has ratified the plan and authorized a task, slice, or phase | Verified delivery through the authorized boundary |
| [4. Implementation Rework](#4-implementation-rework) | A delivered implementation candidate needs correction | Corrected candidate with applicable checks and rereview |
| [5. Commit](#5-commit) | The owner has accepted the exact candidate and authorized a commit | Verified local commit |
| [6. Investigation](#6-investigation) | Evidence is needed before deciding whether or how to proceed | Findings and options for the owner |
| [7. Independent Candidate Review](#7-independent-candidate-review) | The owner requests a fresh, read-only assessment of a plan or implementation | Evidence-backed verdict |
| [8. Integration and Publication](#8-integration-and-publication) | The owner wants to integrate an accepted commit, publish a ref, or both | Verification of the authorized Git operations |

Templates 1–5 cover the usual handoffs. Use 6–8 when the work calls for a distinct assignment. Governor can review, correct, and commit within an authorized implementation run. The owner ratifies the plan or accepts the exact candidate when required. Carry the recorded decision into the next assignment.

When drafting, fill in the actual repository, candidate identity, evidence, settled decisions, exclusions, and stop point. Use `None` for absent permissions and mark missing facts or owner decisions as pending. Record only authority the owner has granted. If a required grant or decision is missing, label the draft pending and state what it needs. A review verdict can support a handoff but carries no grant of authority. Route material findings on a plan to Planning Revision and those on an implementation candidate to Implementation Rework. Use Commit or Integration and Publication only for the exact candidate and operations the owner has approved.

## 1. Planning

~~~markdown
# Governor — Planning Assignment

Use your installed Governor skill. Prepare a planning candidate for owner ratification.

## Assignment

- Repository — [PATH]
- Requested outcome — [OUTCOME]
- Context — [PHASE, ROADMAP ITEM, SETTLED DECISIONS, RELEVANT REFERENCES]
- Expected baseline — [BRANCH AND HEAD, IF KNOWN]
- Exclusions — [OUT-OF-SCOPE WORK]

Read applicable `AGENTS.md`, architecture, roadmap, TODO, existing plans, code, and tests. Inspect Git state and relevant history. Establish what is implemented, the last accepted boundary, and the next roadmap item. Reconcile conflicting or stale records with current evidence.

Identify reusable capabilities, acceptance criteria, architectural constraints, and protected guarantees. Investigate material uncertainties with authorized, bounded, non-destructive probes. Propose the smallest coherent slice sequence, with dependencies, acceptance conditions, verification, independent review, documentation, risks, and unresolved decisions. Reconcile it with existing ratified plans. Obtain proportionate independent review and address in-scope findings. Preserve material disagreements for the owner.

## Authority and handback

- Planning and bounded investigation — [AUTHORIZED SCOPE]
- Branch creation or switching — [EXACT PERMISSION OR NONE]
- Commit of planning materials — [EXACT PERMISSION OR NONE]
- Production implementation, destructive operations, push, integration, and tags — None

Return the source-backed baseline, plan and slice sequence, acceptance and qualification approach, review findings and dispositions, exact document paths and Git state, and decisions for owner ratification. Stop at the reviewed planning candidate.
~~~

## 2. Planning Revision

~~~markdown
# Governor — Planning Revision Assignment

Use your installed Governor skill. Revise the complete planning candidate for owner ratification.

## Assignment

- Repository — [PATH]
- Existing plan — [PATH AND VERSION OR COMMIT]
- Original baseline — [BRANCH AND HEAD]
- Owner feedback and review findings — [SPECIFIC FINDINGS AND REFERENCES]
- Settled decisions and exclusions — [DECISIONS AND EXCLUSIONS]

Read the complete plan and supporting evidence. Establish its ratification status. Preserve ratified historical records and follow repository conventions for a successor or amendment when needed. Test the feedback against the actual architecture and implementation. Classify findings by impact and scope, revise the affected decisions, and preserve justified decisions and evidence. Reconcile scope, dependencies, acceptance criteria, exclusions, and relevant living documents. Obtain independent review of the complete revised candidate. Resolve material in-scope findings and surface unresolved decisions.

## Authority and handback

- Planning revision and bounded investigation — [AUTHORIZED SCOPE]
- Branch creation or switching — [EXACT PERMISSION OR NONE]
- Commit of planning materials — [EXACT PERMISSION OR NONE]
- Production implementation, push, integration, and tags — None

Return a coherent replacement candidate, the rationale for material changes, dispositions of prior findings, the new review verdict, exact paths and Git state, and any outstanding owner decisions. Stop for owner ratification.
~~~

## 3. Implementation

~~~markdown
# Governor — Implementation Assignment

Use your installed Governor skill. Deliver the authorized scope autonomously through the stated boundary.

## Assignment

- Repository — [PATH]
- Requested outcome and acceptance criteria — [OBSERVABLE OUTCOME AND CRITERIA]
- Ratified plan and owner decision — [PATH, VERSION OR COMMIT, DECISION REFERENCE]
- Authorized task, slices, or phase — [EXACT SCOPE AND TERMINAL BOUNDARY]
- Expected working branch and starting HEAD — [BASELINE]
- Settled architectural decisions and exclusions — [DECISIONS AND EXCLUSIONS]

Re-establish repository truth. Apply Governor's slice delivery loop. Make the smallest coherent change, update affected tests and documentation, verify the affected guarantees, obtain proportionate independent review, classify and resolve in-scope findings, and reverify invalidated evidence. The primary Governor owns integration and acceptance of delegated work. Delivery workers have no Git delivery authority. Reconcile living roadmap and implementation records. At an authorized phase boundary, complete integrated qualification and fresh whole-phase review.

Continue through routine corrections. Stop at the authorized boundary or when progress needs a material owner decision, missing authority, resolution of a conflict with the ratified plan, or a blocker that cannot be resolved within scope.

## Authority and handback

- Source changes — [EXACT IMPLEMENTATION SCOPE AUTHORIZED BY THE OWNER]
- Branch creation or switching — [EXACT PERMISSION OR NONE]
- Commit — [PER REVIEWED SLICE, FINAL CANDIDATE, OR NONE]
- Push — [EXACT REMOTE REF AND CADENCE OR NONE]
- Integration — [EXACT TARGET AND PERMISSION OR NONE]
- Required final owner acceptance — [SPECIFIC GATE OR NONE]

Preserve material failures and authoritative evidence. Apply Governor's scratch artifact rules at closeout. Report delivered slices, verification and review results, corrections, unresolved findings, exact commits and Git state, remaining roadmap position, retained and removed artifacts, and material deviations. Stop before work beyond the authorized boundary.
~~~

## 4. Implementation Rework

~~~markdown
# Governor — Implementation Rework Assignment

Use your installed Governor skill. Correct the identified findings within the existing candidate's accepted requirements.

## Assignment

- Repository — [PATH]
- Candidate — [BRANCH, HEAD, AND DIFF OR COMMIT RANGE AS APPLICABLE]
- Affected slice or phase — [IDENTIFIER]
- Accepted requirements — [PLAN OR CONTRACT]
- Review findings and owner feedback — [EXACT FINDINGS AND EVIDENCE]

Inspect the actual diff, relevant code and tests, and original evidence. Classify each finding as an in-scope product defect, a test or verification defect, an environment or tooling failure, an inherited issue, or a scope or architecture decision for the owner. Use a small discriminating experiment where the cause is uncertain.

Make the smallest coherent corrections. Preserve accepted architecture, unaffected behavior, unrelated user changes, applicable qualification evidence, and original failure records. Add regression coverage where appropriate. Preserve the strength of existing assertions and escalate material changes to requirements or scope. Recheck invalidated or uncertain evidence, obtain independent rereview of material corrections, and inspect the complete resulting candidate.

## Authority and handback

- Correction scope — [EXACT CORRECTIONS AUTHORIZED BY THE OWNER]
- Branch creation or switching — [EXACT PERMISSION OR NONE]
- Commit — [EXACT PERMISSION OR NONE]
- Push — [EXACT REMOTE REF AND CADENCE OR NONE]
- Integration — [EXACT TARGET AND PERMISSION OR NONE]

Report each finding's classification, root cause and disposition, changes and changed paths, fresh and retained verification, rereview verdict, Git state, and unresolved blockers or deviations. Stop at the agreed acceptance boundary.
~~~

## 5. Commit

~~~markdown
# Governor — Commit Ratified Candidate

Use your installed Governor skill. Commit the exact owner-accepted candidate.

## Assignment

- Repository — [PATH]
- Approved branch and expected parent HEAD — [BRANCH AND COMMIT]
- Approved candidate — [EXACT DIFF OR TREE, APPROVED PATHS, OWNER ACCEPTANCE RECORD]
- Approved Conventional Commit message — [MESSAGE]
- Verification and review evidence — [REFERENCES]

Confirm the branch and parent, and verify the candidate against the reviewed and accepted material. Stage only the approved content, inspect the complete staged diff, check for unrelated staged changes, and run `git diff --cached --check`. Verify that applicable qualification evidence remains valid. Stop on a material mismatch and obtain renewed review and owner acceptance. Use the supported commit procedure, account for mandatory hook effects, and preserve any applicable passing evidence.

## Authority and handback

- Branch creation or switching — [EXACT PERMISSION OR NONE]
- Stage and commit the accepted candidate — [EXACT PERMISSION]
- Source corrections, amend, push, integration, tags, and next task — None

Verify the actual commit, parent, tree, changed paths, hook effects, and final Git status. If a hook materially changes the committed candidate, report the discrepancy and stop for review. Report the verified commit and contents, final Git state, and material limitations. Stop after the authorized commit.
~~~

## 6. Investigation

~~~markdown
# Governor — Investigation Assignment

Use your installed Governor skill. Investigate the question for an owner decision.

## Assignment

- Repository — [PATH]
- Technical or architectural question — [EXACT QUESTION]
- Context — [KNOWN FACTS AND SOURCE REFERENCES]

Establish current repository and Git state. Inspect relevant source, tests, architecture, roadmap, and accepted evidence. Report what exists and can be reused, what the evidence establishes, what remains uncertain or contradicted, and which options are technically viable. Recommend the smallest useful next experiment or decision. Run bounded, non-destructive probes only within the scope below.

## Authority and handback

- Read-only inspection — [SCOPE]
- Bounded probes — [EXACT PERMISSION OR NONE]
- Production changes and Git mutations — None

Provide exact paths and evidence for observations, identify inferences and material risks, and report unresolved questions and justified recommendations. Stop after delivering the investigation.
~~~

## 7. Independent Candidate Review

~~~markdown
# Governor — Independent Candidate Review

Apply the review standard in Project Governor Prompt v3 where available. Keep this assignment read-only.

## Review target

- Repository — [PATH]
- Exact candidate — [PLAN PATH AND VERSION, STAGED DIFF, BRANCH AND HEAD, OR COMMIT RANGE]
- Requirements — [REQUESTED OUTCOME, ACCEPTANCE CRITERIA, SETTLED DECISIONS, EXCLUSIONS]
- Claimed verification — [EVIDENCE REFERENCES]

Inspect the identified candidate and relevant repository state directly. For a plan, assess the baseline, feasibility, architecture, scope, dependencies, and coverage of the acceptance criteria. For implementation, assess correctness, architecture and dependency direction, security and data integrity, ownership and concurrency, error behavior, regression coverage, documentation, and unintended changes where relevant. Verify that evidence applies to the candidate and covers the affected requirements.

For each material finding, report the affected requirement, severity, exact source evidence or reproducible observation, and smallest suitable correction. Distinguish candidate defects, inherited issues, unsupported assumptions, and optional improvements. Keep files, tests, plans, the Git index, and commits read-only. Identify verification gaps if the necessary evidence is unavailable within that boundary.

## Verdict

Return `Accepted`, `Accepted with limitations`, or `Rework required`. Include findings, unverified claims, the smallest correction set if needed, and readiness for owner ratification or acceptance. Stop after review. The owner decides whether to ratify the candidate and authorize subsequent work.
~~~

## 8. Integration and Publication

~~~markdown
# Governor — Integration and Publication Assignment

Use your installed Governor skill. Carry out the Git operations the owner has explicitly authorized below.

## Accepted source and destination

- Repository — [PATH]
- Accepted source branch and HEAD — [BRANCH AND COMMIT]
- Reviewed candidate and owner acceptance — [REVIEWED TREE AND DECISION RECORD]
- Integration target and expected HEAD — [TARGET BRANCH AND COMMIT, IF APPLICABLE]
- Publication — [REMOTE, EXACT SOURCE AND DESTINATION REFS, EXPECTED PUBLISHED COMMIT, IF APPLICABLE]

Before any mutation, verify the authorized refs, accepted source and tree, working-tree state, and ancestry. Stop on unexpected divergence, changed accepted material, or unreviewed changes that affect the operation. Protect accepted history and any unrelated local work.

If integration is authorized, fast-forward the named target to the accepted commit and verify the resulting target. History rewrites, merge commits, squashes, rebases, and cherry-picks are outside this assignment. If publication is authorized, push the specified ref and verify its exact remote identity before reporting success. Create a tag only with explicit authority for its name and target. Publication of a tag requires its own explicit ref authorization.

## Authority and handback

- Branch creation or switching — [EXACT PERMISSION OR NONE]
- Fast-forward integration — [EXACT TARGET AND PERMISSION OR NONE]
- Push — [EXACT REMOTE, SOURCE AND DESTINATION REFS, AND PERMISSION OR NONE]
- Tag creation — [EXACT TAG NAME, TARGET, AND PERMISSION OR NONE]
- Source modification, branch or tag deletion, and next phase — None

Report starting and final refs, the verified fast-forward and integrated commit if applicable, the push result and verified remote ref if applicable, any authorized tag, final Git state, and deviations or blockers. Stop after the authorized operations.
~~~
