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

- `project.xml`
- `screens/scoreboard.xml`
- `components/`
- `widgets/`
- `fonts/`
- `images/`

This is the project structure LVGL Pro expects for an editable XML-based project.

## Current Scope

This repository is UI-only for now. The XML screen focuses on editable layout and visual structure for the scoreboard:

- home `+1` / `-1`
- home score
- timer with `Start`, `Pause`, `Reset`
- guest score
- guest `+1` / `-1`

Runtime/exported code should be generated from the editor later instead of maintained by hand in this repository.

## Files

- `project.xml`: LVGL Pro project definition and target display
- `screens/scoreboard.xml`: editable scoreboard screen with local styles
- `components/`, `widgets/`, `fonts/`, `images/`: supporting project folders for future XML assets and reuse

## LVGL 8 Note

The repository has been cleaned so it no longer carries a handwritten C scaffold with mixed-version assumptions. If your LVGL Pro installation offers an LVGL 8 code-generation/export target, that generated output should be treated as a build artifact derived from these XML files rather than committed as the maintained source.

## Editor Friendliness

The repository now contains only the editor-oriented XML project files and supporting folders, which keeps the project simpler to validate and easier to cleanly regenerate later.
