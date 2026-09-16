# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

[**Issue link**](https://github.com/codepath/pathreview-ai301-fa26-s1/issues/70)

[The individual Path Review issue page. A link to the repository or the issue list
does not satisfy this field.]

**Verdict output**

[Your skill's live-mode output for this issue, pasted verbatim and ending with the
fenced JSON verdict block. A summary does not satisfy this field.]

**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

```
paste the output here, including the closing JSON block
```

---

## Eval iterations

Quote source text directly in each field below. Paraphrase does not satisfy them.

[The agreement score of each run you did, in order. A single run is a complete answer if
only one run occurred. **The last score in your list must match the agreement line in the
`eval-run.txt` you committed** — that file is the record of your final run.]

**Issue analysis**

[One scored issue, identified by id (`issue-01` through `issue-20`; the `calib-`
issues are not scored). State your rubric's decision, the gold label, and the
reasoning that produced your rubric's result.]

The issue is accepted by my rubric based on the evidence I reviewed. The issue describes a concrete README parser bug: ReadmeParser.parse() returns zero sections for a conventional README with #/## headings. The issue identifies the relevant parser and test files and estimates 2–4 hours of work. I also checked that there was no assignee, no linked PR, and no comment indicating that another contributor was actively working on the issue.

**Check rationale**

[One check from the `rubric.md` uploaded to `tools/issue-select/`, quoted as it is
currently written, with the reasoning behind its current form.]

| project-active | repo-facts block: last push to any branch, last 5 default-branch commits, and maintainer first-response sample | Pass if the repo had a push within the last 90 days AND at least one of the five sampled issues has a maintainer/owner/member/collaborator response within 30 days | required |

I included this check because a first contribution should be going into a repository that is active and has maintainers who participate in the project. The check uses specific activity and response evidence rather than relying only on whether the repository appears active.

**Trade-offs**

[What the quoted check gives up. Any one of these is a complete answer: an issue whose
result it changes, a canary you re-ran with `--only`, a case you accept it will miss, or a
stated reason nothing changed elsewhere. "Nothing changed, and here is how I know" earns
the point in full when the reason follows.]

This check can reject an otherwise manageable issue when the repository does not have enough recent activity or maintainer-response evidence. That trade-off is intentional because an inactive repository can make a first contribution harder even when the issue itself is technically straightforward.
---

## Selection rationale

Graded on whether all three are answered, in your own words. Not on how good the
reasoning is, and not on length — a short honest answer to each earns the full marks.
This is also the basis for the claim comment you write in Unit 2.

The issue fits the time available because the estimated effort is 2–4 hours, and the task is limited to a specific parser bug and its covering test. It also fits my interest in working on a concrete software bug rather than a large project redesign.

The verdict correctly identified that the issue has a bounded scope and that there is no current assignee or linked pull request. I also weighed the specific files involved, the estimated effort, and the fact that the issue provides a clear description of what is currently failing. Those details are not all captured by the rubric.

The anticipated difficulty in claiming it is that it is labeled intermediate difficulty, so it may require understanding how the README parser performs section extraction before making the fix. However, the issue provides the relevant files and a specific failing behavior to investigate.

[Answer all three:

1. The issue's fit to your interests and to the time available.
2. What the verdict identified correctly, and what you weighed that the rubric could
   not.
3. The anticipated difficulty in claiming it.]



---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
