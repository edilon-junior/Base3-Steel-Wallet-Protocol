# Ternary-Steel-Seed Protocol (9-3-1)

A ultra-compact, DIY BIP39 cold storage protocol using **Incomplete Ternary Logic** to store seed phrases on stainless steel plates.

## Description
Each letter of a BIP39 word is encoded into 3 weighted positions (**9, 3, 1**). This approach uses dual sub-slots per weight to represent values 0, 1, and 2.

---

## The Logic: Weighted Ternary
Each letter has a decimal index (A=0, Z=25).
* **Weight 9, 3, 1**: Three columns of storage.
* **Slot A**: Value 1.
* **Slot B**: Value 2.
* **Empty**: Value 0.

**Formula:** `Index = (W9 * SlotValue) + (W3 * SlotValue) + (W1 * SlotValue)`

---

## Mapping Table (A-Z)

| Letter | Index | 9 (A\|B) | 3 (A\|B) | 1 (A\|B) | Letter | Index | 9 (A\|B) | 3 (A\|B) | 1 (A\|B) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **A** | 0 | 0 \| 0 | 0 \| 0 | 0 \| 0 | **N** | 13 | 1 \| 0 | 1 \| 0 | 1 \| 0 |
| **B** | 1 | 0 \| 0 | 0 \| 0 | 1 \| 0 | **O** | 14 | 1 \| 0 | 1 \| 0 | 0 \| 1 |
| **C** | 2 | 0 \| 0 | 0 \| 0 | 0 \| 1 | **P** | 15 | 1 \| 0 | 0 \| 1 | 0 \| 0 |
| **D** | 3 | 0 \| 0 | 1 \| 0 | 0 \| 0 | **Q** | 16 | 1 \| 0 | 0 \| 1 | 1 \| 0 |
| **E** | 4 | 0 \| 0 | 1 \| 0 | 1 \| 0 | **R** | 17 | 1 \| 0 | 0 \| 1 | 0 \| 1 |
| **F** | 5 | 0 \| 0 | 1 \| 0 | 0 \| 1 | **S** | 18 | 0 \| 1 | 0 \| 0 | 0 \| 0 |
| **G** | 6 | 0 \| 0 | 0 \| 1 | 0 \| 0 | **T** | 19 | 0 \| 1 | 0 \| 0 | 1 \| 0 |
| **H** | 7 | 0 \| 0 | 0 \| 1 | 1 \| 0 | **U** | 20 | 0 \| 1 | 0 \| 0 | 0 \| 1 |
| **I** | 8 | 0 \| 0 | 0 \| 1 | 0 \| 1 | **V** | 21 | 0 \| 1 | 1 \| 0 | 0 \| 0 |
| **J** | 9 | 1 \| 0 | 0 \| 0 | 0 \| 0 | **W** | 22 | 0 \| 1 | 1 \| 0 | 1 \| 0 |
| **K** | 10 | 1 \| 0 | 0 \| 0 | 1 \| 0 | **X** | 23 | 0 \| 1 | 1 \| 0 | 0 \| 1 |
| **L** | 11 | 1 \| 0 | 0 \| 0 | 0 \| 1 | **Y** | 24 | 0 \| 1 | 0 \| 1 | 0 \| 0 |
| **M** | 12 | 1 \| 0 | 1 \| 0 | 0 \| 0 | **Z** | 25 | 0 \| 1 | 0 \| 1 | 1 \| 0 |

---

## Grid Layout (Visual Example)

### 1. Empty Grid (Per Word)

```text
 WORD 01   |   WEIGHT 9  |   WEIGHT 3  |   WEIGHT 1  |
-----------|-------------|-------------|-------------|
 SUB-SLOTS |  A  |  B    |  A  |  B    |  A  |  B    |
-----------|-----|-------|-----|-------|-----|-------|
 LETTER 1  | [ ] | [ ]   | [ ] | [ ]   | [ ] | [ ]   |
 LETTER 2  | [ ] | [ ]   | [ ] | [ ]   | [ ] | [ ]   |
 LETTER 3  | [ ] | [ ]   | [ ] | [ ]   | [ ] | [ ]   |
 LETTER 4  | [ ] | [ ]   | [ ] | [ ]   | [ ] | [ ]   |
-----------|-----|-------|-----|-------|-----|-------|
