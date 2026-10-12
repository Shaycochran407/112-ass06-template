# AGENTS.md

This repository is a small C project built with GCC and Make. The main goal is to implement and verify the functions declared in the header and exercised from the test harness.

## Build and verification

- Run the project build from the repository root with `mingw32-make`.
- The default target builds `bin/main.exe` from the object files in `obj/`.
- Use `mingw32-make clean` to remove generated build artifacts (`obj/` and `bin/`).
- Prefer fixing all compiler warnings because the build uses `-Wall`.

## Project layout

- `include/code.h`: public declarations, structs, typedefs, and function prototypes.
- `src/code.c`: implementation file for the assignment logic.
- `src/main.c`: sandbox/test harness for quick manual validation.
- `Makefile`: build rules for compiling the project.
- `lib/`: supporting library code or assets, if added later.

## Conventions

- Keep declarations in the header and definitions in the source file.
- Do not rename existing structs, typedefs, or function names unless the task explicitly requires it.
- Match the existing C coding style and assignment-specific API contracts exactly.
- Preserve include guards and keep any new helper functions consistent with the project’s naming patterns.
- Avoid editing generated binaries or build output files directly.

## Typical workflow

1. Update the declaration in `include/code.h` when a function signature changes.
2. Implement or fix the matching logic in `src/code.c`.
3. Use `src/main.c` for quick manual checks when needed.
4. Rebuild with `mingw32-make` to confirm the project compiles cleanly.

## Notes for AI agents

- This project is assignment-focused and intentionally small; changes should stay minimal and targeted.
- Prefer correctness over large refactors.
- If you need to verify behavior beyond compilation, add focused test code in `src/main.c` rather than changing the project structure.
