# Unit 2 — Claim and Reproduce

Path: `beat-1-sandbox/unit-2/reproduction.md`

Record of your claim and reproduction on the issue you chose in Unit 1, and of the
evaluation runs that produced `eval-run.txt`. This file is graded at the path above; a copy
kept anywhere else in the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the wrong
label is not graded.

---

## Your identity upstream

**GitHub username**

[Your GitHub username, exactly as it appears on your profile — no `@`, no profile URL. Your
comments upstream are identified by this name.]

Juuicee
---

## Posted upstream

**Claim comment**

[Link to the comment where you claimed the issue. Use the comment's own permalink, not the
issue page on its own. **Then paste the text of that comment underneath the link** — the
pasted text is what this field is graded on, so copy across what you actually posted.]

**Reproduction comment**

[Link to the comment where you posted your reproduction. It must record the environment
(OS, relevant versions, code state), steps a stranger could follow, and what you observed.
**Then paste the text of that comment underneath the link** — the pasted text is what this
field is graded on, so copy across what you actually posted.]

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

[Quote one check from the `rubric.md` you uploaded to `tools/repro-check/`, exactly as it reads now.
Then say why it reads that way — what you revised to get there, or what you rejected in
favour of it.]

- conventions-respected Candidate report follows applicable repository requirements, including any stated AI-use or disclosure requirement; when the repository requires disclosure of AI assistance, the candidate comments disclose the tool used and the extent of assistance as required.

This check is included because a reproduction can contain technically useful evidence while still failing the repository's contribution requirements. The check therefore looks beyond whether the bug was reproduced and verifies that the report follows the applicable contribution policy, bug-report template, and other repository conventions.

In particular, the check explicitly accounts for AI-use or disclosure requirements when the repository has them. This prevents a technically complete reproduction from being considered ready when it does not satisfy a requirement for how the contribution must be presented.

The check is required because the verdict rule states that every required check must pass. An unclear check is also treated as a failure, so missing evidence about repository requirements cannot simply be assumed to be acceptable.
**Trade-offs**

[Every check gives something up. Any one of these is a complete answer: a package whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

The conventions-respected check gives up some flexibility in exchange for consistency with the repository's contribution rules. A reproduction may contain strong technical evidence but still fail this check if it does not follow an applicable repository requirement.

This can make the rubric stricter than a purely technical reproduction test, but that trade-off is appropriate because the question being graded is whether the reproduction package is ready to post, not merely whether the underlying behavior was observed.

The check also avoids requiring unnecessary conventions that are not actually applicable: its pass condition is limited to the repository requirements that apply to the candidate report.

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/repro-check/`.
