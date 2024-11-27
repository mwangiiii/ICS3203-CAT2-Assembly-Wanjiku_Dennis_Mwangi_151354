# Assembly Program - Control Flow and Logic Tasks

## 1. Control Flow and Conditional Logic

### Task Description:
This program prompts the user to input a number and then classifies it as "POSITIVE," "NEGATIVE," or "ZERO." It uses **branching logic** to determine the classification.

### Steps:
- The program asks for user input.
- It compares the number using conditional jumps (`je`, `jg`, `jl`).
- Based on the comparison, it branches to either the "POSITIVE," "NEGATIVE," or "ZERO" section and prints the appropriate classification.
  
### Key Concepts:
- **Conditional Jumps**: These are used to handle different conditions (`je` for equality, `jg` for greater than, `jl` for less than) to control the flow.
- **Unconditional Jumps**: These allow the program to jump to specific labels or sections of code without conditions, ensuring proper flow after classification.

### Explanation of Jumps:
- `je` (jump if equal) is used to check if the number is zero.
- `jg` (jump if greater) is used to check if the number is positive.
- `jl` (jump if less) is used to check if the number is negative.

---

## 2. Array Manipulation with Looping and Reversal

### Task Description:
This program accepts an array of 5 integers from the user, reverses the array in place without using extra memory, and outputs the reversed array.

### Steps:
- The program accepts 5 integers as input.
- It uses a **loop** to reverse the array in place by swapping elements.
- The reversed array is printed at the end.

### Key Concepts:
- **In-Place Reversal**: The reversal is done without using additional memory by directly swapping elements in the original array.
- **Looping**: A loop is used to iterate over the array and perform the swaps in a systematic way.

### Challenges:
- Handling array reversal without additional memory can be tricky, especially when manipulating values directly in the array.
- The loop ensures that the first element is swapped with the last, the second with the second-to-last, and so on, ensuring the array is reversed without extra space.

---

## 3. Modular Program with Subroutines for Factorial Calculation

### Task Description:
This program computes the factorial of a number entered by the user using a subroutine to perform the calculation.

### Steps:
- The program accepts a number as input.
- A **subroutine** is called to calculate the factorial.
- The result is placed in a register and printed.

### Key Concepts:
- **Subroutines**: The factorial calculation is done in a separate code block (subroutine), demonstrating modular programming.
- **Stack Management**: The stack is used to save registers and preserve values during the execution of the subroutine.

### Explanation of Register Management:
- Registers are saved on the stack before calling the subroutine and restored afterward. This ensures that the program's state is maintained across subroutine calls.
  
---

## 4. Data Monitoring and Control Using Port-Based Simulation

### Task Description:
This program simulates a control system where it reads a **sensor value** (e.g., water level) from a specified memory location and performs actions based on the input, such as turning on a motor or triggering an alarm.

### Steps:
- The program reads a "sensor value" from a specified location.
- Based on the sensor value:
  - If the water level is too high, it triggers an alarm.
  - If the water level is moderate, it stops the motor.

### Key Concepts:
- **Memory-based Simulation**: The program reads input from a simulated sensor value, which could represent any type of system data.
- **Control Actions**: It then uses conditional checks to determine the actions to take, such as setting bits to turn on the motor or triggering an alarm.

### Explanation of Control Flow:
- If the sensor value indicates a high water level, the program sets a bit to turn on the motor and triggers an alarm.
- If the water level is moderate, the program stops the motor.
- Memory addresses or locations are used to simulate input and output actions (such as turning on the motor or triggering the alarm).

---

## Documentation Guidelines:

For each section, **commenting** is essential to explain the key steps in your code. The comments should:
1. Explain the purpose of each instruction, particularly **conditional and unconditional jumps**.
2. Describe how arrays and loops are used to manipulate data efficiently.
3. Provide insights into how **subroutines** help in modularizing the program.
4. Document how data input/output is simulated, especially when dealing with control programs or memory-based actions.

---

## How to Run:
1. Assemble the code using the assembler for your platform (e.g., `nasm`).
   -    for conditional logic and control flow program - task 1:
   ```
   nasm -f elf64 -g -o conditional_logic_and_control_flow_program.o conditional_logic_and_control_flow program.asm
   ```
   
   -    for second program for array manipulation:
   ```
   nasm -f elf64 -g -o array_manipulation.o array_manipaulation.asm
   ```
   
   -    for third program for factorial calculation
   ```
   nasm -f elf64 -g -o factorial_calculation.o factorial_calculation.asm
   ```
   
   -    for fourth program for data monitoring
   ```
   nasm -f elf64 -g -o data_monitoring.o data_monitoring.asm
   ```
   
3. Link the object files to create an executable.

   -   for the first task:
     
    ```
    ld -o conditional_logic_and_control_flow_program conditional_logic_and_control_flow_program.o
    ```

    -   for the second task:
      
    ```
    ld -o array_manipulation array_manipulation.o
    ```

    -   for the third task:
      
    ```
    ld -o factorial_calculation factorial_calculation.o
    ```

    -   for the fourth task:
      
    ```
    ld -o data_monitoring data_monitoring.o
    ```

5. Run the program in a terminal, and provide the required inputs as prompted.

   -   for the first task:
     
   ```
   ./conditional_logic_and_control_flow_program
   ```

   -   for the second task:
     
   ```
   ./array_manipulation
   ```

   -   for the third task:
   
   ```
   ./factorial_calculation
   ```

   -   for the fourth task:
     
   ```
   ./data_monitoring
   ```
   

---

