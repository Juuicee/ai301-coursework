# Voice guide: how I talk upstream

<!--
THIS IS THE PART YOU WRITE (new this week). Live mode reads this file
before any comment of yours goes out the door; eval mode ignores it
entirely, because your voice is yours and carries no gold labels.

This is not etiquette. "Be polite and concise" is advice for everyone
and therefore rules for no one. Write rules YOU need, in your own
words, each one concrete enough that the skill can hold a draft
against it and say which rule it breaks.

Three sections. Fill all three.
-->

## Who I am in threads

<!-- 2-3 lines. Who is talking when you comment on an issue: your
experience level stated plainly, what you are doing in this repo, what
readers can expect from you. This is the register your rules protect. -->

I am a tech fellow making my first contributions to this repository.
I will be clear that I am investigating/reproducing an issue rather than presenting myself as a maintainer.
Expect specific claims based on what I have observed.

## Rules I write by

<!-- 3-5 rules, drafted from the lecture's slide-12 moment. Each rule
needs a wrong/right pair from your own hand: one line you might
actually have written that breaks the rule, and the line you would
post instead. The pair is what makes a rule executable; a rule without
one is a wish.

Format each rule like this:

### Rule: <short name>

<The rule, one or two sentences.>

- Wrong: "<a line that breaks it>"
- Right: "<the line to post instead>"
-->

### Rule: Say what I actually know

I separate what I observed from what I think might be causing it.

- Wrong: "I found the bug and know exactly why this is happening."
- Right: "I reproduced the behavior and the failure appears to occur in this part of the decoder."

### Rule: Promise before I reproduce

When I first claim an issue, I describe what I plan to investigate instead of claiming that I already reproduced it.

- Wrong: "I reproduced this issue and will fix it."
- Right: "I'd like to investigate this issue and report back with what I can reproduce."

### Rule: Give evidence, not confidence

I do not use confidence or repetition as a substitute for evidence.

- Wrong: "This definitely happens everywhere and is obviously a major bug."
- Right: "I reproduced the behavior on Ubuntu 24.04 with version 4.53.3; the command produced the error shown below."

## Things I never post

<!-- A short list. Promises you cannot keep, tones you refuse,
shortcuts you know you reach for when tired. The skill quotes this
list back at you when a draft crosses it. -->

I never claim to have reproduced something I did not actually test.
I never claim that a failure is universal based on one environment.
I never state a suspected cause as a confirmed cause without evidence.
I never promise a fix, pull request, or deadline before I know I can deliver it.
