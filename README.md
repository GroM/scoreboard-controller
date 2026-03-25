# LVGL Scoreboard Controller

Landscape LVGL Pro / XML scoreboard project for the Waveshare ESP32-S3 Touch LCD 3.49" display (`640x172`).

This repository is intended to be maintained as an XML-only LVGL 8 editor project. The XML files are the only source of truth.

## Screen Layout

The UI is organized as five columns:

1. Home controls: `+1`, `-1`
2. Home score
3. Timer, `Start`, `Pause`, `Reset`
4. Guest score
5. Guest controls: `+1`, `-1`

The score buttons stay on the outer edges, while the timer and score values remain central and readable.

## LVGL Pro Files

The editable source of truth for LVGL Pro is:

- `globals.xml`
- `screens/scoreboard.xml`
- `components/`
- `widgets/`
- `fonts/`
- `images/`
- `CMakeLists.txt`

This now mirrors the generated `ui/` skeleton from the current branch, which is a better baseline for editor compatibility than the earlier guessed `project.xml` layout.

## Current Scope

This repository is UI-only for now. The XML screen focuses on editable layout and visual structure for the scoreboard:

- home `+1` / `-1`
- home score
- timer with `Start`, `Pause`, `Reset`
- guest score
- guest `+1` / `-1`

Runtime/exported code should be generated from the editor later instead of maintained by hand in this repository.

## Files

- `globals.xml`: global declarations and shared project placeholders
- `screens/scoreboard.xml`: editable scoreboard screen with local styles
- `components/`, `widgets/`, `fonts/`, `images/`: supporting project folders for future XML assets and reuse
- `CMakeLists.txt`: preview/runtime helper used by the editor flow

## LVGL 8 Note

The repository has been cleaned so it no longer carries a handwritten C scaffold with mixed-version assumptions. This root layout is now based on the `/ui` folder skeleton from the current branch.

## Editor Friendliness

The repository now contains only the editor-oriented XML project files and supporting folders, which keeps the project simpler to validate and easier to cleanly regenerate later.
