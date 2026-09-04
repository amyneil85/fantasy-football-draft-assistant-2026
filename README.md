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

## Test

The prompt was successfully run through a complete:

- 12-team league
- Snake draft
- Half-PPR scoring
- 15 rounds
- Draft slot 6

using FantasyPros Draft Wizard.

The Draft Goblin completed the full draft, recovered successfully from an already-drafted recommendation, and produced an **84/100 FantasyPros Draft Score**.

## Files

- `PROMPT.md` — exact contest submission prompt
- `LICENSE` — MIT License

## License

MIT

The Draft Goblin has been informed that open-source licensing does not constitute compensation.
