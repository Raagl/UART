# UART

A VHDL-based UART system that receives a byte, increments it, and sends it back.

## :rocket: Key features

1) **Multi Baud rate**: tx_mod and rx_mod use a CLK_PER_BIT generic to support any baud rate.
2) **Reliable RX**: Implements center-sampling and metastability synchronizers.
3) **Visual Debugging**: The top module uses the 7-segment display to show the hex value of processed data.

## How to use

1) Set CLK_PER_BIT to match your baud rate (default: 434 for 230400 bps @ 100MHz).
2) Connect to the Basys 3 via USB-UART.
3) Send a byte; the FPGA returns byte + 1 and displays it.