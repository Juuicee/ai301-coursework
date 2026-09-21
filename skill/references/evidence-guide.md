# Evidence guide: where proof lives in a reproduction package

<!--
THIS IS THE PART YOU WRITE (new this week: week 1 handed you this file
finished; the scaffolding fades). The skill uses this guide as its map:
for every kind of proof a rubric check names, this file says WHERE to
find it in a package and WHAT GOOD LOOKS LIKE when you do.

Under each family heading below, write:

- Where it lives: the exact places to look. In an eval bundle (which
  section of the package: the issue context, the repo-facts block, the
  claim comment, the repro report and its parts). In live mode (where
  on GitHub or in the draft: the issue thread, the repo's docs, the
  student's draft comment).
- What good looks like: one or two sentences someone else could apply.
  Prefer observable conditions ("the versions named match what the
  issue targets, or the difference is called out") over adjectives
  ("environment is thorough").

A rubric check whose evidence this guide cannot locate is a check
nobody else can execute; your operator swap showed you what that feels
like. Write the map you wish your executor had.
-->

## Environment

**Where it lives:** In an eval bundle, check the candidate repro report's Environment section and Preparation/setup details. Compare them with the issue context and the repository's bug-report template in the repo-facts block. In live mode, check the student's draft/repro comment and the repository's issue template or documentation.

**What good looks like:** The report identifies the relevant project/tool version and operating system and records any installation method, dependency version, configuration, or other setup detail that materially affects the reproduction. If the reproduction intentionally uses a different version or environment from the issue, the difference is explicitly stated.

## Steps

**Where it lives:** In an eval bundle, check the candidate repro report's Preparation, Steps, commands, and Execution sections. Compare them with the issue's stated reproduction conditions. In live mode, check the reproduction report supplied by the student.

**What good looks like:** The reported procedure gives another operator enough starting state, inputs, actions, commands, and trigger conditions to perform the same test. A report may honestly conclude that the issue could not be reproduced; in that case, the attempted procedure still needs enough detail to understand what was tested.

## Behavior shown

**Where it lives:** In an eval bundle, compare the issue description and its reproduction details with the candidate report's commands, inputs, output excerpts, logs, screenshots, or other observed artifacts. In live mode, compare the same evidence in the student's reproduction report with the issue being reproduced.

**What good looks like:** The evidence demonstrates the behavior the issue actually describes, using the relevant input and state. A different error, a merely related failure, or an unsupported assertion does not establish the issue's behavior.

## Honesty

**Where it lives:** In an eval bundle, compare the candidate claim comment and the repro report's Expected, Actual, Analysis, and conclusion statements with the artifacts recorded in the report. In live mode, compare the student's claim and reproduction comments with the evidence they provide.

**What good looks like:** The author distinguishes expected behavior from observed behavior and limits conclusions to what the evidence establishes. An evidenced cannot-reproduce result is acceptable; claiming successful reproduction, scope, cause, or certainty beyond the evidence is not.

## Comms

**Where it lives:** In an eval bundle, check the candidate claim comment and repro report against the repository's issue template, contribution policy, and any AI-use or disclosure requirement stated in the repo-facts block. In live mode, check the student's comments against the issue thread and the repository's current contribution and disclosure requirements.

**What good looks like:** The comments accurately describe the author's intended work and reported results without unsupported claims, and they follow applicable repository communication and disclosure requirements. If the repository states that AI assistance must be disclosed, the required disclosure is present; if no such requirement is stated in the package, do not invent one.
