# Main Concepts of the Ada Programming Language

## 🔹 1. Strongly Typed Language
- **Ada is strongly typed**: each variable has a specific type, reducing runtime errors.
- Supports **enumerated types**, **derived types**, and **constrained types**.

  **Example:**
  ```ada
  type Week_Day is (Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday);
  ```

---

## 🔹 2. Safety and Reliability
- Designed for **critical systems** (aerospace, defense, space).
- Performs **strict compile-time and runtime checks** (range checks, overflows, etc.).

---

## 🔹 3. Modularity with Packages
- Code is organized using **packages**.
- A package consists of:
  - a **specification** (interface)
  - a **body** (implementation)

  **Example:**
  ```ada
  package Maths is
     function Square (X : Integer) return Integer;
  end Maths;

  package body Maths is
     function Square (X : Integer) return Integer is
     begin
        return X * X;
     end Square;
  end Maths;
  ```

---

## 🔹 4. Exception Handling
- Robust **error handling** through **exceptions**.

  **Example:**
  ```ada
  begin
     -- code
  exception
     when Constraint_Error =>
        -- error handling
  end;
  ```

---

## 🔹 5. Concurrency (Parallelism)
- Native support for **multitasking** using **tasks**, **rendezvous**, and **protected objects**.
- Enables **deterministic concurrent programming**.

  **Example:**
  ```ada
  task type Sensor is
     entry Read;
  end Sensor;
  ```

---

## 🔹 6. Contracts (Ada 2012+)
- Supports **preconditions, postconditions, and invariants**.
- Encourages **design by contract**.

  **Example:**
  ```ada
  function Root (X : Float) return Float
    with Pre => X >= 0.0,
         Post => Root'Result ** 2 <= X;
  ```

---

## 🔹 7. Portability and Standards
- **ISO/IEC standardized** language.
- Well-suited for **real-time** and **embedded systems**.

---

## 🔹 8. Clear and Readable Syntax
- Inspired by **Pascal**, with **explicit structure** (no braces).
- Encourages **readable and maintainable code**.

---

## ✅ Simple Example in Ada
```ada
procedure Hello is
begin
   Put_Line("Hello, Ada!");
end Hello;
```
