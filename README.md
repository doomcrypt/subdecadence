# SUBDECADENCE :: Lemurian Time-Sorcery

> *"Governed by the great lemur Tokhatto."*

A single-file browser card game rooted in occult numerology and Lemurian demonology. Play against a 40-card deck, pair cards that sum to 9, and discover which demon your final score summons.

## Play

Open `Subdecadence.html` in any modern web browser. No installation, no dependencies, no server required.

## How to Play

### The Deck

40 cards: 4 suits (♠ ♥ ♦ ♣) × 10 values (0–9). Each card is secretly bound to a Lemurian demon — hover over any revealed card to see its entity name and Mesh coordinates.

### Each Round

Rounds proceed through four phases:

1. **DEAL** — Five cards are placed in a cross formation (Center · West · East · North · South). These are your targets.
2. **DRAW** — You draw five cards from the deck into your hand.
3. **PAIR** — Match hand cards to cross cards. A pairing is only valid if the two values **sum to exactly 9** (e.g. 1+8, 3+6, 4+5, 0+9). Click a hand card, then a cross card to attempt a pair. Use **AUTO-PAIR** to let the engine greedily find all valid pairings.
4. **RESOLVE** — Scoring is calculated and the round ends.

### Scoring

| Outcome | Points |
|---|---|
| Valid pair | **+difference** between the two card values |
| Unpaired cross card | **−its face value** |

Examples:
- Pairing 1 + 8 → **+7**
- Pairing 4 + 5 → **+1**
- Leaving a 9 unpaired → **−9**
- Leaving a 0 unpaired → **−0** (no penalty)

### Winning & Losing

- **Positive round score** → the aeon continues; deal another cross.
- **Zero or negative round score** → the aeon closes; game over.
- **Deck exhausted** (fewer than 10 cards remain) → the aeon closes; game over.

Your cumulative **Angelic Index** tracks all positive scores across the game — a measure of the light generated before the fall.

## The Demons

Your final negative round score (or 0) maps to one of **45 Lemurian entities** from the Numogram — a fictional occult system. The result screen reveals:

- **Name** and demonic type
- **Occult attributes**
- **Mesh number** and **Net-span** coordinates
- **Associated card** from the deck

A score of 0 summons **Lurgo**, the mildest entity. The deeper the negative score (down to −44), the more severe the demon called. Score −44 and you face **Ummnu (Om, Amen, Omen)** — Amphidemon of Earth-Screams.

## Strategy

- **Prioritize high-value cross cards.** A 9 or 8 left unpaired is a heavy penalty. Find their complements (0 or 1) in your hand first.
- **Chase the big differences.** A 0+9 pairing scores +9 — the maximum yield from a single pair. A 4+5 scores only +1.
- **AUTO-PAIR is greedy, not optimal.** It finds the first valid pair it can, which may not maximize your score. Manual pairing can outperform it when multiple valid pairings compete for the same cards.
- **Watch the deck count.** The game ends if fewer than 10 cards remain — plan your rounds accordingly.

## Technical Notes

- Pure HTML/CSS/JavaScript — no frameworks, no build step.
- Audio generated procedurally via the Web Audio API.
- Fonts loaded from Google Fonts (requires an internet connection for full styling; the game is otherwise fully offline).
- All game state is held in memory; refreshing the page resets everything.

## Credits

Demonology, Numogram lore, and card mechanics derived from the Lemurian mythos associated with the CCRU (Cybernetic Culture Research Unit).
