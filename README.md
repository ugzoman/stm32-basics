# STM32 Basics

Basic STM32 examples using HAL.  
Includes GPIO, PWM, ADC and UART fundamentals.

---

## Examples

### 01_blink_led
- Toggle LED using HAL
- GPIO + HAL_Delay

### 02_pwm_servo
- Servo control with PWM
- Changing duty cycle

### 03_adc_potentiometer
- Read analog input with ADC
- Send data over UART

### 04_uart_printf
- Redirect printf to UART
- Debug output via serial terminal

---

## Toolchain
- STM32CubeIDE  
- HAL Drivers  
- ST-Link Debugger

---

## Blink LED Example
```c
#include "main.h"

int main(void)
{
    HAL_Init();
    SystemClock_Config();
    MX_GPIO_Init();

    while (1)
    {
        HAL_GPIO_TogglePin(GPIOA, GPIO_PIN_5);
        HAL_Delay(500);
    }
}
