# Pinterest-AI

A rule set that lets an AI model sort my photos into the right Pinterest board and write search-friendly pin text for them.

**Account:** [rogers.g17 | Mobile Photography](https://in.pinterest.com/rogersg17/) — 1,800+ original mobile photos, peak of 1.2M+ monthly viewers
**Current version:** v2.1 (30 Oct 2026)

---

## The problem

I upload photos often, and they cover many subjects: street dogs, cats, clouds, flowers, buildings, food. Sorting each one by hand was slow and inconsistent. The same kind of photo ended up in different places, and pins went up without titles or descriptions. Pinterest uses board names and pin text to decide who sees a pin, so both problems cost reach.

## The approach

1. **Fixed destinations.** `BOARD.md` lists every board and section a photo can go to. The AI is not allowed to invent new ones.
2. **One decision order.** `CLASSIFICATION_RULES.md` asks up to 16 questions in a fixed order, starting with "Is the subject an animal?". The first "yes" decides the destination.
3. **Subject over context.** The thing being photographed decides where it goes, not the place it is in. A dog on a beach is a dog photo.
4. **Rules from real mistakes.** Each rule was added after the AI got a real photo wrong. `CONFUSION_PREVENTION.md` keeps those traps in one table.
5. **Metadata in the same pass.** `WORKFLOW_PROMPT.md` also has the AI write a keyword-led title, description, keywords and alt text for each photo.

## Results so far

- **Phase 5 (v1 rules):** 44 real photos over four rounds. About 82% were right on the first pass. After each round's corrections became rules, all 44 matched. See `TESTING.md` for what these numbers do and do not show.
- **v2.0:** In October 2026 I rebuilt the account from one catch-all board into keyword boards. A 30-pin check of the v2.0 rules scored 12 of 30 (40%) on the first pass. Several misses were pins the rules sent to a board but I placed in the catch-all section, so the next step is a clearer line between "board-worthy" and "random".
- **v2.1:** Added boards for vehicles, night shots and textures, plus water and symmetry sections, and updated the rules to match. The next test is planned in `TESTING.md`.

## How to use it

1. Open any AI chat that accepts files and images.
2. Upload `BOARD.md`, `CLASSIFICATION_RULES.md`, `CONFUSION_PREVENTION.md` and `WORKFLOW_PROMPT.md`.
3. Paste the prompt from `WORKFLOW_PROMPT.md`, then upload your photos.
4. For each photo you get a destination, decision step, title, description, keywords, alt text and a confidence level.
5. Check every Medium or Low confidence result yourself before pinning.

To adapt it to your own account, replace the destinations in `BOARD.md` and edit the rules that mention them.

## Files

| File | Purpose |
|---|---|
| `BOARD.md` | Allowed destinations, published board descriptions, old-to-new map |
| `CLASSIFICATION_RULES.md` | The decision order and rules |
| `CONFUSION_PREVENTION.md` | Known mistakes and the rule that prevents each one |
| `WORKFLOW_PROMPT.md` | The prompt and output format |
| `TESTING.md` | Test method, results and the next test |
| `STANDARDS.md` | How this repository is maintained |
| `CHANGELOG.md` | Version history |

## Limits

- This is a prompt-and-rules system. It is not an app and does not post to Pinterest. Moving pins is still done by hand.
- Results depend on the AI model used. The tests so far used one model.
- People portraits have no dedicated board yet. They go to the Randoms section.

## Author

Rushabh Ghule — [rushabhghule.github.io](https://rushabhghule.github.io)
