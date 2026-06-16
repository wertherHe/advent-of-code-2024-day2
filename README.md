# Advent of Code 2024 - Day 2: Red-Nosed Reports

This repository contains my Python solution for [Advent of Code 2024 Day 2](https://adventofcode.com/2024/day/2), completed in a Jupyter Notebook.

The challenge is to analyze a list of numerical reports and determine how many reports are considered safe.

## Problem Summary

Each report is a row of numbers called levels. A report is considered safe if:

1. The levels are either strictly increasing or strictly decreasing.
2. The difference between any two adjacent levels is at least 1 and at most 3.

In Part 2, the challenge introduces the **Problem Dampener**, which allows one level to be removed from a report. If removing a single level makes the report safe, that report also counts as safe.

## Solution Approach

The notebook follows three main steps:

1. **Read the input file**

   The input file `input.txt` is read line by line. Each line is converted into a list of integers, and all reports are stored in a list of lists.

2. **Solve Part 1**

   The function `is_safe(report)` checks whether a report is strictly increasing or strictly decreasing, while also making sure every adjacent difference is between 1 and 3.

3. **Solve Part 2**

   The function `is_safe2(report)` first checks whether the report is already safe. If not, it tries removing each level one at a time and checks whether the remaining report becomes safe.

## Files

* `day2_solution.ipynb` — Jupyter Notebook containing the full solution
* `input.txt` — Advent of Code input file, placed in the same folder as the notebook

Note: The personal puzzle input is not included in this repository. To run the notebook, add your own `input.txt` file from Advent of Code.

## How to Run

1. Clone this repository.
2. Place your Advent of Code Day 2 input in a file named `input.txt`.
3. Open `day2_solution.ipynb`.
4. Run all cells in order.

The notebook will print:

* the number of safe reports for Part 1
* the number of safe reports with the Problem Dampener for Part 2

## Key Functions

### `is_safe(report)`

Checks whether a report is safe under the original rules.

### `is_safe2(report)`

Checks whether a report is safe under the updated Part 2 rules, where one bad level can be removed.

## Result

The notebook successfully solves both parts of Advent of Code 2024 Day 2.
