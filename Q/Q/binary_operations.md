# Mathematical Binary Operations and CPU Physical Execution

## A. All Mathematical Binary Operations

A **binary operation** is any function that takes two inputs and
produces one output:

    ★ : S × S → S

There is *no finite list*, since any rule of two variables qualifies.\
But common categories include:

### 1. Arithmetic Operations

-   a + b
-   a - b
-   a × b
-   a / b
-   a \^ b

### 2. Modular Arithmetic

-   a mod b
-   (a + b) mod n
-   (a × b) mod n

### 3. Boolean / Logical Operations

-   AND: a ∧ b
-   OR: a ∨ b
-   XOR: a ⊕ b
-   NAND: ¬(a ∧ b)
-   NOR: ¬(a ∨ b)

### 4. Bitwise Operations

-   a & b
-   a \| b
-   a \^ b
-   a \<\< b
-   a \>\> b

### 5. Algebraic Structure Operations

-   Group operation: a ∘ b
-   Ring operations: a + b, ab
-   Vector addition: u + v
-   Matrix multiplication: AB

------------------------------------------------------------------------

## B. What CPUs Physically Execute

CPUs do **not** directly "perform math" the way humans imagine.\
Everything ultimately comes from **transistor-level logic**.

### Primitive Operations CPUs Are Built From

-   NAND
-   NOR
-   NOT (inverters)
-   Transmission gates
-   Voltage comparators

These are enough to build any logic system.

### Common ALU Operations (Built From Those Gates)

-   Integer addition (ripple carry, carry-lookahead)
-   Subtraction (two's complement)
-   Multiplication (shifts + adds)
-   Bitwise AND/OR/XOR
-   Bit shifts
-   Comparisons
-   Floating-point operations

All reduce to transistor networks.

### Memory Operations

-   Writing a bit (charging/discharging a capacitor or flipping a
    latch)\
-   Reading a bit (detecting stored charge or latch state)

------------------------------------------------------------------------

## C. What Hardware Actually Does (Voltage & Current)

Computers operate purely through **electrical signals**, not symbolic
math.

### Binary Encoding

-   **0** → low voltage
-   **1** → high voltage

Exact values vary by semiconductor process.

### Transistor Physics

A MOSFET acts as a **voltage-controlled switch**: - Gate voltage \>
threshold → current flows (output = 1)\
- Gate voltage \< threshold → no current (output = 0)

### Logic Gate Construction

Networks of MOSFETs create: - AND
- OR
- XOR
- NOT
- NAND (the universal gate n+1) 
- NOR (the universal gate n+1)

### Adders

A full adder implements:

    sum = a ⊕ b ⊕ carry_in
    carry_out = (a ∧ b) ∨ (carry_in ∧ (a ⊕ b))

Physically: XOR, AND, OR circuits built from MOSFETs.

### Multiplication

Implemented using: - shifts (rewiring)
- repeated addition (adder circuits)

### Floating-Point Units

Built from: - shifters
- comparators
- adders
- multipliers

All still based on transistor logic.

------------------------------------------------------------------------

# Summary

### Mathematical Level

Any function of two inputs is a binary operation.

### Computational Level

CPUs execute: - Logic (AND/OR/XOR)
- Arithmetic (add/sub/multiply)
- Bit shifts
- Comparisons
- Memory operations

### Physical Level

The CPU only manipulates: - **voltages**
- **currents**
through billions of **transistors** acting as switches.
