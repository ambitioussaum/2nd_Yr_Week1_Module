# 2nd_Yr_Week1_Module
Handwritten notes, programming codes, and execution proofs for Week 1 Module  (Syntax,Conditions, an d Loops in C and C++).
# C & C++ Pattern Printing Solutions 🚀
This repository contains structured logic, approaches, and detailed hand-written style dry runs for 8 fundamental star pattern-printing problems in C and C++. Master these nested loop logic patterns to build a rock-solid foundation in programming control flow.

---

## 📖 Table of Contents
* [About the Module](#-about-the-module)
* [Pattern Implementations](#-pattern-implementations)
  * [1. Square](#1-square)
  * [2. Hollow Square](#2-hollow-square)
  * [3. Triangle](#3-triangle)
  * [4. Inverted Triangle](#4-inverted-triangle)
  * [5. Pyramid](#5-pyramid)
  * [6. Inverted Pyramid](#6-inverted-pyramid)
  * [7. Half Diamond](#7-half-diamond)
  * [8. Diamond](#8-diamond)
* [Core Concepts Learned](#-core-concepts-learned)

---

## 🧐 About the Module
Pattern printing is a classic approach used to build strong foundational skills in handling **nested loops** and dynamic conditional rendering[span_0](start_span)[span_0](end_span). The repository systematically breaks down how the outer loop handles the row dimensions vertically, while the inner loops control the horizontal column printing (stars, spaces, or custom shapes)[span_1](start_span)[span_1](end_span).

---

## ✨ Pattern Implementations

### 1. Square
text
***
***
***

 * **Logic & Approach:** Generates a uniform matrix where the row bounds match the column bounds (N \times N). Runs a standard outer loop for rows from 1 to N, with an inner loop running from 1 to N to unconditionally print a star (*) at every index.
 * **Dry Run (N=3):**
   * **Pass 1 (i=1):** j runs from 1 \rightarrow 3. Prints: ***
   * **Pass 2 (i=2):** j runs from 1 \rightarrow 3. Prints: ***
   * **Pass 3 (i=3):** j runs from 1 \rightarrow 3. Prints: ***
### 2. Hollow Square
text
* * *
*   *
* * *

 * **Logic & Approach:** Evaluates an N \times N matrix but filters the print statements using an edge boundary conditional check. A star (*) is drawn *only* if the element resides on the first row, last row, first column, or last column (i == 1 || i == N || j == 1 || j == N). All inner cells default to a blank space ( ).
 * **Dry Run (N=4):**
   * **Pass 1 (i=1):** Top boundary active \rightarrow Prints ****
   * **Pass 2 (i=2):** Middle row \rightarrow j=1 (Star), j=2,3 (Spaces), j=4 (Star) \rightarrow Prints *  *
   * **Pass 3 (i=3):** Middle row \rightarrow j=1 (Star), j=2,3 (Spaces), j=4 (Star) \rightarrow Prints *  *
   * **Pass 4 (i=4):** Bottom boundary active \rightarrow Prints ****
### 3. Triangle
text
*
**
***

 **Logic & Approach:** Builds a linear growing structure where row length scales linearly with the index. The outer loop ticks up from 1 to N, forcing the inner loop boundaries to evaluate dynamically based on the current row height constraint (j <= i).
 * **Dry Run (N=3):**
   * **Pass 1 (i=1):** j \le 1 \rightarrow Prints 1 star: *
   * **Pass 2 (i=2):** j \le 2 \rightarrow Prints 2 stars: **
   * **Pass 3 (i=3):** j \le 3 \rightarrow Prints 3 stars: ***
### 4. Inverted Triangle
text
***
**
*

*    **Logic & Approach:** A vertical inversion of the standard triangle. The structural logic operates by shifting the outer loop into reverse (i = N; i >= 1; i--), letting the inner loop expression j <= i continuously shrink the star counts row-by-row.
 * **Dry Run (N=3):**
   * **Pass 1 (i=3):** j \le 3 \rightarrow Prints 3 stars: ***
   * **Pass 2 (i=2):** j \le 2 \rightarrow Prints 2 stars: **
   * **Pass 3 (i=1):** j \le 1 \rightarrow Prints 1 star: *
### 5. Pyramid
text
  *
 ***
*****


 * **Logic & Approach:** Uses exact calculations for centering text block spaces relative to the current row index. For any given row i from 1 to N, the algorithm runs two independent loops sequentially:
   1. Print N - i leading filler spaces.
   2. Print 2 * i - 1 center stars (generating odd number lines: 1, 3, 5...).
 * **Dry Run (N=3):**
   * **Pass 1 (i=1):** Spaces (3-1=2), Stars (2(1)-1=1) \rightarrow   *
   * **Pass 2 (i=2):** Spaces (3-2=1), Stars (2(2)-1=3) \rightarrow  ***
   * **Pass 3 (i=3):** Spaces (3-3=0), Stars (2(3)-1=5) \rightarrow *****
### 6. Inverted Pyramid
text
 *****
  ***
   *


 * **Logic & Approach:** Flips the pyramid layout by executing the row sequence backwards from N down to 1. The core math formulas internally remain completely unchanged (N - i for leading spaces, 2 * i - 1 for center-aligned stars).
 * **Dry Run (N=3):**
   * **Pass 1 (i=3):** Spaces (3-3=0), Stars (2(3)-1=5) \rightarrow *****
   * **Pass 2 (i=2):** Spaces (3-2=1), Stars (2(2)-1=3) \rightarrow  ***
   * **Pass 3 (i=1):** Spaces (3-1=2), Stars (2(1)-1=1) \rightarrow   *
### 7. Half Diamond
text 
*
***
*****
***
*


 * **Logic & Approach:** Stitches two distinct dynamic structures together continuously. The first code component builds an upright growing triangle scaling from row 1 to N. Instantly after, a second separate outer loop executes an inverted structural triangle stepping from row N-1 back down to 1.
 * **Dry Run (N=3):**
   * **Top Half (i = 1 \rightarrow 3):** Prints *, then **, then ***
   * **Bottom Half (i = 2 \rightarrow 1):** Prints **, then *
### 8. Diamond
text
    
   *
  ***
 *****
  ***
   *
    

 * **Logic & Approach:** Creates a perfectly centered diamond figure by stacking a standard pyramid over an inverted pyramid. To avoid duplicate center lines, the top section evaluates from row 1 up to N, whereas the inverted bottom section scales down cleanly from N-1 down to 1.
 * **Dry Run (N=3):**
   * **Top Half (i = 1 \rightarrow 3):** Generates   *,  ***, *****
   * **Bottom Half (i = 2 \rightarrow 1):** Generates  ***,   *
## 🛠️ Core Concepts Learned
 * **Loop Nesting:** Mastering outer loop rows and inner loop column mechanics.
 * **Conditional Printing:** Using boundaries to craft hollow spaces and unique geometric structures.
 * **Math-Driven UI:** Using algebraic statements like N - i and 2 * i - 1 to compute layout placements on the terminal screen.


```
