# Intro Circuits

## 2-bit Adder (Paper Design)
Designed a 2-bit adder using logic gates only (XOR, AND, OR).

### Inputs
- A, B → first 2-bit number (A=MSB, B=LSB)
- C, D → second 2-bit number (C=MSB, D=LSB)

### Outputs
- S0 = B XOR D (LSB of sum)
- S1 = (A XOR C) XOR (B AND D) (MSB of sum)
- Carry = (A AND C) OR ((A XOR C) AND (B AND D))

### Key learnings
- Half adder handles LSB (no carry-in)
- Full adder handles MSB (carry-in from previous stage)
- Carry ripples from bit 0 to bit 1
