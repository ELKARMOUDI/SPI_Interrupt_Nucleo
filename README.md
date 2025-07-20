# STM32F411 Nucleo SPI Interrupt Mode

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue) 
![SPI](https://img.shields.io/badge/SPI-Interrupt_Mode-green)

<img src="https://github.com/user-attachments/assets/37e66d43-0d3e-4c11-826c-b668da84c5e4" width="500" alt="290D243B-2F14-4449-A828-0FC2EFAA27BA">

SPI communication using interrupts on STM32F411 Nucleo.

## Features
- **SPI Master Mode** (SPI1)
- **125kHz Clock** (32MHz/256 prescaler)
- **Full-Duplex** communication
- **10-byte Transfer** with interrupts
- **Completion Callback** handling

## Hardware Setup
| Signal | Nucleo Pin | Connection |
|--------|------------|------------|
| MOSI   | PA7 (D11)  | → Slave MOSI |
| MISO   | PA6 (D12)  | ← Slave MISO |
| SCK    | PA5 (D13)  | → Slave SCK |
| NSS    | PA4 (D10)  | → Slave CS |

## Technical Details
### SPI Configuration 
```c
Mode: Master (SPI1)
Data Size: 8-bit
Clock: Mode 0 (CPOL=0, CPHA=0)
Prescaler: 256 → 125kHz SPI clock (32MHz/256)
