# Li-Charger
The best charging & power management module for your projects.

## Overview
Li-Charger is a tiny, but super powerful board for charging Li-Ion/Li-Po batteries, powered by the MCP73871 chip. It lets you charge your battery and power your projects at the same time automatically using power path.

### Features
- USB-C Input: Works with standard phone chargers, no adapters, no new plugs.
- Status LEDs: Red = charging, green = full.
- Safe charging: Limited to 200mA, so it won't overheat your battery. If you need faster charging you can short FAST CHARGE solder jumper on the bottom, then it charges with 500mA.
- No NTC needed: Fixed resistor on THERM pin, so it works with most single cell Li-Ion/Li-Po batteries.

## Power Path
- When USB-C is connected, the VOUT pin is powered from USB-C through power path. 
- When USB-C is disconnected, it switches to battery automatically.
- Switching is seamless and hardly ever causes system resets, thanks to the 10uF capacitor.

### Output (VOUT)
- USB-C mode: ~5V from USB-C via power path, not generated.
- Battery mode: ~3.0V-4.2V depending on battery charge.

<sub>VOUT is NOT regulated. It follows the power source.</sub>

## Notes
- Designed for single cell batteries only.
- Double check polarity before powering the board.
- VOUT is not regulated.
- Use FAST CHARGE only if your battery and thermal conditions allow higher charge current.
- Battery protection (BMS/PCM) is recommended.

## BOM
[Click Here](./BOM.csv)
