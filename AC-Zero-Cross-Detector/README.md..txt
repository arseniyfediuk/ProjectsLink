# AC Zero-Cross Detector

This repository contains the design, calculations, and physical testing data for a zero-crossing detector node used in a solid-state AC power phase control device. The circuit safely monitors the 230V/50Hz mains and generates accurate synchronization pulses for a microcontroller, enabling power switching exactly at the zero-crossing point to minimize electromagnetic interference.

Technical Details
Core Component: PC814 (LTV-814S-A) bidirectional optocoupler, allowing direct AC monitoring without the need for an external diode bridge
Galvanic Isolation: Safely separates the 220V AC high-voltage side from the sensitive 5V microcontroller logic
Input Stage: Utilizes two 50 kΩ (2W) through-hole current-limiting resistors in series to handle peak voltages up to 325V and safely dissipate thermal load
Output Signal: Generates 5V logic pulses (approximately 1ms in width) at every zero crossing, resulting in 100 pulses per second
Software Integration: Optimized for microcontroller hardware interrupts (FALLING edge) with a 2ms software debounce filter to eliminate high-frequency noise.