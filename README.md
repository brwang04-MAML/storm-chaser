# 🌪️ Storm Chaser — Math Check

A free, play-based math diagnostic for children aged roughly 3 to 5, mapped to the
**California Preschool/Transitional Kindergarten Learning Foundations (PTKLF)**, Mathematics domain.

Runs in any browser. Designed for iPad. No install, no account, no data leaves the device.

**▶️ [Play it here](https://brwang04-MAML.github.io/storm-chaser/)**

---

## What it measures

Fifteen foundations across four ~5-minute "stops":

| Stop | Foundations |
|---|---|
| 🚚 Load the Storm Truck | 1.1 reciting numbers · 1.2 one-to-one correspondence · 1.3 cardinality · 1.4 subitizing · 1.5 numeral recognition |
| 🛣️ Which Road? | 1.6 comparing groups · 2.1 adding & subtracting · 2.2 composing · 2.3 solving problems |
| 🔧 Sort the Garage | 2.5 sorting & classifying · 2.6 patterns |
| 🌪️ Storm Road Signs | 4.1 2-D shapes · 4.2 3-D shapes · 4.5 position words · 4.6 mental rotation |

Each foundation is reported at one of three levels: **Not yet**, **Early** (typical 3–4½),
or **Later** (typical 4–5½ — i.e. where a child is heading by TK entry).

## Design principles

These come from the foundations themselves, not from game convention:

- **No right/wrong feedback.** Every answer gets the same warm response. Corrective
  feedback during a diagnostic teaches the answer and invalidates the measurement.
  It also has to feel like a game the child cannot lose.
- **One instruction at a time.** Working memory at this age holds one to two pieces of
  information (Foundation 2.1, Approaches to Learning). Multi-step instructions measure
  memory, not math.
- **Nothing is timed** except the subitizing flash, which must be timed to be valid.
- **The adult is part of the design.** The foundations say "with adult support" repeatedly
  in the Early band. Items that cannot be scored by a tap — most importantly cardinality —
  ask the grown-up to record what they observed.

## The cardinality item

The most diagnostic moment in the whole thing. After the child counts the cars onto
the truck, the app asks "how many?" and the adult records whether the child **answered
from the count he just did** or **started counting all over again**.

A child who re-counts has one-to-one correspondence but not yet cardinality — to him,
counting *is* the answer, rather than producing one. This is invisible on a worksheet and
invisible to auto-scoring, and it is the highest-leverage thing to know about a
pre-K child's number sense.

## For educators

The item bank is a plain JavaScript object near the top of the `<script>` block in
`index.html`. Each item declares the foundation it targets (`f`) and the band it probes
(`band`). Items can be edited, reordered or removed without touching the engine.

Results stay in memory only — nothing is stored or transmitted. Use the **Copy results**
button before closing the tab.

## Not covered

This checks the Mathematics domain only. It does **not** assess the social-emotional and
self-regulation foundations, which carry the most weight in a California TK classroom and
cannot be meaningfully measured on a tablet.

## Licence

MIT — use it, fork it, adapt it for your own students.
