# Writing style for AI

Opinionated AI writing style that follows **a subset derived from Simplified Technical English (ASD-STE100)**.

Some AI models are getting 'prose' heavy, but universal application of the full STE-100 spec on everything isn't the answer because it's built for procedures which convey factual statements but not for analysis where nuance and caveats are abundant.

Therefore, we don't use STE for in-code comments and issue analysis, but we can use a subset that is especially scoped for commit messages, issue bodies, and issue/PR comments. Glossary-based ubiquitous language is very important and should be used everywhere.

## Good bits

Short sentences, active voice, no metaphors, no -ing nominalisation, concrete verbs.

## Naff bits

Dictionary discipline using "verify" just because it's an approved word when "shows" vs "proves" is a genuine distinction. We want to keep the uncertainty of hedges such as "likely" otherwise they'll be turned into "definitely".

## Scoped application

### Commit messages

Uses the subset because metaphors read poorly. "Same error as issue #2" is better than "wearing a different hat".

### Issue bodies

Broken into sections:

- Reproduction steps, expected/actual, environment: STE-style, these are procedures.
- Background and analysis: normal prose, because that's where you reason about causes and trade-offs, and STE's preference for declarative certainty strips hedging you may actually mean (same scenario for in-code comments).

### Issue comments

May require the lightest touch. They're conversation; forcing STE makes them stilted and, worse, can make uncertain claims read as certain ones. Ubiquitous language yes, sentence-shape rules as a default habit.
