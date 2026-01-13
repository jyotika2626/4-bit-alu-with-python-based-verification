# 4-bit-alu-with-python-based-verification

# 📌 Project Overview
This project implements a 4-bit Arithmetic Logic Unit (ALU) using Verilog HDL and verifies its functionality using Python-generated test vectors.  
The design is simulated on EDA Playground, and correctness is validated through file-based verification and waveform analysis (VCD).

# ⚙️ ALU Features
The 4-bit ALU supports the following operations based on a 3-bit opcode:

| Opcode | Operation |
|------|----------|
| 000 | Addition (A + B) |
| 001 | Subtraction (A − B) |
| 010 | Bitwise AND |
| 011 | Bitwise OR |
| 100 | Bitwise XOR |

- Input width: 4 bits
- Output width: 4 bits
- Overflow handled by truncation (modulo 16)



# 🧠 Design Description

# Verilog ALU Module
- Combinational logic using `always @(*)`
- `case` statement used for opcode-based operation selection
- Output updates immediately with input change

# Testbench
- Reads input vectors from a text file (`input.txt`)
- Applies inputs to ALU
- Captures output into `output.txt`
- Displays results in simulation console
- Generates **VCD waveform** for timing and logic verification

# 🐍 Python-Based Verification
A Python script is used to:
- Generate random ALU test cases
- Ensure the same logic as the Verilog ALU
- Save test vectors in `input.txt`
- Provide cross-verification between software and hardware models

This approach mimics real-world hardware verification workflows.




