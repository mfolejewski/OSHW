"TaczMi" ("TouchMe") - dedicated push-button on/off controller for Raspberry_Pi

MCU -> ATtiny4 with implemented a simple FSM machine

resistor dividers 1k/2k -> for logic conversion 5V -> 3.3V

logic:

when MOS off:
- short pulse -> turn on MOS

when MOS on:
- short pulse -> ignored
- long pulse or CM4_PWR 1/0 edge -> turn off MOS

Dividers for TPI DAT/CLK/RST can be omitted - use only for ISP directly from CM4 GPIOs (TPI emulation, phyton script).
 
2021-04-26
v1.0: draft -> simple switcher with push button input, CM4 PWR input and drive PMOS switch
