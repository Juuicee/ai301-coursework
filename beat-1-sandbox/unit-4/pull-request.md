# Unit 4 — Test and Submit

Path: `beat-1-sandbox/unit-4/pull-request.md`

Record of the pull request you opened against the Path Review repo, and of the evaluation
runs that produced `eval-run.txt`. This file is graded at the path above; a copy kept
anywhere else in the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the wrong
label is not graded.

---

## Your pull request

**Pull request**

[Link to the pull request you opened. It must be the pull request's own page on the Path
Review repo, not your fork's branch page.]

**Branch**

[The name of the branch the pull request comes from, exactly as it appears in your fork.
The naming shape is a type prefix, then the issue number, then a short description. **The
issue number in the branch name must be the number of the issue the pull request fixes** —
a name carrying any other number does not satisfy this field.]

## Eval iterations

Answer all four sections. Quote source text directly; paraphrase does not satisfy these
fields.

**Run history**

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

**Package analysis**

[Pick one scored package (`pkg-01` through `pkg-20` — the four `calib-` packages are never
scored). Name it by id, say what your rubric decided and what the gold label said, and
explain why your rubric read it that way.]

**Check rationale**

[Quote one check from the `rubric.md` you uploaded to `tools/pr-precheck/`, exactly as it reads now.
Then say why it reads that way — what you revised to get there, or what you rejected in
favour of it.]

> `| Plan fidelity | The diff's changed files and hunks read against the plan's stated scope, boundary, and deviation notes; the PR title and description read against the diff |`

I chose this check because Unit 4 is specifically concerned with preventing silent drift between the posted plan, the actual diff, and the claims made in the pull request. The check requires the grader to compare the actual changed files and claims against the plan rather than judging the PR from its description alone.

**Trade-offs**

[Every check gives something up. Any one of these is a complete answer: a package whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

The rubric prioritizes required checks that can prevent an unready PR from being submitted while keeping review clarity and communication quality as preferred checks. This means a PR can remain acceptable when its core evidence is complete even if a preferred communication check is unclear, while missing or unverifiable evidence for a required check causes the package to be held.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/pr-precheck/`.
- `eval-run.txt`
- `tools/pr-precheck/SKILL.md`
- `tools/pr-precheck/rubric.md`
- `tools/pr-precheck/procedure.md`
- `tools/pr-precheck/references/evidence-guide.md`
