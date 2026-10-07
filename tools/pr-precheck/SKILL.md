---
name: pr-precheck
description: Grade a PR package (a candidate pull request read against the plan it claims to implement and the issue that plan belongs to) and decide whether it is ready to submit. Use when checking your own branch, draft PR title, and description before opening the pull request, or when grading an eval package bundle.
---

# pr-precheck: rubric-driven PR grading

<!--
THIS IS THE PART YOU WRITE, and it is the last one: the frame itself.
Weeks 1 through 3 handed you a working SKILL.md and you filled the
files behind it; this week the frame ships as headings, and you write
what it says. The frontmatter above and the section headings below are
fixed (CONTRACT.md's layout rule); the instructions under each heading
are yours. Write instructions to the tool, in the imperative, the way
weeks 1-3's frames spoke to you: what to read, in what order, what to
refuse, what to emit. Your executor in the rotation is the test: a
frame gap they hit (cannot tell what the tool reads, or how a verdict
gets assembled) is a missing sentence here.

One section is not yours: the JSON schema in "Verdict and output" is
reproduced from CONTRACT.md verbatim and may not be altered. Your
words decide everything around it.
-->

## The question

<!-- State, in your words, the one question this tool answers and what
a PR package is: what artifacts it contains and what they are read
against. CONTRACT.md fixes the question; your frame has to say it so
the tool cannot wander into grading something else. -->

Answer exactly one question: **is this PR package ready to submit?**

A PR package contains the candidate pull request's title, description, commits, diff, and test evidence. Read those artifacts against the plan the PR claims to implement and the issue that plan belongs to. Do not grade unrelated work or answer a different question.

## Inputs and modes

<!-- Define both modes. Live mode: name every input (your plan.md with
its deviation notes, your branch's diff, your draft PR title and
description, your test evidence, your issue), where each comes from,
and what a house-chain student reads instead. The branch's diff is
everything the branch changes relative to the repo's default branch:
`git diff main...HEAD` (three dots), run from the working copy, is
the command that produces it; name the source that concretely. Eval
mode: state that the bundle is the whole world, nothing is fetched,
and every check runs with the full verdict rule. -->

In **live mode**, read the student's `plan.md` including deviation notes, the diff of the student's branch against the repository's default branch, the draft PR title and description, the available test evidence, and the issue the plan belongs to. For a house-chain student, use the house plan and house reproduction pack specified by the course instead.

In **eval mode**, treat the supplied package bundle as the whole world. Do not fetch anything, infer missing facts from outside the bundle, or read external files. Run every rubric check and apply the complete verdict rule.

## The scope seam (live mode only)

<!-- Tell the tool when to read scope.md, what to do with the rules it
finds there, what to refuse, and what to do when the scope's repo line
is an unfilled placeholder. State that eval mode ignores scope.md
entirely. CONTRACT.md names the required behavior; your frame has to
instruct it. -->

Read `scope.md` before grading anything else. Use it to determine the repository where the PR must live and the house rules that apply. Refuse to grade a PR outside that scope.

If the repository line in `scope.md` still contains a bracketed placeholder, stop without grading and tell the user to obtain the finalized Path Review repository from the instructor.

Ignore `scope.md` entirely in eval mode.

## The voice seam (live mode only)

<!-- Tell the tool when to read voice-guide.md, which outgoing text it
gates (the PR title and description), how to report a broken rule, and
why it never changes the verdict on its own. State that eval mode
ignores it entirely. -->

Read `voice-guide.md` before evaluating the outgoing PR text. Apply its rules to the draft PR title and description and report any broken rule.

A voice-guide violation does not change the verdict by itself unless a rubric check explicitly makes it part of the verdict. Ignore `voice-guide.md` entirely in eval mode.

## Component reads

<!-- Tell the tool how the pieces connect: rubric.md defines the
checks and the verdict rule, references/evidence-guide.md maps where
each evidence family lives, procedure.md is executed as written. Say
what the tool does when the procedure is silent on a step (report the
gap, never improvise around it) and what it does when rubric.md or
procedure.md has no content (the refusal rule, stated as an
instruction). -->

Read `rubric.md` to determine the checks, evidence requirements, pass conditions, weights, and verdict rule.

Read `references/evidence-guide.md` to locate evidence for plan fidelity, test evidence, diff quality, and standards and communication.

Execute `procedure.md` exactly as written. If the procedure does not specify how to handle a step, report that gap instead of inventing a new procedure.

If `rubric.md` has no actual checks or `procedure.md` has no actual procedure, refuse to grade and say that the required component is incomplete.

## Verdict and output

<!-- State the binary verdict space (accept means submit, reject means
hold) and instruct the tool to end its reply with the fenced JSON
block below, valid and last, with nothing after it. The schema is
CONTRACT.md's, verbatim; do not edit it. -->

```json
{
  "item": "<PR URL or bundle id>",
  "checks": [
    {"name": "<check name>", "grade": "pass|fail|unclear",
     "evidence": "<one line: the fact or quote that decided it>"}
  ],
  "verdict": "accept|reject"
}
```
The verdict is binary:

- `accept` means the PR is ready to submit.
- `reject` means the PR must be held.

Grade every rubric check and record the evidence that decided the grade. Treat `unclear` according to the rubric's verdict rule; when the rubric is silent, an unverifiable claim fails.

The reply must end with the following fenced JSON block, valid and last, with nothing after it:

```json
{
  "item": "<PR URL or bundle id>",
  "checks": [
    {"name": "<check name>", "grade": "pass|fail|unclear",
     "evidence": "<one line: the fact or quote that decided it>"}
  ],
  "verdict": "accept|reject"
}
```
## Grading discipline

<!-- Write the standing rules the tool grades under: evidence first,
grade the thing not the polish, the rubric decides, the procedure
decides how, and how unclear grades are treated when the rubric's
verdict rule is silent. CONTRACT.md states each as a guarantee; your
frame has to make them instructions. -->

Grade from evidence first. Every check must identify the fact or quote that decided its grade.

Grade the artifact itself, not the polish of its presentation. A short complete PR can pass, while a polished PR can fail if its diff, evidence, or claims are inconsistent.

The rubric decides what is checked and whether it passes. Do not override a rubric decision because the result feels wrong.

The procedure decides how evidence is gathered and checks are executed. Do not silently invent missing steps.

When evidence is genuinely unavailable, grade the check unclear; apply the rubric's verdict rule. If that rule does not specify otherwise, treat unclear as a failure.
