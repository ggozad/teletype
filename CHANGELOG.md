# Changelog

## vNext

## v1.41
- **NEW**: added Ansible remote commands `LV.CV` and `CY.CV`
- **NEW**: Added TELEX Modules Support for the TXi and the TXo
- **NEW**: 75 New Operators Across the Two Modules
- **NEW**: Supports all basic Teletype functions (add `TI` and `TO` to the commands you already know)
- **NEW**: Extended functionality allows for additional capabilities for existing functions
- **NEW**: Experimental input operators add capabilities such as input range mapping and quantization
- **NEW**: Experimental output operators add oscillators, envelopes, independent metronomes, pulse dividing, etc.
- **NEW**: [Full List of Methods Found and Maintained Here](https://github.com/bpcmusic/telex/blob/master/commands.md)

## v1.21
- **NEW**: Just Friends ops: `JF.GOD`, `JF.MODE`, `JF.NOTE`, `JF.RMODE`, `JF.RUN`, `JF.SHIFT`, `JF.TICK`, `JF.TR`, `JF.VOX`, `JF.VTR`

## v1.2
- **NEW**: Ansible support added to ops: `CV`, `CV.OFF`, `CV.SET`, `CV.SLEW`, `STATE`, `TR`, `TR.POL`, `TR.PULSE`, `TR.TIME`, `TR.TOG`
- **NEW**: `P.RM` will also return the value removed
- **NEW**: `ER` op
- **IMP**: a `TR.TIME` of 0 will disable the pulse
- **IMP**: `O.DIR` renamed to `O.INC`, it's the value by which `O` is *incremented* when it is accessed
- **IMP**: `IF`, `ELIF`, `ELSE` status is reset on each script run
- **IMP**: key repeat now works for all keypresses
- **FIX**: `FLIP` won't interfere with the value of `O`
- **FIX**: the `O` op now returns it's set value *before* updating itself
- **FIX**: the `DRUNK` op now returns it's set value *before* updating itself
- **FIX**: `P.START` and `P.END` were set to 1 when set with too large values, now are set to 63
- **FIX**: `CV.SLEW` is correctly initialised to 1 for all outputs
- **FIX**: several bugs where pattern length wasn't updated in track mode
- **FIX**: fixed `[` and `]` not updating values in track mode

## v1.1
- **NEW**: USB flash drive read/write
- **NEW**: `SCRIPT` op for scripted execution of other scripts!
- **NEW**: `MUTE` and `UNMUTE` ops for disabling trigger input
- **NEW**: hotkeys for `MUTE` toggle per input (meta-shift-number)
- **NEW**: screen indication in live mode for `MUTE` status
- **NEW**: `SCALE` op for scaling number from one range to another
- **NEW**: `JI` op just intonation helper
- **NEW**: `STATE` op to read current state of input triggers 1-8 (low/high = 0/1)
- **NEW**: keypad executes scripts (works for standalone USB keypads and full-sized keyboards)
- **NEW**: `KILL` op clears delays, stack, CV slews, pulses
- **NEW**: hotkey meta+ESC executes `KILL`
- **NEW**: `ABS` op absolute value, single argument
- **NEW**: `FLIP` op variable which changes state (0/1) on each read
- **NEW**: logic ops: `AND`, `OR`, `XOR`
- **NEW**: `O` ops: `O.MIN`, `O.MAX`, `O.WRAP`, `O.DIR` for counter range control
- **NEW**: `DRUNK` ops: `DRUNK.MIN`, `DRUNK.MAX`, `DRUNK.WRAP` for range control
- **NEW**: `TR.POL` specifies the polarity of `TR.PULSE`
- **NEW**: if powered down in tracker mode, will power up in tracker mode
- **IMP**: `TR.PULSE` retrigger behaviour now predictable
- **IMP**: mode switch keys more consistent (not constantly resetting to live mode)
- **FIX**: bug in command history in live mode
- **FIX**: `EXP` op now exists
- **FIX**: `P` and `PN` parse error
- **FIX**: possible crash on excess length line entry
- **FIX**: `CV` wrapping with negative `CV.OFF` values
- **FIX**: INIT script executed now on keyboardless scene recall
- **FIX**: `Q.AVG` overflow no more
- **FIX**: `P.PUSH` will fully fill a pattern
- **FIX**: `CV.SET` followed by slewed CV in one command works
- **FIX**: `DEL 0` no longer voids command

## v1.0
- Initial release
