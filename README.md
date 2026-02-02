# Ternary-Steel-Seed Protocol (9-3-1)

A ultra-compact, DIY BIP39 cold storage protocol using **Incomplete Ternary Logic** to store seed phrases on stainless steel plates.

## Description
Each letter is encoded into a 3-digit Ternary string based on weights **9, 3, and 1**. This allows representing letters A-Z (indices 0-25) with only 3 positions.

---

## The Logic: Weighted Ternary
Each letter has a decimal index (A=0, Z=25). We use a 3-digit code where each digit can be **0, 1, or 2**.

* **Value 0:** No holes.
* **Value 1:** Punch **MULTIPLIER 1**.
* **Value 2:** Punch **MULTIPLIER 2**.

**Formula:** `Index = (Digit1 * 9) + (Digit2 * 3) + (Digit3 * 1)`

---

## Simplified Mapping Table (A-Z)

| Letter | Index | Ternary (9-3-1) | Letter | Index | Ternary (9-3-1) |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **A** | 0 | **000** | **N** | 13 | **111** |
| **B** | 1 | **001** | **O** | 14 | **112** |
| **C** | 2 | **002** | **P** | 15 | **120** |
| **D** | 3 | **010** | **Q** | 16 | **121** |
| **E** | 4 | **011** | **R** | 17 | **122** |
| **F** | 5 | **012** | **S** | 18 | **200** |
| **G** | 6 | **020** | **T** | 19 | **201** |
| **H** | 7 | **021** | **U** | 20 | **202** |
| **I** | 8 | **022** | **V** | 21 | **210** |
| **J** | 9 | **100** | **W** | 22 | **211** |
| **K** | 10 | **101** | **X** | 23 | **212** |
| **L** | 11 | **102** | **Y** | 24 | **220** |
| **M** | 12 | **110** | **Z** | 25 | **221** |

---

## Grid Layout (Visual Example)

### 1. Punched Example: Word "BALL" (B-A-L-L)
* **B** (001) | **A** (000) | **L** (102) | **L** (102)

```text
 WORD 01   |   WEIGHT 9  |   WEIGHT 3  |   WEIGHT 1  |
-----------|-------------|-------------|-------------|
 MULTIPLIER|  1  |  2    |  1  |  2    |  1  |  2    |
-----------|-----|-------|-----|-------|-----|-------|
 L1 (B:001)| [ ] | [ ]   | [ ] | [ ]   | [*] | [ ]   |
 L2 (A:000)| [ ] | [ ]   | [ ] | [ ]   | [ ] | [ ]   |
 L3 (L:102)| [*] | [ ]   | [ ] | [ ]   | [ ] | [*]   |
 L4 (L:102)| [*] | [ ]   | [ ] | [ ]   | [ ] | [*]   |
-----------|-----|-------|-----|-------|-----|-------|
```
so for letter letter B we have that the index is 9x0 + 3x0 + 1x1, resulting 1.
















