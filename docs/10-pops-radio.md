# Yarn on Pop's Radio

An idea: build Yarn as a mode on [Pop's Radio](https://github.com/cgbarlow/popsradio), not as a tablet app.

This is written against the Pop's Radio design as locked on 16 November 2026 (Design Decisions and the platform brief). Nothing in either project is built yet.

## Why it fits

Pop's Radio is already the shape Yarn was looking for: a single-purpose object with knobs, a speaker and a one-colour screen. It is something you use, not someone you know.

| Yarn needs | Pop's Radio already has |
|---|---|
| A story box on a shelf | A stout radio with a Mode knob: Talk, FM, Internet radio, Play |
| A channel to a caring adult | Talk: hold the orange button, pick a person or the family |
| The adult's side | The family app planned for Stage 3 |
| No engagement tricks | No adverts, accounts or purchases at the radio |
| Adults choose what is on it | The family switches modes on from the family app |
| A way to deliver new chapters | Signed overnight updates, and streaming as in internet radio |
| Simple pictures | A 2.4 inch black and white screen. An illustrated primer, in one colour |
| A one-off price | Apps bought once in the family app, not a subscription |

## How it would work

**Story is a mode.** The Mode knob gains a fifth stop, Story, if the family switches it on. The Select knob picks the chapter: tonight's, or replay last night's.

**The child answers with the knob.** The troll asks how to share 12 coins between 3 travellers. She turns the Select knob, the radio says each number aloud, and she presses to choose. This is the big change from the earlier design, and it helps three ways:

- **It keeps the microphone rule.** Pop's Radio never shares the microphone with apps. Knob answers need no microphone at all.
- **It drops children's speech recognition,** which is the weakest link in the voice design.
- **Checking is exact.** A chosen number is right or wrong. Code can verify it with no model involved.

**Chapters are made the night before.** The home hub writes tomorrow's chapter, including the branch for each answer she might give, turns it into audio, runs the safety checks and stores it. The radio only plays audio and follows branches. So there is no live language model in the room, nothing unexpected can be said, and a parent can preview any chapter in the ledger.

**Talk stays Talk.** Holding the orange button always talks, in every mode. "Tell Grandad what happened" is one press. An incoming message from the family pauses the story, as it does for everything else.

**Reading aloud goes to a human.** The knob can't check reading. A person can. The quest is "read this page to Grandad": she holds the button and reads, and he listens. The limit becomes the feature, because that is the ractor channel doing its job.

## Pop as the ractor

Pop's radio can show a short message from the family in large type with a chime. That is all the ractor channel needs:

> Ask her how she'd share 12 biscuits between 4.

He turns to her name, holds the orange button and asks. She hears her great-grandad on her radio. It fills the empty chair, and it gives him a job worth having.

Rules for this, in the spirit of "Looking out for Pop":

1. Off until Pop says yes, switched on with him there.
2. One prompt a day at most, at a time he chooses.
3. He can ignore it. Nothing tells the family he did.
4. It never tests or scores him.

## Which radio is the child's?

- **A second Pop's Radio** in the child's home works from Stage 2, and can share a channel with Pop's.
- **The kids' mini phone** on the roadmap is the natural home: a smaller, cheaper radio that only reaches people the parents approve. It has no mesh and no sockets. Yarn needs it to keep one knob, the screen and the speaker.

## Where it rubs

- **Scope.** Pop's Radio is at Stage 1, with the R1 hack day on 4 December. Yarn belongs in the "Later" rows. The only thing worth doing now is keeping the door open: a first-party mode should be able to play staged audio with branches chosen by the Select knob.
- **Store rules.** A third-party app can't use the microphone, the orange button or the talk channels. With knob answers Yarn fits those rules. Voice answers would make it a first-party mode only.
- **Running costs.** Channels are prepaid for life. Stories cost model time every night. So a story arc is bought once in the family app, priced to cover its own running costs, and it ends. That matches "the story ends" and keeps "no subscription, ever".
- **Where the hub lives.** The Pop's Radio service passes sealed messages and can't read them. Yarn's learner model and story state need their own home: a box in the house, or a host declared at review. Talk audio is never Yarn's to see.
- **Two audiences.** Pop's Radio is built for older people. A child's radio wants different sounds, words and limits. Session caps and a quiet time are new requirements.
- **Sealed clips.** A parent's "message from the Queen" can't be lifted from a talk channel, because the service can't open it. It has to be recorded for the story in the family app.

## Cheapest first test

The Pop's Radio site already has a simulator with the three knobs, the orange button and the real screen size. One hand-written chapter with three knob-answered challenges would show whether a child comes back for chapter two. No hardware, no model, no service.

## What this changes in the Yarn design

| Earlier thinking | On Pop's Radio |
|---|---|
| Voice-first tablet app | A mode on a radio |
| Child answers aloud | Child answers with the knob |
| Live model in the session | Chapters made and checked the night before |
| Speech recognition for children | Not needed |
| Reading checked by software | Reading aloud to a person |
| Fixed-term price as an open problem | Story arcs bought once in the family app |
