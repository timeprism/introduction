# Introduction

An alternative time system by [Benno van Hilten](https://onespac.es)

## Basics

The day is split into seven 'winds' (pronounced as in winding a clock).

Seconds are the smallest units, and are the same duration as conventional seconds. The jext largest unit is a nit. Then a play, then a sharp, and finally a wind.

- Bit is ten seconds plus one extra second = 11s
- Play is eleven bits = 121s
- Last Play is a bit plus ten seconds plus one extra second = 22s
- Sharp is nine plays plus one last play = 1,111s
- Last Sharp is ten bits plus ten seconds = 120s
- Wind is eleven sharps plus one Last Sharp = 12,341s

With a few seconds grace (13) at the end of the day, the total number of seconds matches that of the conventional 24 hour clock.

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
