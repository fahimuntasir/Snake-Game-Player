# Snake Game Player — LPC2124 Embedded Systems Project

**Embedded C · ARM7 Microcontroller · Keil µVision · Proteus**

This repository documents a **Snake Game embedded-systems course project** prepared at **Hubei University of Technology**. The work combines an LPC2124 microcontroller program with keypad input, graphical LCD output, and circuit setup and simulation work in **Proteus**.

The repository includes the Keil project, embedded C source and support files, a generated HEX image, and the academic project report.

## Project Overview

The application implements the core Snake Game loop for a microcontroller-based display:

- Read directional input using a matrix-keypad scanning routine
- Update snake position and direction
- Draw the snake and food on a graphical LCD
- Generate food positions and grow the snake after a food collision
- Check for collisions with the snake's body
- Wrap the snake to the opposite side when it crosses a screen boundary

The source represents the snake as an **array of positions** (`struct Snake snake[1000]`), rather than a doubly linked list. The program uses low-level GPIO access and display-driver functions suitable for the LPC2124 target.

## Hardware and Software

| Component | Description |
| --- | --- |
| Microcontroller | NXP LPC2124, ARM7TDMI family |
| Input | 4×4 matrix keypad, handled through GPIO scanning |
| Output | Graphical LCD with supporting driver code |
| Programming language | Embedded C, with ARM startup assembly |
| Development environment | Keil µVision / MDK-ARM |
| Circuit setup | Proteus simulation environment |
| Output artifact | `Snake Game/Objects/Snake_Game.hex` |

**Display note:** The driver source refers to a T6963C-based graphical LCD module. The exact Proteus display part and circuit wiring are not provided as project files in this repository.

## Proteus Setup and Simulation

Proteus was used during the coursework for the **microcontroller circuit setup and integration work**, alongside the C program developed in Keil. The setup involved configuring the LPC2124-based circuit and its display/keypad connections for the Snake Game demonstration.

The accompanying report provides academic documentation of the project. **The Proteus schematic or project file is not currently included in the repository**, so the original circuit cannot be opened directly from GitHub.

For a compatible Proteus recreation, the general workflow is:

1. Create an LPC2124-based circuit with compatible keypad and graphical LCD components.
2. Connect the peripherals according to the GPIO mapping expected by the source and LCD driver.
3. Configure the microcontroller with the generated HEX image.
4. Run the simulation and check the keypad response and game display.

These are general reconstruction steps, **not a verified pin-by-pin wiring guide**. An original Proteus design file or clear circuit screenshot would be needed for exact reproduction.

## Repository Structure

```text
Snake-Game-Player/
├── README.md
├── Embedded System Course Design_1911521213_王一然.pdf
└── Snake Game/
    ├── main.c                   # Game state, snake movement, keypad logic
    ├── lcddrv.c                 # Graphical LCD driver routines
    ├── lcddrv.h
    ├── config.h                 # Microcontroller and project configuration
    ├── target.c
    ├── target.h
    ├── Startup.s                # ARM startup assembly
    ├── Snake_Game.uvproj        # Keil project
    ├── Snake_Game.uvopt
    ├── Objects/
    │   └── Snake_Game.hex       # Generated program image
    └── Listings/                # Build listings and map file
```

## Building the Firmware

1. Open `Snake Game/Snake_Game.uvproj` in a compatible **Keil µVision** environment with LPC2124 and ARM Compiler 5 support.
2. Check the device and target settings.
3. Build the target to generate an updated HEX file.
4. If you have the matching Proteus circuit, assign the HEX image to the LPC2124 component and run the simulation.

The included build log records a successful legacy Keil build with **0 errors and 0 warnings**. This does not establish compatibility with current toolchains or confirm that a complete Proteus circuit is available here.

## Scope and Limitations

- The game uses an array for snake segments; a linked-list implementation is **not** present.
- The programmed behavior includes screen-edge wrapping, so boundaries are not treated as game-over collisions.
- The source uses low-level peripheral code and requires a correctly configured LPC2124/LCD/keypad setup.
- The simulation design file, exact component wiring, and independent runtime test results are not included in this repository.
- The code is preserved as educational embedded-systems coursework, not as a portable PC game or production firmware.

## Academic Information

- **Course:** Embedded System Course Design
- **Department:** Computer Science and Technology
- **University:** Hubei University of Technology
- **Instructor:** Dr. Liu Chun
- **Student:** Muntasir Md Fahim 
- **Documentation:** [Embedded System Course Design Report](Embedded%20System%20Course%20Design_1911521213_%E7%8E%8B%E4%B8%80%E7%84%B6.pdf)

## References and Acknowledgments

The project combines embedded-programming examples, supporting microcontroller/LCD code, and course-specific configuration and simulation work. Some routines were adapted from existing educational sources whose original links are no longer available.

The source files retain earlier author and copyright notices. In particular, `config.h` and `target.h` identify **Guangzhou ZLG-MCU Development Co., Ltd.** and **Chen Mingji** in their historical headers. Those notices should be preserved when reusing the files.

This repository is shared for **academic documentation and learning**. No blanket reuse license is granted for third-party material without confirmation of its original terms.
