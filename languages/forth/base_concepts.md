# Main Concepts of the FORTH Programming Language

## 🔹 1. Stack-Based Language
- FORTH uses a **data stack** to perform operations.
- **Operands** are pushed onto the stack, and **operators** consume values from the top of the stack.

  **Example:**
  ```forth
  3 4 +   \ pushes 3 and 4, then adds them → stack contains 7
  ```

---

## 🔹 2. Postfix Notation (Reverse Polish Notation - RPN)
- Expressions are written in **postfix notation**: operands first, then the operator.

  **Example:**
  ```forth
  2 5 *   \ equivalent to 2 * 5 in infix notation
  ```

---

## 🔹 3. Concatenative Language
- FORTH is a **concatenative language**: programs are created by **chaining words** (functions or commands).
- Each word operates on the **implicit stack**.

---

## 🔹 4. Defining Words (Functions)
- The `:` keyword defines a **new word** (function):

  **Example:**
  ```forth
  : SQUARE ( n -- n² ) DUP * ;
  ```
  - `DUP` duplicates the top of the stack.
  - `*` multiplies the top two values on the stack.

---

## 🔹 5. Built-in Interpreter and Compiler
- FORTH works in two modes:
  - **Interpretation mode**: immediate execution.
  - **Compilation mode**: defining new words.
- Enables **direct and interactive** control of the system.

---

## 🔹 6. Minimalist and Extensible
- The **core of FORTH is small and minimal**.
- Users can define new words to build **domain-specific languages**.
- Offers **low-level control** over the system.

---

## 🔹 7. Portability and Efficiency
- FORTH is **lightweight** and **fast**.
- Popular in **embedded systems**, and used by organizations like **NASA**.

---

## 🔹 8. Comments and Conventions
- Comments are enclosed in parentheses:
  ```forth
  ( This is a comment )
  ```

---

## ✅ Complete Example
```forth
: CUBE ( n -- n³ ) DUP DUP * * ;
5 CUBE .   \ Outputs 125
```
