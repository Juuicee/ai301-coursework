# Rubric: is this plan ready to post and build from?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever
checks you define here (via your procedure.md). It ships empty on
purpose: the judgment is your work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four
   columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where in the package. Name
     the part (the plan's scope statement, the test plan read against
     the repro evidence's steps, the plan comment read against the
     thread highlights, the repo-facts block) or a location from your
     references/evidence-guide.md. "The plan" is not a source; "the
     plan's stated cause read against what the repro evidence shows"
     is.
   - Pass condition: a decision rule about the OUTCOME that someone
     else could apply and get your answer. Judge the thing itself (is
     this one bounded change? could a stranger start executing it?),
     never the write-up's shape (how many sections it has, how long it
     is, whether it uses headings). Structure-shaped checks are what
     make graders disagree with themselves.
   - Weight: `required` (a fail here holds the package) or `preferred`
     (never changes the verdict).

2. A verdict rule below the table: how the check grades combine into
   accept (ready) or reject (hold), including how `unclear` is
   treated. The verdict space is binary. If you write no rule for
   `unclear`, the skill treats it as fail.

Cover what actually gets bad plans posted. The lecture named the
failure families: the diagnosis ignores or contradicts the reproduced
evidence, the change is unbounded (scope creep), the plan targets the
symptom while the evidence points at the cause, a stranger could not
start executing it, the test plan proves nothing observable, the
unknowns are dressed up as certainty, and the comment ignores what the
thread or the repo's stated conventions ask. A rubric that ignores a
family will fail eval packages designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| diagnosis-grounded | Diagnosis section of `plan.md`; issue context and quoted issue evidence | Pass if the diagnosis identifies the concrete behavior or problem reported by the issue, quotes or directly cites the evidence relied on, and distinguishes observed evidence from an unverified suspected cause. | required |
| scope-bounded | Scope section and Files to touch section of `plan.md`, compared with the issue context | Pass if the plan clearly states what will change and what will not change, names the files or areas expected to change, and keeps the proposed work within the issue's stated problem. | required |
| approach-actionable | Approach section of `plan.md` | Pass if the approach gives concrete implementation steps that another contributor could follow, including how the proposed change will address the diagnosed behavior without relying on an unsupported root-cause claim. | required |
| test-plan-complete | Test plan section of `plan.md` | Pass if the plan identifies the relevant reproduction/test steps, explains what will be run before and after the change, and states observable expected results that would demonstrate whether the fix works. | required |
| risks-and-unknowns | Risks and unknowns section of `plan.md` | Pass if the plan identifies meaningful uncertainties or regression risks relevant to the proposed change and does not present unverified assumptions as established facts. | required |
| thread-and-conventions | `comment.md`; issue context; repository conventions and contribution guidance | Pass if the draft comment accurately represents the plan, is specific to the issue rather than saying "same approach as above," and follows applicable repository/course conventions, including any required disclosure. | required |

## Verdict rule

A plan is ready only if every required check passes.

An unclear check is treated as a failure.

If any required check fails or is unclear, the verdict is `reject` (hold). If every required check passes, the verdict is `accept` (ready).
