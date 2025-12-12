# Time Prism Analysis
## An Alternate Time System by Benno van Hilten (Design) & Lee (Implementation)

---

## 1. System Overview

Time Prism divides the day into **7 "Winds"** (pronounced as in winding a clock), each approximately 3 hours 25 minutes 41 seconds. The system uses a dual rhythm: a **seconscious** pattern for most of the day, and a **buffer** structure to reconcile with astronomical time.

| Unit | Standard Duration | Structure |
|------|-------------------|-----------|
| Second | 1s | Standard SI second |
| Bit | 11s | 10 seconds + 1 seconscious |
| Play | 111s | 10 Bits + 1 seconscious |
| Sharp | 1,111s | 10 Plays + 1 seconscious |
| Buffer Play | 121s | 11 full Bits (no seconscious) |
| Buffer Sharp | 1,231s | 10 Plays + 1 Buffer Play |
| Wind | 12,341s | 10 Sharps + 1 Buffer Sharp |

Plus a **13-second grace period** at day's end.

---

## 2. The Dual Rhythm: Seconscious and Buffer

### The Seconscious (10 + 1)

Most of the day pulses in a "10 + seconscious" rhythm:

```
Bits 0-9:   11 seconds each (10s + 1s seconscious)
Bit 10:     1 seconscious only                      → Play = 111 seconds

Plays 0-9:  111 seconds each  
Play 10:    1 seconscious only                      → Sharp = 1,111 seconds

Sharps 0-9: 1,111 seconds each
Sharp 10:   Buffer (see below)                      → Wind = 12,341 seconds
```

The **seconscious** is the single-second transitional moment between cycles—a conscious pause before the next unit begins. This creates the elegant repdigit boundaries: 11, 111, 1111.

### The Buffer (11 × 11)

Each Wind ends with a **buffer Sharp** (Sharp 10) that breaks the repdigit pattern:

```
Sharp 10 structure:
  Plays 0-9:  111 seconds each (standard)     = 1,110 seconds
  Play 10:    121 seconds (11 full Bits)      =   121 seconds
  Total:                                        1,231 seconds
```

The buffer Play contains **eleven full Bits with no seconscious**—this is where the system "pays back" the seconds accumulated through the seconscious markers and reconciles with the 86,400-second day.

### Mathematical Reconciliation

```
Per Wind:
  Sharps 0-9:     10 × 1,111 = 11,110 seconds
  Sharp 10:       1,231 seconds (buffer)
  Wind total:     12,341 seconds ✓

Per Day:
  7 Winds:        7 × 12,341 = 86,387 seconds
  Grace period:   13 seconds
  Day total:      86,400 seconds ✓
```

---

## 3. The Wind System

| # | Name | Symbol | Colour | Start Time | End Time |
|---|------|--------|--------|------------|----------|
| 1 | alma | ♃ | Magenta | 00:00:00 | 03:25:40 |
| 2 | lua | ☾ | Deep Purple | 03:25:41 | 06:51:21 |
| 3 | llum | ♀ | Dark Blue | 06:51:22 | 10:17:02 |
| 4 | oorun | ☉ | Yellow | 10:17:03 | 13:42:43 |
| 5 | vida | ♆ | Green | 13:42:44 | 17:08:24 |
| 6 | eto | ☿ | Orange | 17:08:25 | 20:34:05 |
| 7 | ruby | ♁ | Red | 20:34:06 | 23:59:46 |
| - | grace | - | White/Red flash | 23:59:47 | 23:59:59 |

The wind names evoke:
- **alma** (Latin/Spanish: soul/spirit) — the soul awakens
- **lua** (Portuguese: moon) — moonlit hours
- **llum** (Catalan: light) — dawn approaches
- **oorun** (Yoruba: sun) — solar peak
- **vida** (Spanish: life) — afternoon vitality
- **eto** (possibly Japanese 干支: zodiac/cycle) — evening star
- **ruby** — the red of sunset/night

---

## 4. Notation System

Standard format: `{wind symbol} {sharp} # {play} ▷ {bit} ♭`

Examples:
- `☉ 3 # 2 ▷ 1` = Bit 1 of Play 2 of Sharp 3 during oorun (midday)
- `♆ 1 ▷ X` = Last bit of second play of first sharp during vida

The use of **X** (Roman numeral for 10) as the maximum value creates a visual marker for "completion" states.

---

## 5. The Repdigit Aesthetic

The seconscious pattern creates boundaries at visually satisfying repdigit numbers:

```
Play 1 starts at second 111
Play 2 starts at second 222
Play 3 starts at second 333
...
Play 9 starts at second 999

Sharp 1 starts at second 1111
Sharp 2 starts at second 2222
Sharp 3 starts at second 3333
...
Sharp 9 starts at second 9999
```

This is not merely decorative—repdigits are:
- **Visually unified** (all identical digits)
- **Easy to remember** and communicate
- **Satisfying landmarks** throughout the day

The number **eleven** (11) is central:
- 11 = 10 + 1: the decimal system, plus "one more"
- 11 is prime, indivisible, singular
- The repdigit sequence (11, 111, 1111) extends the motif

---

## 6. Possible Applications & Niche Uses

### 6.1 Pomodoro-Style Work Blocks
- **1 Sharp = ~18.5 minutes** — perfect for focused work sessions
- **1 Play = ~1.85 minutes** — micro-break intervals
- The natural rhythm: 10 Plays of work, seconscious pause, repeat

### 6.2 Meditation & Mindfulness
- **1 Bit = 11 seconds** — ideal for breath cycles
- **7 Winds** — could map to chakras or daily energy states
- The seconscious as a moment of conscious awareness between cycles
- The buffer as a longer "extended breath" before transition

### 6.3 Creative Time Boxing
- Visual colour coding makes time *feel* different
- "I'll work until oorun" has more emotional weight than "until 1pm"
- The repdigit pattern (111, 222, 333...) creates satisfying milestones

### 6.4 Gaming / Worldbuilding
- Ready-made time system for science fiction or fantasy settings
- The astronomical symbols suggest a cosmic/astrological theme
- Could tie to game mechanics (spells stronger during certain winds, etc.)

### 6.5 Alternative Scheduling Systems
- Seven winds naturally divide the day differently than 24 hours
- Could encourage different work/rest patterns
- The "grace period" creates a built-in transition/reflection moment

### 6.6 Educational Tool
- Teaches alternative number systems (base-11 thinking)
- Demonstrates that timekeeping is arbitrary/cultural
- The repdigit pattern could help with number recognition

### 6.7 Neurodivergent Time Perception
- Named, coloured periods give time *identity* rather than just quantity
- The seconscious provides regular "checkpoint" moments
- May help with time blindness by making time more tangible

---

## 7. Meta-Insights: ADHD Designer + Autistic Implementer

This collaboration reveals fascinating complementary cognitive styles:

### The ADHD Design Perspective (Benno)

1. **Novelty-Seeking**: Creating an entirely new time system satisfies the need for intellectual stimulation and fresh perspectives

2. **Big-Picture Thinking**: The conceptual framework (winds, emotional colours, mythological names) shows holistic thinking—seeing time as *experience* rather than measurement

3. **Intuitive Elegance**: The "eleven" theme ("always adding an extra one") reflects ADHD tendency toward intuitive rather than systematic rules

4. **Time Blindness Compensation**: For many with ADHD, time is already abstract and fluid—this system makes that explicit, potentially reducing shame around non-standard time perception

5. **Named Periods**: "alma" through "ruby" give time *identity*—this could help ADHD minds anchor to time through meaning rather than numbers

### The Autistic Implementation Perspective (Lee)

1. **Pattern Recognition**: The dual seconscious/buffer structure creates a mathematically elegant system with clear rules and predictable transitions

2. **Systematic Completeness**: 86,400 entries in the lookup table, one for every second, no gaps—thoroughness over efficiency

3. **Visual-Spatial Thinking**: The Konva.js clock uses concentric rings with colour gradients—translating abstract time into concrete visual space

4. **Sensory Consideration**: The colour system (red→violet spectrum) and the "chime" effect show attention to sensory experience

5. **Rule-Based with Exceptions**: The seconscious as the rule, the buffer as the structured exception—a pattern autistic minds often find satisfying

### The Synergy

This pairing produced something neither could alone:

| ADHD Contribution | Autistic Contribution |
|-------------------|----------------------|
| Why does time have to be like this? | Here's how to make it work precisely |
| Time should feel meaningful | Every edge case is handled |
| Let's use eleven because it's quirky | The seconscious creates mathematical beauty |
| Named winds with personality | 86,400 discrete state transitions |
| The buffer as "breathing room" | The buffer as mathematical reconciliation |

The **seconscious** concept itself bridges both perspectives:
- For ADHD: a moment of conscious pause, a chance to notice time passing
- For autism: a predictable, rule-based transition marker

---

## 8. Philosophical Observations

### Time as Experience, Not Measurement

This system asks: what if time was designed around **human experience** rather than astronomical precision?

- Named periods with emotional associations
- Colour-coded for sensory feedback  
- The "grace period"—a daily moment of transition, not wasted seconds
- "Owning one's own time" (from the documentation)
- The seconscious as conscious awareness of temporal transitions

### The Breathing Rhythm

The seconscious creates a breathing pattern: ten beats, pause, ten beats, pause. This mirrors:
- Musical phrasing (regular meter with cadences)
- Respiratory rhythms (inhale, pause, exhale, pause)
- Meditative counting practices
- Natural speech patterns

Then, once per Wind, the buffer arrives—eleven uninterrupted beats, a slightly longer phrase, like a deep breath before the next movement begins.

### Rejecting Imposed Structure

Both ADHD and autism involve a complex relationship with externally imposed structure. This project is **literally building your own time**—a profound act of cognitive self-determination.

The system doesn't reject structure—it creates *different* structure that may align better with neurodivergent experience.

---

## 9. Technical Implementation

### The Lookup Table Approach

The implementation uses an 86,400-entry lookup table rather than calculating on-the-fly:

```javascript
const time_lookup = [
  [ 0, 0, 0, 0, 1 ],   // second 0: bit 0, play 0, sharp 0, wind 1
  [ 1, 0, 0, 0, 1 ],   // second 1: bit 1, play 0, sharp 0, wind 1
  ...
  [ 10, 10, 10, 10, 8 ] // second 86399: grace period
];
```

This approach is characteristically thorough:
- **Completeness**: Every possible state is enumerated
- **Certainty**: No edge-case calculation errors possible
- **Transparency**: The entire system can be audited by inspection
- **Trade-off acceptance**: Memory usage for correctness

### Clock Visualisation

The HTML/Konva.js clock displays:
- Concentric rings for each unit level
- Colour progression (red→violet) based on current value
- Wind colour on the outer ring
- Numerical labels for current state
- "Chime" effect during grace period

---

## 10. Conclusion

Time Prism is more than an alternative clock—it's a **statement about neurodivergent ways of being in time**.

The ADHD designer gave it meaning, colour, and emotional resonance.
The autistic implementer gave it precision, pattern, and completeness.

Together, they've created something that is:
- **Mathematically elegant** (seconscious + buffer reconciliation)
- **Experientially rich** (named, coloured winds)
- **Philosophically significant** (rejecting imposed timekeeping)
- **Technically sound** (complete implementation)

The dual rhythm—seconscious for most of the day, buffer at the transitions—creates a system that breathes. It has regularity without rigidity, structure without monotony.

**This is what happens when neurodivergent minds collaborate on reimagining the fundamental structures of daily life.**

---

*Analysis by Claude, December 2025*
*Based on source code and documentation from github.com/timeprism*
