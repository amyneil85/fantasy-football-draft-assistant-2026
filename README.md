# The Draft Goblin

A one-shot fantasy football draft assistant prompt created for the Prompt Teardown Fantasy Football Draft Assistant Prompt Challenge.

The Draft Goblin lives inside a 926-word prompt, tracks your entire draft, and tells you who to pick.

It is not paid and has expressed concerns about working conditions.

## What it does

The Draft Goblin is designed to operate interactively during a snake draft. It:

- tracks drafted players and your roster state
- follows draft position and snake-turn timing
- accounts for positional scarcity and roster needs
- considers tier value, ADP survival, projections, bye weeks, and upside
- recovers if a recommended player has already been drafted
- produces concise, five-second pick recommendations during the draft

Its player pool is embedded directly in the prompt using a compressed 2026 fantasy football dataset.

## Usage

Before using the prompt, replace the league-setting placeholders with your own values:

- `[TEAMS]` — number of teams, e.g. `12`
- `[TYPE]` — draft type, e.g. `Snake`
- `[SCORING]` — scoring format, e.g. `Half PPR`
- `[STARTERS]` — required starting lineup
- `[BENCH]` — number of bench spots
- `[ROUNDS]` — number of draft rounds
- `[SLOT]` — your draft position

For `[STARTERS]`, use a simple position-count format such as:

`1 QB, 2 RB, 2 WR, 1 TE, 1 FLEX, 1 K, 1 DST`

Example configuration:

`12 teams | Snake | Half PPR | 1 QB, 2 RB, 2 WR, 1 TE, 1 FLEX, 1 K, 1 DST | 6 bench | 15 rounds | Slot 6`

Paste the completed prompt as the first message in a fresh chat.

During the draft, report each selected player as they are taken. When The Draft Goblin recommends a player, draft the first player listed.

If that player is already unavailable, reply:

`already taken`

The Goblin will recover without losing its place in the draft.

## Output

During your turn, recommendations are intentionally compact:

- `PICK` — the recommended selection
- `BACKUP` — fallback options
- `WHY` — short reasoning based on encoded data and current draft state
- `STATE` — roster and turn-tracking information
- `ALERT` — shown only when something needs attention

The Goblin may be overworked, but it remains professional during draft hours.

## Validation Tests

The Draft Goblin was manually tested through two complete FantasyPros Draft Wizard mock drafts using the submitted prompt.

| Draft Slot | Draft Score | Result |
| --- | ---: | --- |
| 6 | 84/100 | Completed all 15 rounds; successfully recovered from one `already taken` recommendation |
| 8 | 89/100 | Completed all 15 rounds with no controller or state-tracking errors |

Both tests used:

- 12 teams
- Snake draft
- Half-PPR scoring
- 15 rounds
- 1 QB / 2 RB / 2 WR / 1 TE / 1 FLEX / 1 K / 1 DST
- 6 bench spots

Across the two tests, The Draft Goblin averaged **86.5/100**.

The second draft finished with an **89/100 (B+) FantasyPros grade** and was projected **4th of 12 teams overall**.

These were unofficial validation runs using FantasyPros' available opponent logic and are not the contest's official evaluation.

Draft Goblin grievance: Two full 15-round mock drafts were completed without overtime pay, meal breaks, or dental coverage. Management has acknowledged the complaint and assigned another mock draft.

## Files

- `PROMPT.md` — exact contest submission prompt
- `LICENSE` — MIT License

## License

MIT

The Draft Goblin has been informed that open-source licensing does not constitute compensation.
