# PLC-Based Traffic Light Control System

**Industrial automation training project | April–September 2025**  
**Training:** Advanxis Technologies, Port Harcourt, Nigeria  
**Tools:** Allen-Bradley MicroLogix training environment, RSLogix 500, ladder logic, timer-on-delay (TON), start/stop control and indicator lamps

## Overview

This project documents a traffic-light control exercise completed during my industrial automation training. The objective was to control red, yellow and green indicator lamps in a repeating sequence using PLC ladder logic and timer instructions. The exercise combined programming, PLC I/O wiring, relay interfacing and troubleshooting on a training board.

This repository is an **experimental training case study**, not a production-ready traffic-signal controller and not a distributable PLC program. It contains photographs and screenshots documenting the exercise; original editable PLC project files are not included.

## Physical setup

![Training panel with indicator lamps and wiring](images/01-traffic-light-training-panel.jpeg)

*Training board with illuminated indicators and connected wiring. A single photograph does not establish the timing behaviour of an entire cycle.*

The documented setup used start/stop pushbuttons, three indicator lamps, PLC outputs and relay interfaces. The training report describes wiring checks and monitoring of the program while connected to the training hardware.

## Intended control sequence

1. Press **START** to initiate the sequence.
2. Energise the **red** indicator for its timer-controlled interval.
3. Transition to **yellow**, then **green** as each preceding stage completes.
4. Continue cycling until **STOP** is activated.

The SIWES report describes target intervals of **red: 10 seconds, yellow: 3 seconds, green: 7 seconds**. However, some preserved RSLogix screenshots show timer presets of **10** for the yellow or green timers. The screenshots therefore should **not** be taken as verification that this specific captured version used the final 10/3/7-second settings. The original PLC project file is not available to resolve the discrepancy.

## Ladder-logic evidence

### Start/stop, red and yellow lamp control

![Traffic-light ladder logic showing red, yellow and green rungs](images/02-red-yellow-green-ladder-logic.jpeg)

### Yellow-to-green transitions and timers

![RSLogix 500 screenshot showing yellow and green lamp timers](images/03-yellow-green-timer-rungs.jpeg)

### Additional ladder-logic screenshot

![Another capture of RSLogix 500 traffic-light logic](images/04-ladder-logic-overview.jpeg)

These screenshots show **RSLogix 500**, the program's traffic-light-related contact/coil labels and **TON** timers. Some captures display **OFFLINE**, so the screenshots alone do not prove an online execution state. They are presented as records of ladder-logic work, rather than independent proof of field performance.

## Reported testing and troubleshooting

My SIWES training report documents:

- Connecting indicator lamps and pushbuttons to PLC inputs/outputs through training hardware and relay interfaces.
- Checking wiring continuity and connections before testing.
- Observing the programmed light sequence on the training panel.
- Troubleshooting a yellow-light timer preset error; the report says it was adjusted from **5 seconds to 3 seconds**.
- Using PLC programming and testing activities to learn sequencing, interlocking and digital I/O control.

These are **reported training observations**, not a new test conducted for this GitHub publication.

## Engineering concepts demonstrated

- PLC ladder logic and digital input/output mapping
- Start/stop circuits and process sequencing
- TON timers and timer-completion contacts
- Basic interlocking between sequential outputs
- Relay interfacing, wiring verification and debugging

## Scope, attribution and limitations

This was a **supervised training exercise**, not a commercial deployment. The documentation reflects my participation and observations during the course; it does not claim that I independently authored every rung of the source program. The original editable RSLogix project file is unavailable, so no reconstructed program is presented as the original implementation.

The red/yellow/green timing discrepancy between the report and archived screenshots remains unresolved, and the provided images must not be used as evidence that the final program was independently re-tested for publication. The screenshots are training artifacts, not proof of a fully validated safety-critical traffic controller.

**Safety note:** This project is educational. Real-road traffic-signal systems require approved hardware, fault management and safety engineering beyond this exercise.
