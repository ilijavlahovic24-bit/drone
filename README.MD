# MIPS Drone
## Status: Active Development

## Overview
MIPS Drone is project meant to replace exam for subject Microprocessor Systems in School of Electrical Engineeringm, University of Belgrade.
Software side of this project includes programming bare-metal in C, simulating harware in Proteus and simulating algorithms using Python scripts.

## Components
| Components | Description | Mass | Dimensions | Price |
|---|---|---|---|---|
| STM32 | Microcontroler | 10g | 16mm x 16mm x 2mm | 5$ |
| IMU | Inertial Measurement Unit  | 6gm | 6mm x 6mm x 2mm | 5$ |


## Prerequisits
- gnu mcu arm none eabi gcc 10.2.1-1.1
- gnu mcu build tools 4.2.1-2 win32-x64
- gnu mcu eclipse 2021 06 R win32 x64

## Instuctions
Instructions to start building project in eclipse:

Eclipse--->Windows--->Preferences--->MCU--->Workspace ARM Toolchains Paths

	Default toolchain(Choose "xPack GNU Arm Embedded GCC")

	Toolchain folder(Set "%extractionPath%\GNU MCU\arm-none-eabi-gcc-10.2.1-1.1\bin")

Eclipse--->Windows--->Preferences--->MCU--->Workspace Build Tools Path

	Build Tools folder(Set "%extractionPath%\GNU MCU\build-tools-4.2.1-2\bin")

Eclipse--->File--->Import...--->C/C++--->Existing Code as Makefile project

	Toolchain for Indexer Settings (Choose "ARM Cross GCC")		

Eclipse--->Project--->Properties--->C/C++ Build--->Settings--->Toolchains

	Check whether Name is set to correct value ("xPack GNU Arm Embedded GCC (arm-none-eabi-gcc)")

	Check whether Toolchain path is set to correct value ("%extractionPath%\GNU MCU\arm-none-eabi-gcc-10.2.1-1.1\bin")

	Check whether Build tools path is set to correct value ("%extractionPath%\GNU MCU\build-tools-4.2.1-2\bin")		

	Select Apply and close because explicit apply may be needed for Eclipse's Indexer to get necessary include informations from the Toolchain	

Eclipse--->Project--->Properties--->C/C++ General--->Paths and symbols--->Symbols--->GNU C

	Add symbol with name "USE_HAL_DRIVER" (value does not matter)

	Add symbol with name "STM32F103x6" (value does not matter)

## Project structure
```
project/ (root)
├── cubemx/ (directorium for Eclipse workspace)
│   └── code/ (Directorim for source code)
│       ├── Core/
│       ├── Drivers/
│       ├── Middlewares/
│       ├── makefile
│       ├── STM32F103R6Tx_FLASH.ld
│       └── code.ioc
├── proteus/ (directoryum for proteus schema)
|    └── proteus.pdsprj
├──models/ (directorium for Autocad and Fusion models) 
├──simulations/ (directorium for python simulations) 
└──doc/ (dorectoriuym for documentation and references) 
```
## References and Documentation
1. STM32F103 Cortex M3 Programming Manual
2. STM32F103 Datasheet
3. STM32F103 Reference Manual
4. STM32F103 Timer Cookbook
5. STM32F103 HAL and LL Drivers
6. STM32F103 System Memory Boot Mode
7. STM32F103 Flash Memory Programming
8. STM32F103 Errata
9. STM32F103 Bootloader USART Protocols
10. STM32F103 Hardware development
11. CMSIS (Cortex Microcontrollers Software Interface Standard)URL adresa
12. [https://www.youtube.com/watch?v=lxzHzU_byH0]-I made an STM32 Powered Drone!, Aayush Bhansali
13. [https://www.youtube.com/watch?v=Fb3n_CTAc6w]-How to Add MPU 6050, 6500, 9250 Module Library in Proteus 8,  Virtual Simulation Lab

