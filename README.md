# Bluetti solar charger (Home Assistant)

One automation (every 2 min) that charges a Bluetti AC70 through a smart plug **only with real solar surplus** (battery charging power ≤ −1600 W), keeps it charging until full, releases it when solar is no longer enough (so the power station acts as a battery), and has a critical protection (SOC ≤ 5 % or < 30 min left → reconnect).

| Path | What |
|---|---|
| `homeassistant/packages/bluetti_charger.yaml` | The automation and its on/off helper |
| `esphome/archive/bluetti.yaml` | An ESP32 BLE experiment from before the `bluetti_bt` integration |

## Requires
- [solar-inverter-modbus-monitor](https://github.com/KleverBatista-max/solar-inverter-modbus-monitor) for `sensor.inverter_battery_power`.
- `bluetti_bt` custom integration (HACS) and a smart plug; adapt entity IDs.
- Pairs well with [solar-ac-controller](https://github.com/KleverBatista-max/solar-ac-controller). Overview: [solar-home-overview](https://github.com/KleverBatista-max/solar-home-overview).

Created by **John Batista** ([@KleverBatista-max](https://github.com/KleverBatista-max)). Built with AI assistants (ChatGPT, Claude) as tools. MIT licensed. Secrets are not included; replace `!secret` values and regenerate ESPHome keys.
