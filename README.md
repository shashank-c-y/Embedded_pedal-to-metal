# STM32C031C6 ADC + Potentiometer + LED — Wokwi

Files:
- `diagram.json` — NUCLEO-C031C6, potentiometer, external LED + 330 ohm resistor, and serial monitor.
- `wokwi.toml` — points Wokwi at the STM32CubeIDE Debug ELF.

Connections:
- Pot VCC -> 3V3
- Pot GND -> GND
- Pot SIG -> PA1 / ADC1 channel 1
- PA5 -> 330 ohm resistor -> LED -> GND
- USART1 TX PA9 -> Wokwi Serial Monitor RX
- USART1 RX PA10 -> Wokwi Serial Monitor TX

Important:
Your current CubeMX code selects `ADC_CHANNEL_1`, which corresponds to PA1 on STM32C031.
Therefore this Wokwi diagram uses PA1 rather than A0/PA0.

The `wokwi.toml` assumes STM32CubeIDE generates:
`Debug/adc.elf`

If your ELF is in a different folder/name, edit that path in `wokwi.toml`.

In VS Code:
1. Build the STM32 project so the ELF exists.
2. Open `diagram.json`.
3. Start the Wokwi simulator.

<img width="1134" height="922" alt="image" src="https://github.com/user-attachments/assets/c8fab17e-4411-454f-b924-dffb28337a34" />

