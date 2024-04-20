# Line isolator
Here is a cheap solution to get rid of ground loop and phase issues when routing a guitar signal into multiple amplifiers.

![drawing]

Note that this is not a DI box but rather a tool to help you conveniently "fix" you signal chain on stage.

## Schematic

[ ![Line isolator schematic][schematic_svg] ][schematic_link]
(Black and white version available [here][schematic_link_bw].)

It uses a cheap signal transformer which costs about 5€ ([see TY-250P datasheet][datasheet]). You should be able to replace it with any symetrical signal transformer with a flat 20-20k Hz frequency response.

The input buffer is necessary because guitar pickups are high impedance (maybe around 5k to 15k) while the transformer has a low input impedance (in this case 1k).

I didn't choose the `TL071` opamp for any particular reason. It's just what I had in stock, and it works great! 

## Features:
- **Buffer**: takes a high impedance input signal and outputs a low impedance one.
- **Ground lift**: isolates your input signal from the output, effectively removing ground loop noise.
- **Phase flip**: flip the polarity/phase of your signal.
- **Balanced signal**: converts an unbalanced signal to a balanced signal.

### I/O

- **Active input**: Takes a high impedance signal (i.e. guitar). Requires 9V power.
- **Passive input**: Takes a low impedance signal (i.e. from another pedal's buffered output) and bypasses the buffer circuit entirely. Doesn't need any power.
- **Output**: A low impedance,  balanced (TRS) or unbalanced (TS) signal at the same level as the input.


[datasheet]: https://catalog.triadmagnetics.com/Asset/TY-250P.pdf
[drawing]: drawing.png
[schematic_svg]: schematic-line-isolator.svg
[schematic_link]: schematic-line-isolator.pdf
[schematic_link_bw]: schematic-line-isolator-bw.pdf