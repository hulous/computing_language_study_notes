# Main Concepts of the Fortran Programming Language

## 🔹 1. Purpose and Origin
- **Fortran** (Formula Translation) is one of the oldest high-level programming languages, developed in the 1950s.
- Designed for **scientific and numerical computing**, especially in fields like physics, engineering, and climate modeling.

---

## 🔹 2. Syntax and Structure
- Fortran code is structured around **program units** such as:
  - `program`, `subroutine`, `function`, `module`
- Case-insensitive and **column-sensitive** in older versions (e.g., Fortran 77).
- Modern Fortran (90/95/2003/2008/2018) uses **free-form source format**.

  **Example:**
  ```fortran
  program hello
    print *, "Hello, Fortran!"
  end program hello
  ```

---

## 🔹 3. Strong Support for Numerical Computation
- Native support for **complex numbers**, **real and double precision**, **arrays**, and **mathematical functions**.

  **Example:**
  ```fortran
  real :: a, b, result
  result = sqrt(a**2 + b**2)
  ```

---

## 🔹 4. Arrays and Matrix Operations
- Built-in array handling and operations without explicit loops.
- Modern Fortran supports **whole-array operations** and **array slicing**.

  **Example:**
  ```fortran
  real :: A(10), B(10)
  A = B + 5.0
  ```

---

## 🔹 5. Modularity with Modules
- **Modules** allow grouping of related procedures, types, and variables.
- Encourages **modular and reusable code**.

  **Example:**
  ```fortran
  module math_utils
    contains
    function square(x)
      real :: square, x
      square = x * x
    end function square
  end module math_utils
  ```

---

## 🔹 6. Procedures and Interfaces
- Supports **subroutines** and **functions**.
- Interfaces allow **procedure overloading** and **generic programming**.

---

## 🔹 7. Parallel and High-Performance Computing
- Fortran is widely used in **HPC (High Performance Computing)**.
- Modern standards support:
  - **Coarrays** for parallel programming
  - **OpenMP** and **MPI** for shared/distributed memory

---

## 🔹 8. Type Safety and Derived Types
- Fortran 90+ includes **user-defined types** (similar to structs).

  **Example:**
  ```fortran
  type :: Point
    real :: x, y
  end type Point
  ```

---

## ✅ Simple Fortran Program Example
```fortran
program sum_example
  real :: a, b, result
  a = 3.0
  b = 4.0
  result = a + b
  print *, "Sum is", result
end program sum_example
```