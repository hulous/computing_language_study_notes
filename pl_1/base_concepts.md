# Main Concepts of the PL/I Programming Language

## 🔹 1. Purpose and History
- **PL/I** (Programming Language One) was developed in the 1960s by IBM.
- Intended as a **general-purpose language** combining features of COBOL (business) and FORTRAN (scientific).
- Used in **business, scientific, and systems programming**.

---

## 🔹 2. Multi-Paradigm Support
- Supports **procedural**, **structured**, and **imperative** programming styles.
- Combines features from both **business and scientific computing**.

---

## 🔹 3. Data Types and Structures
- Rich set of **built-in types**: FIXED, FLOAT, COMPLEX, CHARACTER, BIT, PICTURE.
- Support for **structures (records)**, **arrays**, and **unions**.
- Strong typing with flexibility to mix types safely.

  **Example:**
  ```pli
  DECLARE X FIXED DECIMAL(5,2);
  DECLARE NAME CHAR(20);
  ```

---

## 🔹 4. Exception and Condition Handling
- PL/I has a powerful **condition handling mechanism** similar to modern exception handling.
- Supports ON-units for handling specific conditions (e.g., `ON ZERODIVIDE`, `ON ENDFILE`).

  **Example:**
  ```pli
  ON ZERODIVIDE BEGIN;
     PUT SKIP LIST('Division by zero');
     STOP;
  END;
  ```

---

## 🔹 5. Input/Output Flexibility
- Highly flexible **I/O system** with formats and file control similar to COBOL and FORTRAN.
- Support for **sequential, direct access**, and **formatted/unformatted I/O**.

---

## 🔹 6. Concurrency and Tasking
- PL/I includes **multitasking support** with tasks, events, and semaphores.
- Rare among early high-level languages.

---

## 🔹 7. Compile-Time Features
- Includes **preprocessor directives**, **macros**, and **conditional compilation**.
- Allows **meta-programming** and **configurable builds**.

---

## 🔹 8. Portability and Versatility
- Designed to be portable across IBM systems.
- Used in mainframe systems and early system software projects.

---

## ✅ Simple PL/I Example
```pli
HELLO: PROCEDURE OPTIONS(MAIN);
  PUT SKIP LIST('Hello, PL/I!');
END HELLO;
```
