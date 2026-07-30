# 🌪️ Storm Chaser — Math Check

**v2** · A free, play-based mathematics check for children aged roughly 3 to 5, mapped to
the **California Preschool/Transitional Kindergarten Learning Foundations (PTKLF)**.

Runs in any browser. Built for iPad, works on a laptop. No install, no account, nothing
stored, nothing transmitted.

**▶️ [Play it here](https://brwang04-maml.github.io/storm-chaser/)**

---

## What it measures

Sixteen foundations across four stops of about five minutes each.

| Stop | Covers |
|---|---|
| 🚚 Load the Storm Truck | reciting numbers · one-to-one correspondence · cardinality · subitizing · numeral recognition |
| 🛣️ Which Road? | comparing groups · adding and taking away · composing numbers · solving problems |
| 🔧 Sort the Garage | sorting and classifying · patterns |
| 🌪️ Storm Road Signs | 2-D shapes · shape names · solid shape names · position words · mental rotation |

Results are reported in four groups — **Number sense**, **Patterns & sorting**,
**Spatial thinking**, and **Math language** — at one of three levels: *Not yet*,
*Early* (typical 3–4½), or *Later* (typical 4–5½, i.e. TK entry).

## Design principles

These come from the foundations themselves and from playtesting, not from game convention.

**No right or wrong feedback, ever.** Every answer gets the same warm response.
Corrective feedback during a diagnostic teaches the answer and invalidates the
measurement. It also has to feel like a game the child cannot lose.

**One instruction at a time.** Working memory at this age holds one to two pieces of
information. Multi-step instructions measure memory, not mathematics.

**Nothing explanatory on the play screen.** The adult is supervising a small child and
cannot read a paragraph mid-item. Rationale lives in the report, where it aids
interpretation instead of competing with it.

**Everything randomised.** Fixed quantities make a diagnostic single-use — the child
answers the second run from memory. Every number, colour, shape and rotation is generated
fresh, so progress can actually be measured over time.

**No fine motor demand on the child.** Where precision would be the limiting factor, the
adult records the observation. Otherwise the item measures mouse control.

**Nothing fades to mean "gone."** Reduced opacity does not read as absence to a
three-year-old. Objects visibly leave.

**Quantities are answered with quantities.** Answering "how many" with a written numeral
silently requires numeral recognition — a different foundation, measured separately.

## Three items worth understanding

### Cardinality

The most diagnostic moment in the check. After the child counts, the app asks "how many?"
and the **adult** records whether he answered from the count he just made or started
counting all over again.

A child who re-counts has one-to-one correspondence but not yet cardinality — to him,
counting *is* the answer rather than producing one. This is invisible on a worksheet and
cannot be auto-scored.

### "Fewer"

Asked twice on the same picture: once with *fewer*, once with *more*.

Donaldson and Balfour (1968) tested fifteen children between three-and-a-half and four
years old. Only one answered "less" correctly every time. Townsend (1974) named the
measurement problem that follows: a single question cannot separate a child who reads
"fewer" as "more" from one who has no meaning for the word at all.

Two questions on one picture distinguish four outcomes — and only one of them, missing
both, is a mathematics finding. The others are reported as **vocabulary, not maths**.

### Shapes, split in two

Naming a shape is vocabulary. The mathematics is recognising a rotated square as still a
square. So the geometry item is silent and non-verbal, and shape naming is reported
separately under Math language. A child with no shape words can still score at the later
band on geometry.

## For educators

The item bank is a plain JavaScript object near the top of the `<script>` block in
`index.html`. Each item declares the foundation it targets (`f`), the band it probes
(`band`), the child-facing question (`say`), the adult's one-line cue (`hint`), and a
`build()` function that generates fresh randomised content each run. Items can be edited,
reordered or removed without touching the engine.

All report copy — what each foundation measures, why it is included, what each band
means, and what to try next — lives in the `F` object and can be rewritten for your own
setting.

Results stay in memory only. Use **Copy** before closing the tab.

## Not covered

Mathematics only. This does **not** assess the social-emotional and self-regulation
foundations, which carry the most weight in a California TK classroom and cannot be
meaningfully measured on a tablet.

## References

Donaldson, M. & Balfour, G. (1968). Less is more: a study of language comprehension in
children. *British Journal of Psychology*, 59(4).
Townsend, D. (1974). Children's comprehension of comparative forms.
California Department of Education (2024). *Preschool/Transitional Kindergarten Learning
Foundations.*

## Licence

MIT — use it, fork it, adapt it for your own students.
