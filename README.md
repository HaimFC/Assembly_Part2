# MSP430 Assembly Programming Lab 2

This repository contains the solution to **Lab 2** for MSP430 assembly programming. The lab introduces the use of stack, routines, and macros while developing efficient assembly code for the MSP430 microcontroller. It focuses on translating pseudocode into assembly while ensuring proper stack usage and function execution.

---

## 📋 Description of the Assignment

### Part A: Theoretical Section
1. **The Stack**:
   - Explanation of the stack's purpose and its usage in embedded systems.
2. **Routines**:
   - The concept of routines, their necessity, and their impact on stack operations.
3. **Macros vs. Routines**:
   - Definition of macros, their purpose, and a comparison of their advantages and disadvantages compared to routines.

### Part B: Practical Section
1. **Task Description**:
   - Write an assembly program to compute results using stack-based function calls.
   - Input:
     - Two arrays, each containing eight 16-bit integers, represent two student IDs.
     - A variable `IDsize` representing the array size (type `int`).
     - A variable `num` for storing the result.
   - Output:
     - A computed value `num` based on the function version determined by the last digit of the smaller ID.

2. **Operation Table**:
   Based on the last digit of the smaller ID, the function behavior is selected:
   - `0`: Element-wise multiplication and sum.
   - `1`: Element-wise addition and sum.
   - `2`: Logical OR of elements and sum.
   - `3`: Logical XOR of elements and sum.
   - `4`: Element-wise subtraction and sum.
   - `5`: Maximum of corresponding elements and sum.
   - `6`: Minimum of corresponding elements and sum.
   - `7`: Minimum odd values (default 0 if none) and sum.
   - `8`: Maximum even values (default 0 if none) and sum.
   - `9`: Minimum even values (default 0 if none) and sum.

3. **Program Implementation**:
   - A stack-based approach is used for function calls, ensuring:
     1. Arguments are pushed to the stack before function execution.
     2. Function retrieves arguments from the stack and processes them.
     3. If the function returns a value, it is pushed onto the stack before exiting.
     4. The stack pointer is restored to its original state after the function call.

4. **Simulation Details**:
   - Test the program in the simulator.
   - Record program size and runtime cycle count.
   - Calculate runtime in microseconds using the default clock settings.

---
