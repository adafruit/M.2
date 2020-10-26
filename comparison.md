# M.2 Maker boards comparison

This is an attempt to better understand the similarities and differences between the existing boards.

## M.2 Pin usage

| Pin | Key E (1-SD)    | Google          | makerdiary    | Particle   | SparkFun    | Sipeed     | WRTnode    | SNAPZZ gen.1  |
| --- | --------------- | --------------- | ------------- | ---------- | ----------- | ---------- | ---------- | ------------- |
| 1   | GND             | GND             | GND           | GND        | GND         | IO39       | UART1_RX   | GND           |
| 2   | 3.3V            | 3.3V            | 3.3V          | VCC        | 3.3V        | 5V         | 3.3V.      | 3.3V          |
| 3   | USB_DP          | NC              | USB_DP        | GND        | USB_DP      | IO37       | GND        | NC            |
| 4   | 3.3V            | 3.3V            | 3.3V          | VCC        | 3.3V EN     | 5V         | 3.3V       | 3.3V          |
| 5   | USB_DM          | NC              | USB_DM        | GND        | USB_DM      | IO38       | GND        | NC            |
| 6   | LED1#(I)(OD)    | NC              | P0.19         | VCC        | RESET#      | GND        | UART1_TX   | NC            |
| 7   | GND             | GND             | GND           | GND        | GND         | IO36       | USB_DP     | NC            |
| 8   | PCM (1.8V)      | NC              | P0.20         | VCC        | G11         | GND        | WLED       | NC            |
| 9   | SDIO (1.8V)     | NC              | P0.11         | GND        | USB_VIN     | IO34       | USB_DM     | NC            |
| 10  | PCM (1.8V)      | NC              | P0.21         | 3.3V       | D0          | RST        | LINK0      | NC            |
| 11  | SDIO (1.8V)     | NC              | P0.12         | USB_DP     | BOOT        | IO35       | GND        | NC            |
| 12  | PCM (1.8V)      | NC              | P0.22         | 3.3V       | I2C_SDA     | Key B slot | Key B slot | NC            |
| 13  | SDIO (1.8V)     | NC              | P1.08         | USB_DN     | UART_RTS1   | Key B slot | Key B slot | NC            |
| 14  | PCM (1.8V)      | NC              | P0.23         | RSV        | I2C_SCL     | Key B slot | Key B slot | NC            |
| 15  | SDIO (1.8V)     | NC              | P1.09         | GND        | UART_CTS1   | Key B slot | Key B slot | NC            |
| 16  | LED2#           | NC              | P0.24         | VUSB       | I2C_INT#    | Key B slot | Key B slot | NC            |
| 17  | SDIO (1.8V)     | NC              | P0.08         | NFC1       | UART_TX1    | Key B slot | Key B slot | NC            |
| 18  | GND             | GND             | GND           | RSV        | D1          | Key B slot | Key B slot | NC            |
| 19  | SDIO (1.8V)     | NC              | P0.07         | NFC2       | UART_RX1    | Key B slot | Key B slot | NC            |
| 20  | UART_WAKE#(3.3V)| NC              | P0.25         | SCL        | UART_RX2    | IO47       | LINK1      | NC            |
| 21  | SDIO (1.8V)     | NC              | P0.06         | GND        | SWDCK       | IO32       | LINK2      | NC            |
| 22  | UART RXD (1.8V) | NC              | P0.16         | SDA        | UART_TX2    | IO45       | LINK3      | NC            |
| 23  | SDIO (1.8V)     | NC              | P0.05 / AIN3  | ADC0       | SWDIO       | IO33       | LINK4      | GPIO-0        |
| 24  | Key E slot      | Key E slot      | Key E slot    | Key E slot | Key E slot  | IO43       | RXIP0      | Key E slot    |
| 25  | Key E slot      | Key E slot      | Key E slot    | Key E slot | Key E slot  | IO30       | REF_CLK0   | Key E slot    |
| 26  | Key E slot      | Key E slot      | Key E slot    | Key E slot | Key E slot  | IO41       | RXIN0      | Key E slot    |
| 27  | Key E slot      | Key E slot      | Key E slot    | Key E slot | Key E slot  | IO31       | GND        | Key E slot    |
| 28  | Key E slot      | Key E slot      | Key E slot    | Key E slot | Key E slot  | IO40       | TXOP0      | Key E slot    |
| 29  | Key E slot      | Key E slot      | Key E slot    | Key E slot | Key E slot  | IO28       | TXON4      | Key E slot    |
| 30  | Key E slot      | Key E slot      | Key E slot    | Key E slot | Key E slot  | IO42       | TXON0      | Key E slot    |
| 31  | Key E slot      | Key E slot      | Key E slot    | Key E slot | Key E slot  | IO29       | TXOP4      | Key E slot    |
| 32  | UART TXD (1.8V) | NC              | P0.15         | MODE       | PWM0        | IO44       | RXIN4      | NC            |
| 33  | GND             | GND             | GND           | ADC1       | GND         | IO26       | GND        | NC            |
| 34  | UART CTS (1.8V) | NC              | P0.14         | RESET      | A0          | IO46       | RXIP4      | NC            |
| 35  | PETp0           | PERn0           | RSV           | ADC2       | USBHOST_DP  | IO27       | RXIN3      | NC            |
| 36  | UART RTS (1.8V) | NC              | P0.13         | TX         | GND         | IO8        | TXON3      | NC            |
| 37  | PETn0           | PERp0           | RSV           | ADC3       | USBHOST_DM  | IO24       | RXIP3      | NC            |
| 38  | VENDOR          | RST_EN          | RESET / P0.18 | RX         | A1          | IO6        | TXOP3      | IO4           |
| 39  | GND             | GND             | GND           | AGND       | GND         | IO25       | GND        | NC            |
| 40  | VENDOR          | NC              | SWDIO         | CTS        | G0 / BUS0   | IO5        | TXON2      | USB_TTL-TX    |
| 41  | PERp0           | PETp0           | RSV           | ADC4       | CAN_RX      | IO22       | PCIE_TXN   | NC            |
| 42  | VENDOR          | NC              | SWDCLK        | RTS        | G1 / BUS1   | IO4        | TXOP2      | USB_TTL-RX    |
| 43  | PERn0           | PETn0           | RSV           | ADC5       | CAN_TX      | IO23       | PCIE_TXP   | IO3           |
| 44  | COEX (1.8V)     | NC              | P1.00         | MOD USB_DP | G2 / BUS2   | SPI0_D7    | RXIN2      | NC            |
| 45  | GND             | GND             | GND           | ADC6       | GND         | IO20       | GND        | NC            |
| 46  | COEX (1.8V)     | NC              | P1.01         | MOD USB_DM | G3 / BUS3   | SPI0_D6    | RXIP2      | NC            |
| 47  | REFCLKp0        | REFCLKp0        | RSV           | ADC7       | PWM1        | IO21       | PCIE_RXN   | USB-DN        |
| 48  | COEX (1.8V)     | NC              | P1.02         | CS         | G4 / BUS4   | SPI0_D5    | GPIO0      | USB-tgt-sel   |
| 49  | REFCLKn0        | REFCLKn0        | RSV           | AGND       | BATT_VIN    | IO18       | PCIE_RXP   | USB-DP        |
| 50  | SUSCLK (32KHz)  | NC              | RSV           | MISO       | AUD_BCLK    | SPI0_D4    | PERSTN     | NC            |
| 51  | GND             | GND             | GND           | RSV        | I2C_SDA1    | IO19       | GND        | NC            |
| 52  | PERST0# (3.3V)  | PERST0# (3.3V)  | RSV           | MOSI       | AUD_LRCLK   | SPI0_D3    | RXIN1      | NC            |
| 53  | CLKREQ0# (3.3V) | CLKREQ0# (3.3V) | RSV           | RSV        | I2C_SCL1    | BOOT       | PCIE_CKN   | I2C_SCL1      |
| 54  | W_DISABLE (3.3V)| NC              | P1.03         | SCK        | AUD_IN      | SPI0_D2    | RXIP1      | NC            |
| 55  | PEWAKE0 (3.3V)  | GND             | RSV           | RSV        | SPI_CS      | IO17       | PCIE_CKP   | I2C_SDA1      |
| 56  | W_DISABLE (3.3V)| NC              | P1.04         | GND        | AUD_OUT     | SPI0_D1    | TXON1      | NC            |
| 57  | GND             | GND             | GND           | RSV        | SPI_SCK     | IO14       | GND        | NC            |
| 58  | SDA             | NC              | P1.05         | RSV        | AUD_MCLK    | SPI0_D0    | TXOP1      | I2C_SDA       |
| 59  | PETp1           | PERn1           | P0.04 / AIN2  | RSV        | SPI_COPI    | IO16       | UART0_RX   | NC            |
| 60  | SDC             | NC              | P1.06         | RSV        | SDIO_SCK    | DVP_D0     | UART0_TX   | I2C_SCL       |
| 61  | PETn1           | PERp1           | P0.26         | RED        | SPI_CIPO    | IO12       | SPI_MOSI   | NC            |
| 62  | ALERT# (3.3V)   | ALERT# (3.3V)   | P1.07         | GPIO0      | SDIO_CMD    | DVP_D1     | SPI_MISO   | NC            |
| 63  | GND             | GND             | GND           | GREEN      | G10         | IO13       | SPI_CLK    | NC            |
| 64  | VENDOR          | NC              | VBUS          | GPIO1      | SDIO_DATA0  | DVP_D2     | SPI_CS1    | Mod-RST_EN    |
| 65  | PERp1           | PETp1           | P0.27         | BLUE       | G9          | IO10       | SDA        | NC            |
| 66  | PERST1# (3.3V)  | PERST1# (3.3V)  | RSV           | PWM0       | SDIO_DATA1  | DVP_D3     | SCLK       | NC            |
| 67  | PERn1           | PETn1           | P0.28 / AIN4  | SIM_VCC    | G8          | IO11       | I2S_CLK    | NC            |
| 68  | CLKREQ1# (3.3V) | CLKREQ1# (3.3V) | RSV           | PWM1       | SDIO_DATA2  | DVP_D4     | I2S_WS     | IO2           |
| 69  | GND             | GND             | GND           | SIM_RST    | G7 / BUS7   | IO9        | I2S_SDO    | NC            |
| 70  | GPIO1/REWAKE1#  | NC              | RSV           | PWM2       | SDIO_DATA3  | DVP_D5     | 3.3V       | IO1           |
| 71  | REFCLKp1        | REFCLKp1        | P0.03 / AIN1  | SIM_CLK    | G6 / BUS6   | IO7        | GND        | NC            |
| 72  | 3.3V            | 3.3V            | 3.3V          | PWM3       | RTC_3V_BATT | DVP_D6     | 3.3V       | 3.3V          |
| 73  | REFCLKn1        | REFCLKn1        | P0.02 / AIN0  | SIM_DATA   | G5 / BUS5   | 3.3V       | GND        | NC            |
| 74  | 3.3V            | 3.3V            | 3.3V          | MOD VBUS   | 3.3V        | DVP_D7     | 3.3V       | 3.3V          |
| 75  | GND             | GND             | GND           | MOD RI     | GND         | 1.8V       | I2S_SDI    | NC            |

## M.2 Mechanical size

| Dimension | Google    | makerdiary    | Particle   | SparkFun    | Sipeed     | WRTnode    | SNAPZZ gen.1 |
| --------- | --------- | ------------- | ---------- | ----------- | ---------- | ---------- | ------------ |
| Key       | Type E    | Type E        | Type E     | Type E      | Type B     | Type B     | Type E       |
| Width     | 22 mm     | 22 mm         | 30 mm      | 22 mm       | 22 mm      | 22 mm      | 22 mm        |
| Length    | 30 mm     | 30 mm         | 42 mm      | 22 mm       | 25 mm      | 42 mm      | 30 / 40 mm   |
| Height    | 2.8 mm    | 2.1 mm        | 5.5 mm     |             | 2.7 mm     | 3.5 mm     | 1.8 mm       |
| Screw pos | Center    | Center        | Center     | Offset, key | Center     | Center     | Centre       |
