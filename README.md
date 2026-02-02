Ternary-Steel-Seed Protocol (9-3-1)
​A ultra-compact, DIY BIP39 cold storage protocol that uses Incomplete Ternary Logic to store seed phrases on stainless steel plates.
​Description
​This method encodes each letter of a BIP39 word (first 4 letters) into 3 weighted positions (9, 3, 1) using a "Mark-on-Presence" system. Unlike binary which requires 5 slots, this ternary-inspired approach uses dual sub-slots to represent the values 0, 1, and 2, achieving high data density with manual tools (center punch and hammer).
​The Logic: Weighted Ternary (Base-3)
​Each letter is assigned a decimal index (A=0, Z=25). To store this value, we use three weights: 9, 3, and 1.
​Each weight has two physical slots: Slot A (Value 1) and Slot B (Value 2).
​Value 0: No holes.
​Value 1: Punch Slot A.
​Value 2: Punch Slot B.
​Mathematical Formula:
Letter Index = (Weight 9 * SlotValue) + (Weight 3 * SlotValue) + (Weight 1 * SlotValue)
​Mapping Table (A-Z)
​| Letter | Index | 9 (A|B) | 3 (A|B) | 1 (A|B) | Letter | Index | 9 (A|B) | 3 (A|B) | 1 (A|B) |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| A | 0 | 0 | 0 | 0 | 0 | 0 | 0 | N | 13 | 1 | 0 | 1 | 0 | 1 | 0 |
| B | 1 | 0 | 0 | 0 | 0 | 1 | 0 | O | 14 | 1 | 0 | 1 | 0 | 0 | 1 |
| P | 2 | 0 | 0 | 0 | 0 | 0 | 1 | P | 15 | 1 | 0 | 0 | 1 | 0 | 0 |
| D | 3 | 0 | 0 | 1 | 0 | 0 | 0 | Q | 16 | 1 | 0 | 0 | 1 | 1 | 0 |
| E | 4 | 0 | 0 | 1 | 0 | 1 | 0 | R | 17 | 1 | 0 | 0 | 1 | 0 | 1 |
| F | 5 | 0 | 0 | 1 | 0 | 0 | 1 | S | 18 | 0 | 1 | 0 | 0 | 0 | 0 |
| G | 6 | 0 | 0 | 0 | 1 | 0 | 0 | T | 19 | 0 | 1 | 0 | 0 | 1 | 0 |
| H | 7 | 0 | 0 | 0 | 1 | 1 | 0 | U | 20 | 0 | 1 | 0 | 0 | 0 | 1 |
| I | 8 | 0 | 0 | 0 | 1 | 0 | 1 | V | 21 | 0 | 1 | 1 | 0 | 0 | 0 |
| J | 9 | 1 | 0 | 0 | 0 | 0 | 0 | W | 22 | 0 | 1 | 1 | 0 | 1 | 0 |
| K | 10 | 1 | 0 | 0 | 0 | 1 | 0 | X | 23 | 0 | 1 | 1 | 0 | 0 | 1 |
| L | 11 | 1 | 0 | 0 | 0 | 0 | 1 | Y | 24 | 0 | 1 | 0 | 1 | 0 | 0 |
| M | 12 | 1 | 0 | 1 | 0 | 0 | 0 | Z | 25 | 0 | 1 | 0 | 1 | 1 | 0 |
​Grid Layout (Visual Example)
​1. Empty Grid (Per Word)
​Each word contains 4 letters (L1-L4). Each letter has 3 weight columns (9, 3, 1), each with 2 sub-slots (A, B).
