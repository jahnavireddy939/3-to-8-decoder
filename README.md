# 3-to-8 Decoder using Verilog

## Overview

This project implements a **3-to-8 Decoder** using Verilog HDL. The decoder converts a 3-bit binary input into one of eight active-high output lines.

## Truth Table

| A2 | A1 | A0 | Active Output |
|----|----|----|---------------|
| 0 | 0 | 0 | Y0 |
| 0 | 0 | 1 | Y1 |
| 0 | 1 | 0 | Y2 |
| 0 | 1 | 1 | Y3 |
| 1 | 0 | 0 | Y4 |
| 1 | 0 | 1 | Y5 |
| 1 | 1 | 0 | Y6 |
| 1 | 1 | 1 | Y7 |

## Inputs

- `A[2:0]` – 3-bit binary input

## Outputs

- `Y[7:0]` – One active-high output corresponding to the input value

## Project Structure

```
3to8-decoder-verilog/
├── src/
├── tb/
├── sim/
├── images/
└── README.md
```

## Simulation

Compile:

```bash
iverilog -o decoder src/decoder3to8.v tb/decoder3to8_tb.v
```

Run:

```bash
vvp decoder
```

View the waveform:

```bash
gtkwave decoder3to8.vcd
```

## Applications

- Memory address decoding
- Instruction decoding
- Chip select generation
- Digital control systems
- FPGA and ASIC designs

## License

MIT License