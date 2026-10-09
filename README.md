# Monaco GP 64

A Commodore 64 port of Sega's 1979 arcade game **Monaco GP** (the original, not Pro Monaco GP),
shown inside the arcade bezel. The whole 240 x 384 arcade playfield is on screen in true
proportions, scrolling at full frame rate on PAL and NTSC machines.

## Running it

- `MonacoGP64.d64`: `LOAD"MONACO GP",8,1` then `RUN` (or autostart it in VICE).
- `MonacoGP64.prg` is the same program as a single file: load it and `RUN`.

## Controls

On the attract screen: **F1** or fire starts a game, **F3** picks the controller and
**F5** picks automatic or manual gears (both shown under PRESS FIRE). In a game,
**RUN/STOP** pauses.

| | port | steer | accelerator | gears (manual) |
|---|---|---|---|---|
| joystick | 2 | left / right | fire | up = HIGH, down = LOW |
| 1351 mouse | 1 | move left / right, like the arcade's wheel | left button | right button toggles |
| paddles | 1 | paddle A knob | paddle A button | paddle B button toggles |

Picking the paddles also picks automatic gears; the others start with manual gears.
With the paddles, a car put at the start position on the right (when a game starts, and
after a crash) waits there, in its grace, until the knob has been turned far enough to the
right for the rest of its travel to cover the road: about two thirds of the way round on
most roads, a little more on the widest. From then on the car moves with the knob from
where it stands, so it is never swung to wherever the knob was left, and the knob never
runs out of travel before the car is across the road. Turn the knob right while the car
spins or burns and no time is lost. On ice the car slides away from the knob's position,
as it does from the stick's.
Automatic gears change up where low gear stops pulling and back down when the car slows.
The gear you are in shows as **HI** or **LO** beside the clock.

## The game

Race up the road before the clock runs out. Points for distance and overtakes grow with your
speed. Pass 2000 points on the way to the extended-play roads and the game switches to
EXTENDED PLAY when the clock reaches 0: no clock, spare cars instead (they blink in a
column under the gear display), tow trucks, the narrow bridge and the harbour loop. In
normal play a crash spins you and costs time; in extended play it costs a car. Today's
best 5 and your ranking are kept while the machine is on.

## Play-testing

A game that never ends, for trying out the later roads:

    LOAD"MONACO GP",8,1
    POKE 1020,1
    RUN

The clock starts again from 90 instead of running out (extended play still begins when it
runs out with 2000 points past the mark), and a crash in extended play costs no car. It lasts
until the machine is reset.


## Credits

Monaco GP (c) Sega 1979.

This port is built on **Monaco GP Remake (MGPr) v1.5.3 by Ben Geeves**. Its graphics,
tracks, rules, timings and sounds are what the C64 version is made from and checked
against; without it, this game would not have happened.

The MONACO GP logo in the panel is converted from **Zorg's** artwork of the arcade bezel.
This is a fan-made port, not a Sega product, and not for commercial use. The Exomizer
self-extractor in the crunched file is for non-commercial use only.
