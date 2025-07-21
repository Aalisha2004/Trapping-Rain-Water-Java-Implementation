# Trapping Rain Water – Java Implementation

## Overview

This Java program calculates the total amount of **trapped rainwater** between bars in a histogram. It uses an efficient approach by precomputing the **left max** and **right max** boundaries for each bar to determine how much water can be trapped at each position.

This is based on the **"Trapping Rain Water"** problem commonly found in coding interviews and competitive programming platforms.

---

## How It Works

Given an array of non-negative integers where each element represents the height of a bar, the algorithm:

1. Computes an array `leftMax[]` where each element holds the maximum height to the **left** (including itself).
2. Computes an array `rightMax[]` where each element holds the maximum height to the **right** (including itself).
3. For each bar, calculates the **water level** as `min(leftMax[i], rightMax[i])`.
4. Computes **trapped water** at that index as `waterLevel - height[i]`.
5. Sums up trapped water for all bars.

---

## Code File

`TrapppingWater.java`

## Example

**Input:**

```java
int height[] = {4, 2, 0, 3, 2, 5};
```

**Output:**

```
9
```

**Explanation:**

Visual representation:

```
|
|        |       
|   |    |   |   |
|   | |  | | | | |
-------------------
[4, 2, 0, 3, 2, 5]
```

Total water trapped = 9 units

---

## How to Compile and Run

### Compile:

```bash
javac TrapppingWater.java
```

### Run:

```bash
java TrapppingWater
```

---

## Time and Space Complexity

* **Time Complexity:** O(n)
* **Space Complexity:** O(n) for leftMax and rightMax arrays

