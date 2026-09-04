# Fantasy Football Draft Assistant 2026

A one-shot fantasy football draft assistant prompt created for the Prompt Teardown Fantasy Football Draft Assistant Prompt Challenge.

The assistant is designed to operate interactively during a snake draft, track selections and roster state, account for positional scarcity and draft gaps, and produce concise pick recommendations using an embedded 2026 player dataset.

## Files

- `PROMPT.md` — exact contest submission prompt
- `LICENSE` — MIT License

## Test

The prompt was successfully run through a complete 12-team, 15-round, Half-PPR FantasyPros mock draft from draft slot 6.

It completed the full draft, recovered successfully from an already-drafted recommendation, and produced an 84/100 FantasyPros Draft Score.

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

Paste the completed prompt as the first message in a fresh chat. During the draft, report each selected player as they are taken. When the assistant recommends a player, draft the first player listed. If that player is already unavailable, reply `already taken`.

## License

MIT
