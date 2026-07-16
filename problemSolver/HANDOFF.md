# ProblemSolver Project Handoff

## Project purpose

ProblemSolver is a reusable framework for working through real problems that involve uncertainty, institutions, delays, handoffs, incomplete information, and multiple possible paths.

The project began with a specific problem encountered today, but the underlying issue was broader: when a person is trying to obtain help, the burden of understanding the system, preserving the history, identifying the next action, and recovering from failed handoffs often falls on the person who is already under stress.

ProblemSolver is intended to make that work visible, structured, and manageable.

---

## Today's problem

The immediate problem was access to existing VA mental-health care.

The user was already an active mental-health patient and had recurring VA Video Connect appointments. A new identity-verification requirement appeared without advance notice. The user had previously been able to log in normally, but the new verification process failed to match the existing VA record.

An audio-only fallback was attempted, but the interaction felt unwelcoming and the user left without receiving care that day.

The practical failure was not simply “a login problem.” It involved several connected issues:

- an unexpected process change;
- a mismatch between identity verification and an existing patient record;
- no clear owner responsible for restoring access;
- a fallback that did not preserve a usable care experience;
- a failed handoff between the technical system and the care system;
- loss of care despite the user already being enrolled and scheduled.

This exposed a common pattern: an institution may have many departments, records, procedures, and fallback channels, while the person seeking help is left to reconstruct the entire problem alone.

---

## How the problem became ProblemSolver

The discussion moved from solving one access failure to designing a general method for handling problems of this kind.

The core realization was that many difficult problems share the same structure:

1. A real need exists.
2. A process is supposed to meet that need.
3. Something fails at a boundary, handoff, rule, record, or communication point.
4. Responsibility becomes unclear.
5. The person must repeat the history, find the correct office, test possible paths, and remember what happened.
6. The problem is often treated as closed before the original need is actually met.

ProblemSolver turns that experience into a structured case.

Instead of relying on memory or repeatedly starting over, each case should preserve:

- the original need;
- the triggering event;
- the history;
- known facts and unknowns;
- stakeholders and responsibilities;
- barriers and failed attempts;
- next actions;
- evidence;
- communication records;
- escalation paths;
- test points;
- closure criteria;
- lessons for improving the framework.

The framework should be useful for healthcare access, benefits, housing, employment, finances, repairs, administrative processes, learning goals, and other problems that unfold over time.

---

## Working philosophy

ProblemSolver should be practical rather than theoretical.

A case is not complete because a phone call was made, a form was submitted, or a referral was entered. It is complete only when the original need has been met and the result has been verified.

The framework should:

- preserve history so the user does not have to reconstruct it repeatedly;
- distinguish facts, assumptions, hypotheses, and unanswered questions;
- identify who owns each part of the process;
- make the current state and next action obvious;
- support escalation without losing the original goal;
- record failures as information rather than treating them as dead ends;
- remain useful during stress, confusion, delay, or interruption;
- evolve through versioned rulesets as real cases reveal weaknesses.

---

## First project goals

### 1. Create the initial ruleset

Create a versioned ProblemSolver ruleset that defines:

- the purpose of the framework;
- the structure of a case;
- required fields;
- problem states and status values;
- evidence and source handling;
- stakeholder and responsibility mapping;
- action planning;
- communication logging;
- handoffs and escalation;
- test points;
- closure criteria;
- lessons learned;
- ruleset feedback.

The active ruleset should remain unsuffixed:

```text
ruleset.json
```

When a new version replaces it, rename the outgoing active file using its version, for example:

```text
ruleset-v1.0.json
```

The new active version then remains:

```text
ruleset.json
```

A readable Markdown companion should be maintained alongside the JSON ruleset.

### 2. Define the first case-file format

Create a reusable case format that can hold both the model and the working record.

The first case should include at least:

- case ID;
- title;
- type;
- priority;
- status;
- original need;
- problem statement;
- desired outcome;
- triggering event;
- relevant history;
- known facts;
- unknowns;
- assumptions;
- stakeholders;
- process map;
- barriers;
- attempted actions;
- evidence;
- current state;
- next action;
- escalation path;
- test points;
- closure criteria;
- case log;
- lessons learned;
- ruleset feedback.

### 3. Begin testing with one real-world problem

The first modeling sandbox will be:

```text
Obtaining dental care
```

This should not be a fictional demonstration. It should be a real working case that helps the user make progress toward obtaining actual dental care.

The case will test whether ProblemSolver can:

- define the dental-care need precisely;
- reconstruct relevant history from existing information;
- distinguish urgent treatment needs from longer-term restoration;
- identify eligibility, coverage, referral, scheduling, transportation, cost, and communication barriers;
- map possible care routes without losing track of previous attempts;
- identify the next useful action;
- preserve records of calls, messages, appointments, estimates, denials, and referrals;
- define test points for whether each route is actually working;
- escalate when a route stalls;
- close only when the dental need has been meaningfully addressed.

### 4. Use the dental case to improve the ruleset

The first ruleset should be treated as a working draft.

As the dental-care case is used, record:

- fields that are missing;
- fields that are unnecessary;
- unclear status values;
- places where the next action is hard to identify;
- weak handoff or escalation rules;
- communication needs;
- useful interface ideas;
- repeated patterns that should become standard rules.

Those findings should become the basis for version 1.1.

### 5. Begin designing usable interfaces

After the initial ruleset and case format exist, begin designing simple interfaces for:

- opening a case;
- viewing the current state;
- recording a new event;
- adding evidence;
- identifying the next action;
- tracking waiting periods and follow-ups;
- viewing stakeholder responsibilities;
- escalating a stalled case;
- marking test points;
- reviewing closure criteria.

The interface can begin as structured Markdown or HTML before any more complex application is built.

---

## First expected outputs

The first stage of the project should produce:

```text
ProblemSolver/
├── HANDOFF.md
├── ruleset.json
├── ruleset-v1.0.md
├── cases/
│   └── obtaining-dental-care/
│       ├── case.md
│       ├── case.json
│       └── evidence/
└── README.md
```

The exact structure may change as the project develops.

The initial useful results should be:

1. a clear ProblemSolver ruleset;
2. a readable explanation of the ruleset;
3. a working dental-care case;
4. an explicit current state and next action;
5. a record of ruleset improvements discovered through use;
6. an early interface concept for managing cases.

---

## Important distinction

The VA access failure explains why the project was needed.

The dental-care case is the first deliberate sandbox for building and testing the framework.

The project should preserve both:

- the general lesson from today's failure: systems often lose responsibility at boundaries and handoffs;
- the practical goal of the first case: help the user obtain real dental care.

ProblemSolver succeeds only when it improves the ability to act on real problems, preserve progress, and reach verified outcomes.
