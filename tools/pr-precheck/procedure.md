# Procedure: how this tool grades a PR package

<!--
THIS IS THE PART YOU WRITE (second week running for the procedure).
Week 3 you wrote these steps for a plan package; this week the graded
object is a PR package, and the read that matters most is a
side-by-side: the diff against the plan, the evidence against the test
plan, the description against both. Your week-3 procedure is the
pattern; do not paste it unchanged, because its read order was built
for a different object.

Your rotation is the design brief again, and this week friction routes
three ways: a stall on WHAT to decide is a rubric gap, a stall on
WHERE to look is a procedure gap (this file), and a stall on what the
tool even reads or outputs is a frame gap (your SKILL.md). A complete
procedure lets someone who has never seen a PR package before grade
one exactly the way you would.

Under each stage heading below, write the concrete steps for that
stage. The one-line note under each heading says what a complete
procedure must decide there. Write steps, not intentions: "read the
plan's scope pair before opening the diff, and list the files the plan
names" is a step; "understand the change" is a wish.
-->

## Read order

<!-- What gets read, in what order, before any check is graded, and
what to note down from each part while reading. A complete procedure
decides where the plan sits in the order (before the diff? before the
description?) and says why the order matters for the side-by-side
checks that come later. -->

1. In live mode, read `scope.md` first and verify that the PR targets the scoped repository.
2. Read the issue and the plan, including the plan's scope pair, test plan, and deviation notes.
3. Read the PR diff and commit list.
4. Read the PR title and description.
5. Read the test-evidence section and captured check results.
6. Read the repository's PR template, contributing instructions, stated policy, and required disclosure information.
7. Read `rubric.md` and use its checks and pass conditions for the final grading.

This order establishes the intended change before inspecting what changed, so the diff and PR claims can be evaluated against the plan instead of becoming the definition of the plan.

## Evidence gathering

<!-- For each evidence family your rubric's checks name, the concrete
gathering move: which part of the package (or, live, which file, diff,
or page per your evidence guide) to pull the fact from, and what to
record. The load-bearing gathers this week are pairings: diff files
against plan scope, claimed evidence against the plan's test plan and
the repo's checks, description claims against diff contents. A
complete procedure leaves no check whose evidence an executor would
have to hunt for. -->

For **plan fidelity**, list the files and boundaries named by the plan, then compare them with every changed file in the diff. Record any deviation note that explains a mismatch. Compare the PR title and description with what the diff actually delivers.

For **test evidence**, identify the observable behavior the plan says should change. Read the supplied reproduction or before/after evidence and record the expected-after result and the visible outcome of the repository's own checks.

For **diff quality**, inspect the complete diff and commit list. Record unrelated files, unrelated hunks, debug leftovers, dead code, commented-out code, formatting churn, or other debris that makes the intended change harder to review.

For **standards and communication**, record each repository requirement from the PR template, contributing instructions, stated policy, and disclosure requirements. Compare those requirements with the PR description and communication.

## Check execution

<!-- How one check runs against gathered evidence: in what order the
checks execute, what an executor does when evidence for a check is
genuinely absent, and when a check may be graded without re-reading
the whole package. A complete procedure makes two executors grade the
same package the same way. -->

Execute rubric checks in the order listed in `rubric.md`.

For each check, use the evidence already gathered rather than re-reading the entire package unless the evidence is insufficient.

Grade only from observable evidence. If the required evidence is absent or cannot establish the pass condition, mark the check `unclear` rather than assuming success.

Do not create evidence that is not present in the package.

## Verdict assembly

<!-- How the per-check grades become the final accept or reject:
apply your rubric's verdict rule, state how unclear grades enter it,
and say what gets quoted in the output for the deciding check: the
check whose failure the verdict turned on. When more than one check
failed, your procedure picks which one gets quoted (first failing
required check in rubric order is a fine rule); nothing picks it for
you, so write the rule down. A complete procedure produces the same
verdict from the same grades, every time. -->

Apply the verdict rule in `rubric.md` after all checks have been graded.

If any required check fails, the verdict is `reject`. Preferred checks never change the verdict. Treat `unclear` as a failure unless the rubric explicitly states otherwise.

If multiple checks fail, identify the first failing required check in rubric order as the deciding check for the output evidence line.

Return the required JSON object as the final fenced block and place nothing after it.
