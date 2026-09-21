# Rubric: is this reproduction package ready to post?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever
checks you define here. It ships empty on purpose: the judgment is your
work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four
   columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where in the package. Name
     the part (the claim comment, the repro report's environment
     record, the artifacts read against the issue's description, the
     repo-facts block) or a location from your
     references/evidence-guide.md. "The report" is not a source; "the
     output excerpt read against the error the issue describes" is.
   - Pass condition: a decision rule about the OUTCOME that someone
     else could apply and get your answer. Judge the thing itself (does
     the artifact show the issue's behavior?), never the write-up's
     shape (how many steps it has, how long it is, whether it uses a
     template's headings). Structure-shaped checks are what make
     graders disagree with themselves.
   - Weight: `required` (a fail here holds the package) or `preferred`
     (never changes the verdict).

2. A verdict rule below the table: how the check grades combine into
   accept (ready) or reject (hold), including how `unclear` is
   treated. The verdict space is binary. If you write no rule for
   `unclear`, the skill treats it as fail.

Cover what actually gets bad packages posted. The lecture named the
proof families: the environment is recorded, the steps are complete
and followable, the behavior shown matches the issue (not an adjacent
one), the outcome is stated honestly (an evidenced cannot-reproduce is
a pass, a confident wrong-target is not), and the words respect the
repo's conventions. A rubric that ignores a family will fail eval
packages designed around that family.
-->


## Checks

| Check                  | Evidence                                                                                                                                          | Pass condition                                                                                                                                                                                                      | Weight   |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| environment-recorded   | Candidate repro report's Environment section; the issue context and the repo's bug-report template in the package                                 | Pass if the report identifies the relevant project/tool version and operating system and includes the setup details needed to repeat the reported test; details already established by the issue context need not be repeated when the report makes clear it used the same relevant environment. | required |
| reproduction-complete | Candidate repro report's preparation, reproduction commands/actions, and observed result, read against the issue's stated reproduction conditions  | Pass if the reported procedure gives another operator enough starting state, inputs, actions, commands, and trigger conditions to perform the same test and determine the observed outcome; an evidenced cannot-reproduce result passes when the attempted test is sufficiently specified and differences from the issue's environment are identified. | required |
| evidence-matches-issue | Issue description and reproduction details, plus the candidate report's commands, inputs, outputs, screenshots, logs, or other observed artifacts | Pass if the concrete evidence demonstrates the behavior described by the issue using the relevant input/state, and the observed result is consistent with the issue's reported behavior                             | required |
| outcome-honest         | Candidate repro report's Expected and Actual sections and the observed artifacts supporting them                                                  | Pass if the report distinguishes expected behavior from observed behavior and does not claim a reproduction, result, or scope that its evidence does not establish                                                  | required |
| conventions-respected  | Contribution policy, bug-report template, and other repository conventions included in the package's repo-facts block                             | Pass if the report follows applicable repository requirements, including any stated AI-use or disclosure requirement; when the repository requires disclosure of AI assistance, the candidate comments disclose the tool used and the extent of assistance as required. | required |


## Verdict rule

<!-- State how the grades above combine into accept or reject, and how
unclear is treated. Example shape (write your own): "accept if every
required check passes; preferred checks never change the verdict;
unclear counts as fail." --!>

A package is ready only if every required check passes. An unclear check is treated as a failure. If any required check fails or is unclear, the verdict is hold.
