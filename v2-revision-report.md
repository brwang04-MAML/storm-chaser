# Storm Chaser v2 — Revision Report

**From:** v1 playtest, 29 July 2026 · **Built:** 30 July 2026
Every change below traces to a numbered finding in `v1-playtest-notes.md`.

---

## Four changes that apply everywhere

### 1. Text moved off the play screen → findings A2, A3, A4, A6, B2

v1 printed design rationale on screen while the child was waiting. v2 shows exactly two
things during play: the child's question in large type, and **one short line** for the
adult in a slim purple-edged bar.

Every "why" sentence has been moved into the report, where it can be read at leisure and
actually aids interpretation. Nothing was deleted — it was relocated.

| | v1 on screen | v2 on screen |
|---|---|---|
| Cardinality item | 62 words | 9 words |
| Subitizing item | 47 words | 7 words |
| Numerals item | 58 words | 11 words |

### 2. Every quantity is randomised → findings A5, B3

v1 hard-coded numbers, so a second run tested recall. In v2 each item has a `build()`
function that generates fresh content per run:

- tornado flashes: 2–4 (early band), 5–6 (later band)
- counting set: 6–9 cars, colour randomised
- comparison: pairs like 4v5, 5v6, 6v7, chosen at run time
- addition: random addends, sums capped at 10
- subtraction: 4–6 cars
- part-whole: total 4–6, split at random
- patterns: which object plays A, B and C is shuffled
- shape matching: target and distractors drawn from seven shapes; rotation 30°/45°/135°
- parking slot: vertical or horizontal at random

Verified over 300 simulated runs — every generated item has exactly one correct answer.

### 3. Fine motor demand removed → findings A1, A7, D1, D5

Any item where a 3-year-old's mouse control would have been the limiting factor is now
either a single large choice or adult-recorded. **The child never needs precision.**

### 4. No fading to mean "gone" → finding B4

Reduced opacity is not a cue a 3-year-old reads. Things now visibly leave the screen.

---

## Item-by-item

### Load the truck → **Count the cars** · Foundation 1.2 → finding A1

**Was:** child taps each car to load it; app counts taps.
**Now:** cars sit still. The child counts by pointing, out loud. The adult taps one of
four observations — one number per car / accurate to about five then slipped / skipped
or double-counted / did not count.

*Why:* the tapping was never the skill. One-to-one correspondence is about giving one
number word to one object, and an adult watching a finger sees that far better than a
click handler does. It also removed the "where do I tap?" problem entirely, and the item
now works identically on a laptop and an iPad.

### Cardinality · Foundation 1.3 → finding A2

Prompt is now nine words: *"Ask, then WAIT. Do not hint. Watch what he does."* Three
buttons instead of three sentences. The full explanation of why this item matters more
than any other is now in the report.

### Tornado flash · Foundation 1.4 → findings A4, A5

Rationale removed from screen. Count randomised per run. Answer choices shuffled and
regenerated, so their position carries no information either.

### Read the race numbers · Foundation 1.5 → findings A6, A7

Rationale removed. Numerals now appear in shuffled order each run. Already
adult-operated; the instruction is now one line.

### Which road — "fewer" · Foundation 1.6 → finding B1

**Kept the word, fixed the measurement.** "More, same, less, fewer" is explicitly in the
PTKLF later band, so an aligned instrument has to probe it. The fix is that it now asks
**both** questions on the same picture — "fewer" then "more" — which distinguishes four
outcomes instead of two:

| Response | Reading |
|---|---|
| Both right | Comparison and vocabulary both present → Later |
| Picks the **larger** group for "fewer", gets "more" | Classic less-means-more substitution. Comparison intact → Early, flagged **vocabulary** |
| Blank on "fewer", gets "more" | Comparison intact, word has no meaning yet → Early, flagged **vocabulary** |
| Misses both | Comparison by counting not established → Not yet. **The only maths finding of the four** |

The two middle outcomes are labelled **"VOCABULARY, NOT MATHS"** in the report so they
can never be misfiled as a number-sense deficit.

*Grounding:* Donaldson & Balfour (1968) tested fifteen children aged 3:5–4:1 and found
only one answered "less" consistently correctly. Townsend (1974) identified the
measurement flaw a single question leaves — exactly the flaw v1 had.

### The tornado takes a car · Foundation 2.1 → finding B4

**Was:** one car rendered at 28% opacity.
**Now:** a **🌪️ Go!** button. The tornado slides across, the car spins, shrinks and flies
off the top of the screen, and is then removed from the DOM. The follow-up screen shows
only the cars that remain.

*Why:* a faded car is still a car to a three-year-old. The subtraction was never actually
presented, so the item couldn't have measured Foundation 2.1 no matter what he answered.

### Garage parking · Foundation 2.2 → findings B5, B6

**Was:** three cars visible, a question about five, numeral answers.
**Now:** all cars are shown at once with a counter reading **"5 cars"**, counted aloud
together. A **🏠 Park them!** button drives some into the open garage — they visibly slide
down and away. The closed garage shows "?". Answer options are **pictures of cars**.

*Why (B6):* answering a quantity question with a written numeral silently requires
numeral recognition, which is a different foundation measured separately in 1.5. A child
who understands part-whole perfectly but can't read a "3" would have been marked wrong on
the wrong construct. All arithmetic items now use pictorial answers for the same reason.

### Name the road signs → **split in two** · Foundations 4.1 and vocabulary → finding D2

Your question — *is naming shapes maths or vocabulary?* — was correct, and the item was
wrong. It is now two separate items:

**Find the same shape** (Foundation 4.1, Spatial thinking). Silent and non-verbal. A
target shape is shown; the child picks the match from three. The later-band version
rotates the target 30°, 45° or 135° and resizes it, because the actual geometry is
knowing that a turned square is still a square. **A child with no shape vocabulary can
score at the later band on this.**

**Shape names** (Math language). Adult-recorded naming, reported in a separate group.
A rotated square called "diamond" still counts as not-yet-known for square — that
specific error is the informative one.

### Position words · Foundation 4.5 → finding D3

Kept, but **moved out of number sense into a "Math language" group**, with this in the
report: it is largely vocabulary, but it is the vocabulary maths instruction is delivered
in — *"put the counter above the line"*, *"the number between four and six."* A child who
can't parse it fails tasks he actually understands. Worth knowing; not a counting problem,
and now impossible to read as one.

### Turn the car → **Which car will fit?** · Foundation 4.6 → findings D4, D5, D6

**Was:** press a button to rotate a car 90° at a time, then press "Park it". Scored on
number of turns.
**Now:** a parking slot is shown, vertical or horizontal at random, alongside three cars
at different angles. One tap.

*Why:* the old version measured button-pressing and patience. Choosing without
manipulating is a **better** measure of mental rotation, because turning something until
it fits is precisely the trial-and-error strategy that means the child *isn't* rotating it
mentally.

*Why it's in a maths check at all (D6)* — now stated in the report: mental rotation is one
of the stronger early predictors of later mathematics and STEM achievement.

---

## Report — rebuilt · findings R1, R2

### Re-running now replaces results (R1)

v1 kept the highest band ever achieved and merged notes across runs, so a repeat run
appeared not to update. Starting a section now **clears every foundation that section
covers** before the first item. The map shows a run count when a section has been
replayed. There is also a **Clear all results** button.

### Every foundation now reports five things (R2)

1. **What this measures** — one plain sentence
2. **Why it is in the check** — the design rationale, moved here from the play screen
3. **What he did** — every observation from the run, verbatim
4. **What this means** — interpretation written specifically for the band he reached
5. **Try next** — one concrete activity, also specific to his band

### Grouped so vocabulary can't be misread as maths

| Group | Foundations | Why grouped |
|---|---|---|
| **Number sense** | 1.1–1.6, 2.1, 2.2, 2.3 | Core early mathematics |
| **Patterns & sorting** | 2.5, 2.6 | Structure and rule-based reasoning |
| **Spatial thinking** | 4.1, 4.6 | Measured **without words** |
| **Math language** | shape names, 4.2, 4.5 | Vocabulary. Explicitly labelled *not* a number-sense gap |

That last group is the structural answer to findings D2 and D3: a word gap and a thinking
gap now cannot appear in the same column.

---

## Verification

- JavaScript syntax checked
- All 16 foundations confirmed to have complete report metadata for all three bands
- 300 simulated runs of every item builder — all produce exactly one correct answer, no
  duplicate options, and the subitizing target always appears among the choices

## Not addressed

- **Section C (sorting and patterns)** — no specific problems were raised, so only the
  global text and randomisation changes were applied.
- **Offline use.** Still needs a connection to load.
- **Saving between sessions.** Results are held in memory only; copy them before closing.
  Deliberate for now — no child's data is stored anywhere.
