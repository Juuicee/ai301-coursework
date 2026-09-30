# Procedure: how this skill grades a plan package

<!--
THIS IS THE PART YOU WRITE, and it is a new kind of part. Weeks 1 and
2, SKILL.md carried a numbered workflow and you only wrote judgment
files. This week the workflow is gone from the frame: SKILL.md says
"execute procedure.md", and these are the operating steps you author.
The machinery is in your hands now.

Your operator swap is the design brief. When your executor stalled
because your rubric said WHAT to decide but not HOW to find the
evidence, that was a procedure gap. This file is where those gaps get
closed: a complete procedure lets someone who has never seen a plan
package before (a groupmate, or the skill itself) grade one exactly the
way you would.

Under each stage heading below, write the concrete steps for that
stage. The one-line note under each heading says what a complete
procedure must decide there. Write steps, not intentions: "read the
repro evidence before the plan, and note what behavior it pins down"
is a step; "understand the context" is a wish.
-->

## Read order

<!-- What gets read, in what order, before any check is graded, and
what to note down from each part while reading. A complete procedure
decides the order (issue first? repro evidence first?) and says why
the order matters for the checks that come later. -->

1. Read `scope.md` first in live mode and confirm that the issue belongs to `codepath/pathreview-ai301-fa26-s1`.
2. Read `rubric.md` and list every check and its pass condition.
3. Read `references/evidence-guide.md` and use it to locate the evidence named by each check.
4. Read the entire candidate package before assigning grades.
5. Read the issue context first, then `plan.md`, then `comment.md`.
6. Do not use information from files that the candidate package does not contain unless the evidence guide explicitly identifies the issue or repository as the source.
   
## Evidence gathering

<!-- For each evidence family your rubric's checks name, the concrete
gathering move: which part of the package (or, live, which page or
thread location per your evidence guide) to pull the fact from, and
what to record. A complete procedure leaves no check whose evidence an
executor would have to hunt for. -->

1. For the diagnosis check, read the diagnosis section and identify the concrete issue evidence the plan relies on.
2. Confirm that quoted issue evidence actually supports the stated diagnosis.
3. For the scope check, compare the proposed files and changes with the issue's reported behavior.
4. For the approach check, read each proposed implementation step and determine whether another contributor could follow it without guessing at missing actions.
5. For the test-plan check, identify the reproduction/test steps, before/after runs, inputs, commands, and expected observable results.
6. For the risks and unknowns check, identify uncertainties and possible regressions relevant to the proposed implementation.
7. For the thread-and-conventions check, compare `comment.md` with `plan.md`, the issue context, and applicable repository/course conventions.
8. Quote or identify one concrete fact from the evidence for every check grade.
   
## Check execution

<!-- How one check runs against gathered evidence: in what order the
checks execute, what an executor does when evidence for a check is
genuinely absent, and when a check may be graded without re-reading
the whole package. A complete procedure makes two executors grade the
same package the same way. -->

1. Grade each rubric check independently as `pass`, `fail`, or `unclear`.
2. Mark a check `pass` only when its stated pass condition is satisfied by the available evidence.
3. Mark a check `fail` when the evidence contradicts the pass condition or the plan clearly violates it.
4. Mark a check `unclear` when the evidence required by the check is genuinely absent.
5. Do not treat polished writing, confidence, or length as evidence.
6. Do not infer an implementation root cause that the plan does not establish.
7. Do not require unnecessary details that the rubric does not name.
8. Record a short evidence fact or quote beside every grade.
   
## Verdict assembly

<!-- How the per-check grades become the final accept or reject:
apply your rubric's verdict rule, state how unclear grades enter it,
and say what gets quoted in the output for the deciding check. A
complete procedure produces the same verdict from the same grades,
every time. -->

1. Review all required checks after grading them individually.
2. Treat `unclear` as a failure.
3. Return `accept` only when every required check passes.
4. Return `reject` when any required check fails or is unclear.
5. The final verdict must be either `accept` or `reject`; there is no third verdict.
6. In live mode, also compare the draft comments against `voice-guide.md` and report any voice-guide rule they break.
