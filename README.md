## Steane Code – Quantum Error Correction

For this repo we follow https://errorcorrectionzoo.org/c/steane

### Overview

The **Steane code** is a fundamental quantum error-correcting code introduced by Andrew Steane in 1996. It is a **[[7,1,3]] CSS code**, meaning:

- It encodes **1 logical qubit** into **7 physical qubits**.
- It can correct **any single-qubit error** (bit-flip, phase-flip, or both).
- It has **distance 3**, detecting up to two errors and correcting one.

---

### How does it work?

The Steane code uses the classical **[7,4,3] Hamming code** to construct a quantum code via the CSS (Calderbank–Shor–Steane) construction.

1. **Encoding**

   The logical qubit is encoded into 7 physical qubits by combining codewords of the classical Hamming code, distributing quantum information across qubits to protect it from errors.

2. **Error Correction**

   - Separate **syndrome measurements** detect **bit-flip (X)** and **phase-flip (Z)** errors using stabilizer generators derived from the classical code’s parity check matrix.
   - Detected errors are corrected by applying the appropriate Pauli operator to restore the encoded logical qubit.

---

### Key properties

- **Transversal gates:** Logical operations can be implemented by applying the same gate to each qubit, enabling fault-tolerant quantum computation.
- **Stabilizer code:** Uses 6 stabilizer generators to define the code space, leaving 1 logical qubit.
- **Widely used** as an example in quantum error correction courses and as a building block for fault-tolerant quantum computing protocols.


### References

- A. Steane, “Error Correcting Codes in Quantum Theory,” *Phys. Rev. Lett.* 77, 793 (1996).
- Nielsen & Chuang, *Quantum Computation and Quantum Information*, Chapter 10.

---
