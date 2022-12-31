# A3T1 STM32F407VET6 UART Hello World

**Assignment Description:** Read 4 Way DIP switch and print the status in putty terminal via UART communication

**Group Name:** Smart Dolphins\
**Owners:** Veknes Benjaman; Saw Jun Chao

**Source Code:** [main.c](/A3T1_STM32F407VET6_UART/Core/Src/main.c)

## Descriptions on Board and Microcontroller

**STM32 development board model:** STM32F4VE\
**Microcontroller:** STM32F407VET6\
**Core:** ARM Cortex-M4

## GPIO Pins Configuration, Components and Code Functions

[1] Pinout configuration in STM32CubeIDE

- PA9 configured as USART1_TX and Asynchronous mode
- PA10 configured as USART1_RX and Asynchronous mode
- PC0 to PC3 configured as GPIO_Input and GPIO_PULLDOWN

[2] Components

- YP-01 USB to TTL module for UART communication
- 4 Way DIP Switch

<center><img src="/pictures/schematics.png"></center>

[3] Code function

HAL_Delay(Delay) : Creates delay (in ms)\
GPIOC->IDR : Input data register\
HAL_UART_Transmit : Transmit data to UART

[4] Putty terminal configuration

- Serial line number may change (can be checked through Windows Device Manager)
- The other configuration are set based on configuration set in STM32CubeIDE

<center><img src="/pictures/putty_configuration.png"></center>

## Putty Terminal Output

<center><img src="/pictures/putty_terminal_output.png"></center>

## References

[1] Board Details and Schematics:\
[https://stm32-base.org/boards/STM32F407VET6-STM32-F4VE-V2.0.html](https://stm32-base.org/boards/STM32F407VET6-STM32-F4VE-V2.0.html)\
[2] STM32CubeIDE Tutorial:\
[https://www.st.com/resource/en/user_manual/um2609-stm32cubeide-user-guide-stmicroelectronics.pdf](https://www.st.com/resource/en/user_manual/um2609-stm32cubeide-user-guide-stmicroelectronics.pdf)\
[https://www.youtube.com/playlist?list=PLnMKNibPkDnFCosVVv98U5dCulE6T3Iy8](https://www.youtube.com/playlist?list=PLnMKNibPkDnFCosVVv98U5dCulE6T3Iy8)\
[3] Previous Assignment:\
[https://github.com/SawJunChao/stm32blinky](https://github.com/SawJunChao/stm32blinky)\
[https://github.com/SawJunChao/stm32morse](https://github.com/SawJunChao/stm32morse)\
[https://github.com/veknes/stm32knightrider](https://github.com/veknes/stm32knightrider)\
[https://github.com/veknes/stm32switchread](https://github.com/veknes/stm32switchread)\
[4] UART STM32 Configuration:\
[https://wiki.st.com/stm32mcu/wiki/STM32StepByStep:Step3_Introduction_to_the_UART](https://wiki.st.com/stm32mcu/wiki/STM32StepByStep:Step3_Introduction_to_the_UART)\
[https://deepbluembedded.com/stm32-usart-uart-tutorial/](https://deepbluembedded.com/stm32-usart-uart-tutorial/)\
[https://controllerstech.com/uart-transmit-in-stm32/](https://controllerstech.com/uart-transmit-in-stm32/)