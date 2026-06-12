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

## K-map Verification (Day 2)

Verified the full adder logic using K-maps.

### Sum
K-map produces a checkerboard pattern (no adjacent 1s) — confirms
Sum = A ⊕ B ⊕ Cin is already minimal; XOR functions can't be
simplified further via K-maps.

### Carry-out
K-map grouping gives:
Cout = AB + BCin + ACin

This matches the gate-level design from Day 1.

### Key learning
XOR-based logic is a worst case for K-map minimization since 1s
are never adjacent — the unsimplified SOP form is already optimal.
