# Arm Cortex-M3/M4 Programming

Collection of example projects and utilities for programming ARM Cortex‑M3 / M4 microcontrollers. This repository contains simple examples, SVC/math helpers, bit-banding demos, a task scheduler, and reference resources.

## Repository layout

- 001_hello — basic startup / "hello" examples
- 1_inline — inline assembly / inline function examples
- bit_banding — examples and demonstrations of bit-banding usage
- svc_math.c — example SVC (supervisor call) math helper implementation
- svc_math/ — supporting files and examples for SVC math
- task_scheduler — cooperative/simple scheduler examples
- resources — reference files, datasheets, notes, or build scripts

> Note: Some subfolders may include their own README or Makefile with example-specific build/run instructions.

## Requirements

- ARM GCC toolchain (arm-none-eabi-gcc)
- make (or another build system used in the example)
- OpenOCD or vendor flasher (ST-Link, J-Link, etc.) to flash hardware
- A target board with an ARM Cortex-M3 or M4 MCU

## Build & flash (example steps)

1. cd into an example directory (e.g., `001_hello`)
2. run `make` (or follow the example's build instructions)
3. flash to target with OpenOCD or vendor tool, e.g.:
   - `openocd -f interface/stlink.cfg -f target/stm32f4x.cfg -c "program build/firmware.elf verify reset exit"`
   - or use `st-flash` / J-Link CLI depending on your setup

## svc_math

The `svc_math.c` file contains example SVC handlers used to demonstrate supervisor calls for math operations. Review comments in the file for usage details and integration notes.

## Contributing

PRs welcome. When contributing examples, please include:
- a short description of the change
- build instructions for new examples
- the target MCU/board used for testing

## License

Add a LICENSE file to indicate repository licensing (e.g., MIT). If you want, tell me which license to add and I will create it.

---

If you'd like I can update the README with specific build instructions for a particular board or example, or add a LICENSE file. Reply with which branch to use (or I will use the repository default).