# RTC-alarm-wakeup-for-bluepill-STM32f103-

This repository contains the project for BluePill (i.e STM32f103) board, the projects does the task to put the controller in Low power mode (i.e Stop mode or Standby mode) and the wake up from the low power mode after specific time intervals continously. 
The STM32F103 does not have an wakeup timer functionality, so to put the controller to low power mode and to wake it up from low power mode I configure RTC alarm as a timer.
To configure RTC alarm to timer I set the RTC time to 00:00:00 (hrs:min:sec) and set the alarm for the time intervals I needed, and then after the alarm interrupt occurs I had reset the RTC time to 00:00:00 (hrs:min:sec) and same goes again and again in a loop.
The following code can also set different timing (alarm) interval for putting into sleep and waking it from sleep.
