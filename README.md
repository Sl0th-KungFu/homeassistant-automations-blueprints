# homeassistant-automations-blueprints

A collection of Home Assistant automations and blueprints used in my personal smart home setup.

## Blueprints

- **Covers — Sunrise**
  - [blueprints/covers/sunrise/cover_open.yaml](blueprints/covers/sunrise/cover_open.yaml): Opens a cover at different sunrise times depending on workday status; opens at configured times on normal days and holidays, otherwise opens after sunrise with a configurable delay timer.
  - [blueprints/covers/sunrise/cover_open_time_only.yaml](blueprints/covers/sunrise/cover_open_time_only.yaml): Opens a cover at different configured times depending on workday status; no sunrise trigger and no delay logic.
  - [blueprints/covers/sunrise/cover_open_with_presence.yaml](blueprints/covers/sunrise/cover_open_with_presence.yaml): Opens a cover depending on sunrise or configured times; behavior differs between workdays and holidays and only executes if the selected person is at the selected zone.

- **Covers — Sunset**
  - [blueprints/covers/sunset/cover_close.yaml](blueprints/covers/sunset/cover_close.yaml): Closes a cover at sunset (after a delay) or at a fixed time; sets the configured target position.
  - [blueprints/covers/sunset/cover_close_position.yaml](blueprints/covers/sunset/cover_close_position.yaml): Closes a cover at sunset or fixed time to a desired position (reads target from an input_number entity).
  - [blueprints/covers/sunset/cover_close_with_sensor_check.yaml](blueprints/covers/sunset/cover_close_with_sensor_check.yaml): Closes a cover at sunset (after a delay) or at a fixed time only if a binary sensor (e.g., PC status) is off and the cover is still mostly open; intended for offices.

## Usage

- Copy the blueprint YAML files into Home Assistant's `config/blueprints/automation/` folder or import them via the Home Assistant UI.
- Configure the blueprint inputs in the UI (select cover, timers, sensors, persons/zones, etc.) and enable the automation.
