# Testing

How the rules were tested, and what the results do and do not show.

---

## Phase 5 (v1 rules, July 2026)

Method: the owner gave the AI real photos from the account. The AI classified them. The owner corrected mistakes, and each correction became a rule. Then the same photos were classified again.

| Round | Photos | First-pass accuracy | After rule fixes | Main lesson |
|---|---|---|---|---|
| 1 | 10 | 80% | 100% | Visual dominance beats guessed intent. Animals come first. |
| 2 | 12 | 75% | 100% | Dominant clouds override lighting. |
| 3 | 15 | 87% | 100% | Religious buildings are architecture. People can be compositional elements. |
| 4 | 7 | 86% | 100% | Subject overrides context. Flowers and fruits are separate. |
| **Total** | **44** | **≈ 82%** (36 of 44) | **100%** | |

Totals are calculated from the round figures above. The per-photo logs from these rounds are not in this repository.

### What these numbers mean

- **First-pass accuracy** (≈ 82%) is the best measure of how well the rules worked on photos they had not seen.
- **After rule fixes** (100%) shows the final rules agree with the owner on the 44 photos used to write them. It is not a measure of accuracy on new photos.

---

## v2.0 test (30 Oct 2026)

Method: 30 pins were taken from the unorganized pins on the main board. The AI classified each one using only the v2.0 rule files, with no corrections. The owner then marked each result right or wrong. The owner confirmed 11 results as correct and placed every other pin in Randoms. One of those (#28) was already classified as Randoms by the AI, so it also counts as a match.

### Result

**First-pass accuracy: 12 of 30 (40%).**

### Limits of this test

- **Not fully cold.** Earlier in the same session, the AI had looked at all of the unorganized pins to suggest where they should go. Treat this as an internal check, not a measure of accuracy on brand-new photos.
- **Uneven mix.** The unorganized pins had no cats, only 2 dogs and a few flowers, so the planned 3-per-category mix was not possible.
- **Answer key vs rules.** Some of the 18 misses are pins that the v2.0 rules send to a board on purpose, such as dogs (#1, #22), idols (#20, #21) and food (#23). The owner's key sent them to Randoms instead. This gap between the written rules and how the owner curates boards is the main finding to resolve before the next test.

### Log

| # | Photo (short description) | AI destination (v2.0) | Owner's destination | Match? |
|---|---|---|---|---|
| 1 | Man sitting with a dog in a park | Street Dog Photography | Randoms | No |
| 2 | Truck on a tree-lined road | Street & Architecture | Randoms | No |
| 3 | Flower decorations by a doorway | Flower Photography | Flower Photography | Yes |
| 4 | Flower rangoli | Flower Photography | Flower Photography | Yes |
| 5 | Blue sky with wispy clouds | Sky, Cloud & Sunset | Sky, Cloud & Sunset | Yes |
| 6 | Grass amphitheatre under big clouds | Sky, Cloud & Sunset | Sky, Cloud & Sunset | Yes |
| 7 | "SKY" graffiti close-up | Street & Architecture | Randoms | No |
| 8 | Street shop with a dog asleep in front | Street & Architecture | Street & Architecture | Yes |
| 9 | STILLWOOD bare branches | Nature Photography | Nature Photography | Yes |
| 10 | Swimming pool with people | Nature Photography | Randoms | No |
| 11 | Jeep on a road | Street & Architecture | Street & Architecture | Yes |
| 12 | Ganesh idol | Idols and Statues | Idols and Statues | Yes |
| 13 | Carved stone archway | Street & Architecture | Street & Architecture | Yes |
| 14 | "Love like this" graffiti | Street & Architecture | Randoms | No |
| 15 | Wide view of trees, a field and a building | Nature Photography | Nature Photography | Yes |
| 16 | Large tree beside a road | Nature Photography | Nature Photography | Yes |
| 17 | Car on a road at dusk | Street & Architecture | Randoms | No |
| 18 | Temple with steps | Street & Architecture | Randoms | No |
| 19 | Raw mangoes in a bowl on leaves | अन्न | Randoms | No |
| 20 | Temple hall with a large Ganesh idol | Idols and Statues | Randoms | No |
| 21 | Clay fort figurine | Idols and Statues | Randoms | No |
| 22 | Puppy on grass | Street Dog Photography | Randoms | No |
| 23 | Bowls of vegetables | अन्न | Randoms | No |
| 24 | Snack packets in a hand | अन्न | Randoms | No |
| 25 | Smartwatch screen | random | Randoms | No |
| 26 | Man taking a photo with his phone | random | Randoms | No |
| 27 | Bullock cart with hay on a road | creatures (sweet ones) | Randoms | No |
| 28 | Bonfire | Randoms | Randoms | Yes |
| 29 | Pebbles with a ring | Nature Photography | Randoms | No |
| 30 | Road sign beside a road | Street & Architecture | Randoms | No |

---

## Next test (v2.1)

1. Pick 30 photos not used in any earlier test, ideally new uploads. Include at least 3 each of dogs, cats, vehicles, night, sky, flowers, textures and nature.
2. Before classifying, write down one line on what makes a pin "board-worthy" versus Randoms, so the answer key and the rules use the same standard.
3. Classify with the v2.1 rules, without corrections, and log results in the table format above.
4. Report first-pass accuracy, then note any rule fixes in `CHANGELOG.md`.
