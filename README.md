# 192K EGA Moar Ram Expansion Board

Standard IBM EGA cards came with only 64KB of memory onboard which isn't quite enough to run all the software that supports this graphics standard. In particular, the 640x350x4bpp mode requires more than 64KB of memory. Some demos and games may also use the extra video memory for sprites and other graphical effects.

Expanding an EGA card to the full 256KB requires a 192KB memory expansion card, which are somewhat hard to find now. This project is a clone of the board.

[Schematic](https://github.com/schlae/EGAMemory/blob/main/EGAMemory.pdf)

[Fab Files](https://github.com/schlae/EGAMemory/blob/main/fab/EGAMemory-Rev1.zip)

The bill of materials is as follows

| Quantity | Designator | Mouser part number |
|----------|------------|--------------------|
| 16       | C1-C16     | 594-K473K15X7RF5UH5 |
| 3        | C17-C19    | 80-T398E106M16AT or 74-199D10V10-E |
| 2        | H1, H2     | 534-8803 |
| 1        | U9         | 595-SN74LS04N |
| 24       | U1-U8,U10-U25 | TMS4416-15 or equivalent 150ns DRAM |
| 1        | P1         | 571-3-826632-2 or equiv |


## Build Notes

The PCB is 6.125" x 3.9" (156mm x 99mm). It is 0.0625" (1.6mm) thick. Unusually, this board can be built either as a 2-layer board or as a 4-layer board, since the inner layers are only used for power and ground and there are redundant traces on the outside layers. With 4 layers, you may get better EMI performance but the board should be functionally the same even with just 2 layers.

You should purchase 24 IC sockets (18-pin) for the memory, since these older RAM chips are known to go bad. The chips are not available from Mouser; you'll need to find them at online auctions or chip broker sites.

All components are installed on the top of the board (the side with the silkscreen designators)

The original tantalum capacitors are 3-lead so they cannot be installed backwards. These capacitors are still available but are quite expensive, so I've provided an alternate part number for a much cheaper 2-pin tantalum. Be sure to install the positive lead in the center hole of the capacitor footprint. The negative lead can go in either of the other two holes.

To prevent the IC pins from shorting out against adjacent ISA cards, you should install a plastic sheet on the solder side of the expansion board. I have provided a [DXF file](https://github.com/schlae/EGAMemory/blob/main/mech/InsulatorCard.DXF) that you can use with a laser engraver. A card of 0.02" (0.5mm) should be thick enough.

## Installation

Plug the board into the EGA expansion connector at the front of the card (the end opposite the video connectors). It installs clamshell-style, with the memory chips facing the logic chips on the EGA card.

Test it with QBASIC, a game, or your favorite EGA demo.

## License
This work is licensed under a Creative Commons Attribution-ShareAlike 4.0
International License. See [https://creativecommons.org/licenses/by-sa/4.0/](https://creativecommons.org/licenses/by-sa/4.0/).

