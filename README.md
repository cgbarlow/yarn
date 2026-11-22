# Yarn

A story a child wants to come back to, and a daily nudge that makes a caring adult's ten minutes count.

Yarn is a concept for an AI-based learning system in the spirit of the Young Lady's Illustrated Primer from Neal Stephenson's *The Diamond Age*, shaped by Stephenson's later thinking and by what the evidence says about AI tutors so far.

**Status:** concept only. Nothing is built. This repo holds the thinking to date.

## The idea in one paragraph

Don't build an AI tutor. Build a book, not a being. A child hears a long-running story in which their skills move the plot. Code, not a language model, checks their answers. Each day one adult who loves them gets a single, well-aimed prompt for a two-minute conversation. The story ends, the support fades, and success means the child needs it less.

## Why the name

In New Zealand a yarn is both a story and a chat with someone. Those are the two halves of the system: the tale on the box and the talk at dinner.

## Docs

1. [Background](docs/01-background.md): what the Khanmigo evidence shows and how the Primer differs
2. [Principles and primitives](docs/02-principles-and-primitives.md)
3. [Reference architecture](docs/03-architecture.md)
4. [How it would be used](docs/04-how-it-is-used.md)
5. [Risks and objections](docs/05-risks-and-objections.md): dependence, parenting, companions, form factor
6. [Prior art](docs/06-prior-art.md)
7. [Naming](docs/07-naming.md)
8. [Open questions](docs/08-open-questions.md)
9. [Sources](docs/09-sources.md)
10. [Yarn on Pop's Radio](docs/10-pops-radio.md): building it as a live Story mode on the radio, with the family in the loop

Also: the original [council report](docs/council-report.md) comparing Khanmigo with the Primer.

## Three rules that keep it honest

1. The model never judges correctness. Code does.
2. The model never writes to the learner model directly. Only verified events do.
3. The child never gets an open chat box.

## The test it has to pass

A parent reading a book with their child every night already does most of this, free, with no architecture. Yarn only earns its place if it gets more families to that, or makes the ten minutes count for parents who are stretched. If it can't beat the bedtime story, it shouldn't exist.
