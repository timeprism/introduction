# Introduction

An alternative time system by [Benno van Hilten](https://onespac.es)

## Basics

The day is split into seven 'winds' (pronounced as in winding a clock).

Seconds are the smallest units, and are the same duration as conventional seconds. The next largest unit is a Bit, then a Play, then a Sharp, and finally a Wind.

## Standard Units

Most of the day follows a **repdigit pattern** using a "10 + seconscious" structure:

- **Bit** is ten seconds plus one **seconscious** (a transitional marker second) = **11 seconds**

- **Play** is ten Bits plus one seconscious = **111 seconds** (~1 min 51 sec)

- **Sharp** is ten Plays plus one seconscious = **1,111 seconds** (~18 min 31 sec)

The seconscious is the single-second pause between units—a moment of conscious transition before the next cycle begins.

## The Buffer

Each Wind ends with a **buffer Sharp** (Sharp 10) that reconciles the repdigit structure with the day's length:

- **Sharp 10** contains ten standard Plays (1,110 seconds) plus one **buffer Play**

- The **buffer Play** (Play 10 of Sharp 10) breaks the repdigit pattern: it contains eleven full Bits with no seconscious = **121 seconds**

- This gives Sharp 10 a total of **1,231 seconds** (1,110 + 121)

The buffer is where the system "pays back" the seconds saved by using seconscious markers throughout the day.

## Wind Structure

- **Wind** is ten standard Sharps (11,110 seconds) plus one buffer Sharp (1,231 seconds) = **12,341 seconds** (~3 hrs 25 min 41 sec)

- Seven Winds account for 86,387 seconds, with 13 seconds of **grace** at day's end

## Summary Table

| Unit | Standard Duration | Structure |
|------|-------------------|-----------|
| Bit | 11 seconds | 10 seconds + 1 seconscious |
| Play | 111 seconds | 10 Bits + 1 seconscious |
| Sharp | 1,111 seconds | 10 Plays + 1 seconscious |
| Buffer Play | 121 seconds | 11 full Bits (no seconscious) |
| Buffer Sharp | 1,231 seconds | 10 Plays + 1 Buffer Play |
| Wind | 12,341 seconds | 10 Sharps + 1 Buffer Sharp |
| Day | 86,400 seconds | 7 Winds + 13 seconds grace |

## The Rhythm

The seconscious creates a breathing rhythm: ten beats, pause, ten beats, pause. Most of the day pulses in this pattern. Then, once per Wind, the buffer arrives—eleven uninterrupted beats, a slightly longer phrase before the next Wind begins.

This mirrors natural rhythms: regular meter with occasional extended phrases, like a musical cadence or a deep breath before continuing.

## Winds

The winds each have a name, symbol and color, in sequence these are:
- alma ♃ (magenta)
- lua ☾ (deep purple)
- llum ♀ (dark blue)
- oorun ☉ (yellow)
- vida ♆ (green)
- eto ☿ (orange)
- ruby ♁ (red)

![seven winds](https://raw.githubusercontent.com/timeprism/introduction/main/wind%20times.png)

## Colors

The other units follow a spectrum from red to violet.

'1' is red and ten, written 'X' as in the Roman numeral, is violet.

![units](https://raw.githubusercontent.com/timeprism/introduction/main/unit%20colors.png)

## Notation

A shorthand for writing the time (to the nearest bit) is:

``{wind symbol} {sharp} # {play} ▷ {bit} ♭``

Typically the last ``♭`` symbol is omitted.

So bit 1 of play 2 of sharp 3 of eto is written:

``☉ 3 # 2 ▷ 1``

The first unit in a sequence is zero, which can be omitted.

So the last bit of the second play of the first sharp of vida is written:

``♆ 1 ▷ X``

## Name

Various names have been suggested for this time system. 'Ones' is one of these. It is associated with the occurence of the number eleven, always adding an extra one at the end of a sequence, and the idea of "owning one's own time".

## Demo

A demo of one particular clock running to this time system is online at [timeprism.github.io](https://timeprism.github.io). This was written with Javascript and [Konva](https://konvajs.org/index.html).

## Gallery

There are [Screenshots](https://github.com/timeprism/introduction/tree/main/gallery) of various software prototypes using this time system. These were composed in [Pythonista](http://omz-software.com/pythonista/).
