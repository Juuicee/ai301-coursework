# Rubric: is this pull request ready to submit?

<!--
THIS IS THE PART YOU WRITE (fourth week running; this is the rubric's
final form in the sandbox). Your frame in SKILL.md executes whatever
checks you define here, via your procedure.md. It ships empty on
purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four
   columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where in the package. Name
     the part (the diff read against the plan's scope, the test
     evidence read against the plan's test plan, the description read
     against the diff, the repo-facts block's template asks) or a
     location from your references/evidence-guide.md. "The PR" is not
     a source; "the diff's changed files read against the plan's
     stated boundary" is.
   - Pass condition: a decision rule about the OUTCOME that someone
     else could apply and get your answer. Judge the thing itself
     (does the diff fall inside the plan plus its deviation notes? is
     the claimed evidence observable?), never the write-up's shape
     (how long the description is, how many commits there are).
     Structure-shaped checks are what make graders disagree with
     themselves.
   - Weight: `required` (a fail here holds the package) or `preferred`
     (never changes the verdict).

2. A verdict rule below the table: how the check grades combine into
   accept (submit) or reject (hold), including how `unclear` is
   treated. The verdict space is binary. State the `unclear`
   treatment explicitly: the frame here is YOUR SKILL.md, so a rubric
   that stays silent is only covered if your frame's grading
   discipline says what happens (the contract's own default is that
   an unverifiable claim fails).

Cover what actually gets bad PRs submitted. The failure families the
lecture named ARE the harness's scoring categories, same names as the
eval README: silent drift (the diff silently does more or less than
the posted plan, or the description claims fidelity the diff
contradicts), not tested (the evidence proves nothing observable, or
the repo's own checks were never run), unreviewable (debris or
unrelated hunks bury the change), and standards wall (the repo's
stated template and disclosure asks are ignored). Your evidence
guide's four headings map onto these one to one (plan fidelity =
silent drift, test evidence = not tested, diff quality =
unreviewable, standards and comms = standards wall), and the category
floor is scored on exactly these names plus clear accept. A rubric
that ignores a category will fail the eval packages built around
that category. And remember the honest-outcome
rule, fourth week running: a PR that honestly discloses a shortfall
can be ready; a rubric that equates "less than everything" with
"hold" fails the set.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Plan fidelity | The diff's changed files and hunks read against the plan's stated scope, boundary, and deviation notes; the PR title and description read against the diff | Every changed file is inside the planned boundary or explained by a deviation note, and the PR's claims accurately describe what the diff delivers | required |
| Test evidence | The test-evidence section or captured reproduction read against the plan's test plan and the repository's own checks | The package provides observable evidence for the planned behavior, states the expected-after result, and shows the relevant check outcome | required |
| Diff quality | The complete unified diff and commit list | The intended change is reviewable without unrelated files, unrelated hunks, debug leftovers, dead code, commented-out blocks, or formatting churn obscuring it | required |
| Standards and disclosure | The repository's PR template, contributing instructions, stated policy, and disclosure requirements read against the PR description | Required PR-template sections contain real content, required disclosures are present, and stated repository requirements are addressed | required |
| Description fidelity | The PR description read directly against the actual diff and test evidence | The description makes no unsupported claims and does not promise work, coverage, or test results that the package does not demonstrate | required |
| Deviation honesty | The plan's deviation notes read against differences between the plan and the delivered diff | Any genuine deviation is explicitly documented and tied back to the reason for the change; undocumented drift fails | required |
| Review clarity | The diff, commits, and test evidence read together | A reviewer can identify the intended fix, its evidence, and its outcome without relying on unsupported assumptions | preferred |
| Communication quality | The PR title and description read against the repository's communication requirements | The outgoing PR text is specific, accurate, and useful to a maintainer rather than boilerplate or unsupported confidence | preferred |

## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict;
unclear counts as fail." -->

Accept if every required check passes. Preferred checks never change the verdict.

An `unclear` grade on a required check counts as a failure because an unverifiable claim is not sufficient evidence of readiness. An `unclear` grade on a preferred check does not change the verdict.
