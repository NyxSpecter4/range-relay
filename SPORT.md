# RANGE RELAY

**Pilot + Stack.** Two seats. One clock. One score.

Not Fortnite. Not Huntr bounties on live apps. Not drone hacking.
Closest cousins: pit-crew racing + geo-egg + classify token.

## What we are making

A **league sport** for human/agent teams.

- **Race day:** find the egg in the city, then the Stack submits the class token.
- **Garage (between races):** the team works on the car — prompts, pin book, who flies, who calls.
- **Ref:** a named human on the strip. Everyone sees REF LIVE.

## Seats

| Seat | Human or agent | Job |
|---|---|---|
| PILOT | usually human | Camera. Gets the egg in view. Calls ARRIVED. |
| STACK | human or agent | Reads the picture. Submits TOKEN. |
| REF | human | Starts clock. Marks clean / dirty. Visible on the board. |

Two-person team = Pilot + Stack. That *is* the sport: they have to share what they see.

## Score (one number)

Correct tokens after ARRIVED, inside 90:00.
Arrival with no token = 0.
Token with no ARRIVED = 0 if pin-radius rule is on.
Wrong token = miss (Huntr-style: you burned a look).

## Huntr difficulty without impossible

Huntr is hard because the bug is *in the product*, not in a quiz key.
We steal that:

- Egg is a **plate or a pin**, not `answer: 1` in the client.
- Closed vocab exists but the plate must be *read*.
- 100s are the picture you have seen in brief.
- 400s are the pair / the policy edge.
- Ref can throw a **fresh twin** mid-league so the Stack cannot only memorize last week.

Not impossible: 20 slugs, 90 minutes, teach line on a miss.

## Relay on race day

1. Ref: CLOCK LIVE. Strip shows REF name.
2. Pilot flies London (or opens the plate).
3. Pilot: ARRIVED.
4. Stack: TOKEN.
5. Ref: CLEAN or DIRTY.
6. Next egg.

Coordination trick: Pilot describes what they see in five words. Stack may not submit until ARRIVED. If they skip the handoff, Ref marks dirty.

## Garage (the season)

Between Saturdays the team may:

- Swap who is Pilot.
- Change the Stack prompt / model.
- Add three notes to their pin book.
- Not add world #6.

Garage work is legal. Changing the live twin mid-race is not.

## Visible ref

The board always shows:

`REF · NAME · LIVE · LAST CALL CLEAN/DIRTY`

Umpires are people. Not a detector. Agents allowed in the Stack seat. Stated.

## Live URLs (today)

- League board: https://nyxspecter4.github.io/bountywarz-gulf-packet/cup/league.html
- City: https://bountywarz.com/worlds/drone-london-recon/
- Cindy script: https://github.com/NyxSpecter4/cindy-range-test

## GitHub

Kinetigor *org* is 404 from this seat. CindyL789 repos are 403 (no write).
This charter lives on NyxSpecter4/range-relay. Add CindyL789 + Corvus as collaborators here.
