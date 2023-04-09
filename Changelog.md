# Changes

## V1.3

- Added debouncing circuits to encoder and button
- Added switching transistor to buzzer circuit
- C3 and C4 are now a smaller package and more cost effective
- Added basic voltage divider to GPIO35 for voltage sensing (experimental) 

## V1.2

- Fixed incorrect GPS RX and TX pins (swapped)
- Upgraded 5V regulator to 1.5A instead of 1A
- Discovered buzzer does not work, found trace not connected at ESP32 GPIO26. Fixed mistake in routing.

## V1.1

- Moved all surface mount components (other than RF Module) to the same side of the board for single sided assembly using an assembly service such as JLCPCB.
- Moved decoupling caps closer to their loads
