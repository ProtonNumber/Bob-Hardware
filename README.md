# Bob!

This is the Kicad Repo for Bob, an open-source flight computer and data logger
for model rocketry.

## Specification
- MCU: Raspberry Pi [RP2040](https://datasheets.raspberrypi.com/rp2040/rp2040-datasheet.pdf) Dual Core Cortex M0+.
- Flash: 2 x Wimbond [W25Q128](https://www.winbond.com/resource-files/W25Q128JV%20RevI%2008232021%20Plus.pdf) 16 MiB Flash chips.
- IMU: QST [QMI8658C](https://www.qstcorp.com/upload/pdf/202301/13-52-25%20QMI8658A%20Datasheet%20Rev%20A.pdf) 16 G / 2048 DPS IMU
- Compass: QST [QMC5883L](https://datasheet.lcsc.com/szlcsc/QST-QMC5883L-TR_C192585.pdf)
- Barometer: HopeRF [HP203B](https://hoperf.com/data/upload/portal/20190307/HP203B_DataSheet_EN_V2.0.pdf)
- GPIO: 16 GPIO pins broken out, plus access to internal I2C bus.
- Pyro: 2 x Pyro channels with continuity detection and separate arming switch.

## Pin Assignments
| GPIO Pin | Usage             | Broken Out? | Notes                                             |
|----------|-------------------|-------------|---------------------------------------------------|
| GPIO 00  | -                 | Y           |                                                   |
| GPIO 01  | -                 | Y           |                                                   |
| GPIO 02  | -                 | Y           |                                                   |
| GPIO 03  | -                 | Y           |                                                   |
| GPIO 04  | -                 | Y           |                                                   |
| GPIO 05  | -                 | Y           |                                                   |
| GPIO 06  | -                 | Y           |                                                   |
| GPIO 07  | Fire Main         | N           |                                                   |
| GPIO 08  | Fire Drogue       | N           |                                                   |
| GPIO 09  | Compass Interrupt | N           |                                                   |
| GPIO 10  | IMU Interrupt 1   | N           |                                                   |
| GPIO 11  | IMU Interrupt 2   | N           |                                                   |
| GPIO 12  | I2C SDA           | Y           |                                                   |
| GPIO 13  | I2C SCL           | Y           |                                                   |
| GPIO 14  | Drogue Continuity | N           |                                                   |
| GPIO 15  | Main Continuity   | N           |                                                   |
| GPIO 16  | Flash SPI RX      | N           |                                                   |
| GPIO 17  | Flash SPI CS      | N           |                                                   |
| GPIO 18  | Flash SPI SCLK    | N           |                                                   |
| GPIO 19  | Flash SPI TX      | N           |                                                   |
| GPIO 20  | Buzzer            | N           | Buzzer is only powered when battery is connected. |
| GPIO 21  | Arming Signal     | Y           | Reads status of the ARM switch                    |
| GPIO 22  | -                 | Y           |                                                   |
| GPIO 23  | -                 | Y           |                                                   |
| GPIO 24  | -                 | Y           |                                                   |
| GPIO 25  | Status LED        | N           |                                                   |
| GPIO 26  | -                 | Y           | May be used as analogue input                     |
| GPIO 27  | -                 | Y           | May be used as analogue input                     |
| GPIO 28  | -                 | Y           | May be used as analogue input                     |
| GPIO 29  | -                 | Y           | May be used as analogue input                     |
