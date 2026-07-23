---
name: proteus-stm32-homework
description: Use this skill when debugging or finishing a Proteus plus Keil STM32F103 homework project, especially when code, GPIO wiring, hex loading, simulation behavior, and final full-folder packaging all need to be aligned.
---

# Proteus STM32 Homework

Use this skill for student-style embedded assignments built around `STM32F103`, `Proteus`, `Keil`, `.pdsprj`, `.uvprojx`, and generated `.hex` files.

Typical triggers:

- The user provides a Proteus project and wants the behavior to match an example video or screenshot.
- The circuit simulates but GPIO behavior does not match the code.
- The user needs the final submission packaged as a complete engineering folder, not just source files.

## Workflow

1. Inspect the workspace first.
   Find the Proteus project, Keil project, source files, and current hex outputs with `rg --files` or `Get-ChildItem -Recurse`.

2. Confirm what is failing.
   Separate these cases:
   - `hex` path or firmware loading failure inside Proteus
   - code is running but GPIO mapping is wrong
   - timer or main loop logic is wrong
   - Proteus button or LED wiring is misleading

3. Read the code before changing it.
   Start with the main control file, usually `User/main.c`, then verify startup and interrupt linkage if timers are involved.
   Check whether handlers such as `TIM2_IRQHandler` are actually linked by reading the map file.

4. Match code to the actual schematic.
   Do not assume the intended pinout is correct.
   Read the visible Proteus connections and align:
   - `KEY1` input pin
   - `D1` output pin
   - LCD control pins
   If the schematic is ambiguous, reduce the code to the smallest reliable mapping instead of keeping broad compatibility guesses.

5. Simplify aggressively when debugging.
   If interrupts or peripheral timing are suspect, replace them temporarily with a simpler implementation that proves the execution path:
   - timer interrupt
   - `SysTick`
   - main-loop polling with `DelayMs`
   Move from complex to simple until the hardware behavior becomes observable.

6. Rebuild and replace the active hex.
   Use Keil command-line rebuild against the real `.uvprojx`.
   Verify:
   - build completes with `0 Error(s), 0 Warning(s)` when possible
   - the generated `ADC.hex` or equivalent has a fresh timestamp
   - the user-facing `hex` in the working Proteus path is overwritten with the latest build

7. Validate with the user using concrete expectations.
   Give exact expected outcomes such as:
   - power-on state
   - whether counting starts automatically or after `KEY1`
   - exact second when `D1` should toggle
   Avoid vague statements like "try again and see."

8. Package the full submission.
   For homework delivery, include the whole engineering folder:
   - Proteus project
   - Keil project
   - source files
   - generated hex
   - any concise README already used in the task
   Compress the full project folder into a single zip in the outputs directory.

## Debug Priorities

Use this order when the user says "it still doesn't work":

1. Confirm the loaded `hex` is the newest file.
2. Confirm the MCU is actually executing code by forcing visible behavior.
3. Confirm `KEY1` and `D1` are mapped to the real pins in the schematic.
4. Only then refine the timer or assignment-specific logic.

## Good Outcomes

A task is complete when all of these are true:

- Proteus visibly behaves according to the assignment.
- The `hex` being simulated is the newest compiled artifact.
- The full engineering folder is zipped for submission.
- The user gets the exact zip path to submit.
