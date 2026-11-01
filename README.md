# Home Assistant

Home Assistant configuration for pflab.

## Blueprints

Automation blueprints live in `blueprints/automation/pflab/`. This matches the path under the Home Assistant `config/` folder.

| File | Blueprint | What it does |
|------|-----------|--------------|
| `plant_watering.yaml` | Plant Watering Reminder | Checks a soil moisture sensor at 09:00, 15:00 and 21:00. Sends a Telegram message when moisture is below the threshold or the sensor is unavailable. |
| `trv_room_control.yaml` | TRV Room-Sensor Control, Window Cutoff & Schedule | Sends a room sensor reading to the TRV (thermostatic radiator valve) as its external temperature. Sets comfort or eco temperature from an optional schedule. Turns the TRV off while a window or door is open. |

## Install

Copy `blueprints/automation/pflab/` to `config/blueprints/automation/pflab/` on the Home Assistant host. Then reload automations, or go to **Settings > Automations & Scenes > Blueprints**. You can also import a single file with **Import Blueprint** and its raw GitHub URL.

The plant watering blueprint needs the `telegram_bot` integration set up first.
