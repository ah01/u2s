# USB To Serial Convertor Board

<p align="center">
<img src="https://raw.githubusercontent.com/Bastlirovo/u2s/master/docs/photo.jpg" width="400" />
</p>

## Features

- Reliable (no CH340 or FTDI232RL clones)
- 3V3 logic but 5V tolerant (no switching needed)
- On board 3V3 regulator (500 mA)
- Over current protection (suitable for development)
- Connector with key (so you can make idiot-proof cables) but DuPont friendly
- Both micro and USB-C connector (they are on opposite side of the board so you cannot use both in same time, but you will have more probability to find correct cable… you know Murphys Law)

## Connector

<p align="center">
<img src="https://raw.githubusercontent.com/Bastlirovo/u2s/master/docs/pinout.png" />
</p>

| Pin | Dir. | Description |
|:---:|:----:| ------------|
| 1 |  | 3.3 V output (max 500 mA)¹ |
| 2 | OUT | Tx Data Enable² |
| 3 |  | GND |
| 4 |  | 5 V output (max 500 mA)¹ |
| 5 | IN | Rx |
| 6 | IN | DSR |
| 7 | OUT | Tx |
| 8 | IN | CTS |
| 9 | OUT | DTR |
| 10 | OUT | RTS |

¹ 500 mA is total maximum for 5 V  and 3.3 V output.

² Indicate transition for half-duplex communication (e.g. for RS-485).

## PCB

- [Schematics](https://raw.githubusercontent.com/Bastlirovo/u2s/master/docs/usb-to-serial.png) ([PDF](https://raw.githubusercontent.com/Bastlirovo/u2s/master/docs/usb-to-serial.pdf))
- [Sources for Eagle CAD](pcb)
- **[Interactive BOM v1](https://ah01.github.io/u2s/ibom/ibom.html)** ([what is this](https://forums.autodesk.com/t5/eagle-forum/interactive-bom-for-eagle/td-p/8291710))

<p align="center">
<img src="https://raw.githubusercontent.com/Bastlirovo/u2s/master/docs/usb-to-serial_top.png" width="280" /> &nbsp; &nbsp;
<img src="https://raw.githubusercontent.com/Bastlirovo/u2s/master/docs/usb-to-serial_bot.png" width="280" />
</p>

## FTDI Template

For all PIN and LED functionality you need to configure FT231XS converter. There is template for [FT Prog](https://www.ftdichip.com/Support/Utilities.htm#FT_PROG) in [ft_prog directory](ft_prog).

## Credits

- [OK2UQL](https://twitter.com/ok2uqlGabo) - Case for 3D printing (see [tweet for example](https://twitter.com/ok2uqlGabo/status/1366835820972376068))
- [Bastlir](https://twitter.com/bastlir) - Update of design to v2 - mini->USB-C connector, OverCurrent LED, other minor updates based on found issues