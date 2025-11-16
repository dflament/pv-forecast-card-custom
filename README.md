fork of pv-forecast-card

- Added **max_value_entity** which accepts a sensor (I use a template sensor which calculates the max of all the forecast, rounded up)
- max_value_entity has priority over max_value

For the complete options please go to https://github.com/dropqube/pv-forecast-card as he's the original author of this card


### 🔧 Configuration Options

| Option                          | Type     | Description                                            |
| ------------------------------- | -------- | ------------------------------------------------------ |
| `entity_today` to `entity_day7` | `sensor` | Daily forecast in kWh / If you have less entities just don't use the respective day |
| `entity_remaining`              | `sensor` | Optional: remaining value today (in kWh)               |
| `display_mode`                  | `string` | **NEW**: Display mode: `weekday`, `date`, or `relative` (default: `weekday`) |
| `weekday_format`                | `string` | For weekday mode: `narrow`, `short`, or `long` (default: `short`) |
| `date_format`                   | `string` | For date mode: `short` (12. Jun) or `numeric` (12.6.) (default: `short`) |
| `remaining_label`               | `string` | Custom label for remaining indicator (default: "Rest") |
| `remaining_indicator`           | `string` | Display style for remaining value: `bar` (default) or `marker` |
| `animation_duration`            | `string` | CSS time (e.g. `0.5s`, `2s`)                           |
| `bar_color_start` / `end`       | `string` | Gradient colors for main bars                          |
| `remaining_color_start` / `end` | `string` | Gradient colors for remaining bar                      |
| `gradient_fixed`                | `string` | Set to `true` if you want the gradient fixed           |
| `remaining_threshold`           | `number` | If remaining ≤ this, use `low_color_*`                 |
| `remaining_low_color_start`     | `string` | Alert gradient (start)                                 |
| `remaining_low_color_end`       | `string` | Alert gradient (end)                                   |
| `remaining_blink`               | `boolean`| Remaining bar blinks below threshold                   |
| `max_value`                     | `number` | Maximum value to normalize bar width                   |
| `max_value_entity`              | `sensor` | Maximum value to normalize bar width through a sensor, priority over max_value                  |
| `show_tooltips`                 | `boolean`| Show tooltip when hovering the bar                    |
| `relative_plus_one`             | `boolean`| In relative mode show "+1d" instead of "Tomorrow" (default: `false`) |
