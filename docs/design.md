# Game Design Document

## Concept

A procedurally generated detective game where the player takes the role of a detective managing a caseload of simultaneous criminal cases. Cases are worked through a menu-driven UI using an expanding toolkit of investigative actions. Cases are not always immediately solvable — some are gated by toolkit progression, others are unblocked by results from different cases. Actions taken in one case can spawn new cases or alter the nature of existing ones. Efficiency across the whole caseload is a core mechanic. Hidden meta-narratives — organised crime networks, serial offenders — span multiple cases and must be identified by the player.

---

## Core Gameplay Loop

The player maintains an active caseload of multiple open cases at any one time. Cases are not always immediately solvable — some require toolkit capabilities the player hasn't yet unlocked, or are blocked on results that take time. The player must manage their attention across the caseload, progressing each case as their tools and circumstances allow.

1. Multiple cases are open simultaneously; the player selects which to work on at any point.
2. For a given case, the player reviews known facts and identifies leads to pursue.
3. The player selects investigative actions from their toolkit to expand the fact set.
4. Actions may produce new leads, spawn entirely new cases, or alter the nature of open cases — a witness interview might expose a second crime, or a forensic result might reframe the theory of an existing case.
5. When sufficient evidence is gathered, the player reaches a conclusion and closes the case.
6. Efficiency — minimising unnecessary actions and time across the whole caseload — is tracked and scored.
7. Over time, patterns across cases reveal meta-narratives that the player can choose to pursue.

---

## Cases

Each case is procedurally generated and contains:

- A crime type (e.g. homicide, theft, fraud)
- A crime scene with location details
- Details of victims, suspects, and witnesses
- An initial set of discoverable facts seeded at case start
- A hidden solution generated at case creation, against which the player's conclusion is evaluated

Cases are not isolated. They share a world — characters, locations, and organisations recur across cases, forming the substrate for meta-narratives. Some cases cannot be closed until the player has unlocked specific toolkit capabilities, or until another case yields a prerequisite piece of evidence. Investigative actions can spawn new cases: following a lead may uncover a second crime, and a result in one case may reframe the facts of another.

---

## Facts Panel

The facts panel is the player's read-only view of everything known about the current case. Facts are populated as the investigation progresses. Examples of fact types:

- Crime scene details (location, time, condition)
- Victim profile (identity, background, cause of death)
- Physical evidence (fingerprints, fibres, weapons)
- Witness testimony
- Suspect profiles and known associations
- Results of investigative actions (lab reports, interview transcripts, surveillance logs)

---

## Investigative Toolkit

The toolkit is the set of actions the player can take to generate new facts. Each action consumes a resource (time, budget, or both) and returns results after a delay or immediately depending on action type. Examples:

| Action | Description |
|---|---|
| Order DNA analysis | Submits physical evidence for lab processing |
| Bring in for questioning | Conducts a formal interview with a named individual |
| Stakeout location | Places surveillance on an address or venue |
| Obtain warrant | Unlocks searches of property or records |
| Run background check | Retrieves criminal history and associations for a named individual |
| Request forensic sweep | Detailed forensic examination of a scene or object |

Toolkit actions are unlocked progressively as the player advances (see Progression).

---

## Efficiency

Using tools costs resources. The player is scored on:

- Number of actions taken (fewer is better for a given outcome)
- Time elapsed (some actions are time-sensitive)
- Budget spent

Unnecessary or speculative actions are penalised. The player is incentivised to reason carefully before acting rather than exhausting all available options. Efficiency is measured across the whole caseload, not per case — the cost of actions in one case affects the overall score.

---

## Meta-Narratives

Across cases, the procedural generator seeds connections:

- Recurring perpetrators operating across multiple crimes (serial offenders)
- Criminal organisations with members appearing in separate cases
- Patterns in method, location, or victimology

These connections are not surfaced explicitly. The player must notice them independently — a name appearing in two case files, a location recurring, a modus operandi matching a prior case. Pursuing a meta-narrative is optional but unlocks additional content and progression rewards.

---

## Progression

The game uses an incremental unlock model:

- New toolkit actions are unlocked as the player closes cases and earns experience
- New case types and complexity tiers are introduced over time
- Meta-narrative threads unlock new investigative contexts (e.g. organised crime cases, serial killer task forces)
- The player's rank or title advances, reflecting their growing capability

---

## Platform and UI

The UI is menu-driven and text-forward. Target platforms:

- Web browser
- Desktop (Windows / macOS / Linux)
- Mobile (iOS / Android)

The interface is designed to work across all platforms without platform-specific variants — a single responsive menu-based UI.

---

## Multiplayer (Future)

The initial release is single-player. A future multiplayer mode is planned with the following design intent:

- Multiple players operate simultaneously in the same world
- Cases overlap — a witness or suspect in one player's case may be central to another's
- Co-operative play allows players to share evidence and coordinate actions across cases
- The shared world strengthens the meta-narrative layer, as players may independently notice the same patterns

Multiplayer is out of scope for the initial proof of concept but informs world-generation design decisions made now.
