# Game Design Document

## Concept

A procedurally generated detective game where the player takes the role of a detective solving criminal cases. Cases are presented through a menu-driven UI, and the player uses an expanding toolkit of investigative actions to uncover facts and reach a conclusion. Efficiency in how tools are used is a core mechanic. Hidden meta-narratives spanning multiple cases — organised crime networks, serial offenders — emerge organically and must be identified by the player.

---

## Core Gameplay Loop

1. A new case is presented with an initial set of known facts.
2. The player reviews facts and identifies leads to pursue.
3. The player selects investigative actions from their toolkit to expand the fact set.
4. Based on accumulated evidence, the player reaches a conclusion and closes the case.
5. Efficiency — minimising unnecessary actions and time — is tracked and scored.
6. Over time, patterns across cases reveal meta-narratives that the player can choose to pursue.

---

## Cases

Each case is procedurally generated and contains:

- A crime type (e.g. homicide, theft, fraud)
- A crime scene with location details
- Details of victims, suspects, and witnesses
- An initial set of discoverable facts seeded at case start
- A hidden solution generated at case creation, against which the player's conclusion is evaluated

Cases are self-contained but share a world — characters, locations, and organisations can recur across cases, forming the substrate for meta-narratives.

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

Unnecessary or speculative actions are penalised. The player is incentivised to reason carefully before acting rather than exhausting all available options.

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
