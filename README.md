# Roman numerals kata in Python

[![CI](https://github.com/Coding-Cuddles/roman-numerals-python-kata/actions/workflows/main.yml/badge.svg)](https://github.com/Coding-Cuddles/roman-numerals-python-kata/actions/workflows/main.yml)
[![Python 3.11+](https://img.shields.io/badge/python-3.11%2B-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Overview

This kata complements [Clean Code: Advanced TDD, Ep. 19](https://cleancoders.com/episode/clean-code-episode-19-p1).

This repository contains two exercises designed to improve your skills in
test-driven development.

## Instructions

Roman numerals are a numeral system that was used by ancient Rome. Numbers in 
this system use letters from the Latin alphabet. Currently, it uses seven symbols:

| Symbol | Value |
|:-------|-------|
| I      | 1     |
| V      | 5     |
| X      | 10    |
| L      | 50    |
| C      | 100   |
| D      | 500   |
| M      | 1000  |

Instead of writing the same letter four times, a rule for subtraction is used:
the letter is written once, then the next largest Roman numeral is written.
For example, 4 is not written as IIII, but instead as IV, because IV is V (5)
minus I (1).

In general, the values for 5, 50, and 500 are not subtracted.

### Exercise 1

The task at hand entails crafting a function `to_roman(number: int) -> str` to
convert regular Arabic numbers into Roman numerals, such as:

* 4 → IV
* 7 → VII
* 9 → IX

The lowest number you can write in Roman Numerals is number I (1). And the
largest numeral is MMMCMXCIX (3999).

### Exercise 2

In this phase, the objective is to develop a function `from_roman(number: str)
-> int` that performs the reverse conversion, transforming Roman numerals into
their corresponding Arabic digits.

## Guiding Principles

* If you don't know an existing algorithm, follow the principles of strict
  Test-Driven Development (TDD) to derive one.
* Reflect on whether the sequence in which you write tests influences the final
  design of your algorithm.
* Consider whether it's more beneficial to devise an algorithm before embarking
  on TDD, especially if you don't already know one.
* If you do know an algorithm, evaluate if it can be implemented using strict
  TDD principles.

## Prerequisites

Required:

- [Git](https://git-scm.com/downloads)
- [uv](https://docs.astral.sh/uv/getting-started/installation/)

Optional:

- [GNU Make](https://www.gnu.org/software/make/), for shorter commands. Every required task also
  has a direct `uv` command.

You do not need to install Python or pytest separately. `uv` installs a compatible Python version
and the locked project dependencies when needed.

## Set up the kata

1. Clone the repository:

   ```console
   git clone https://github.com/Coding-Cuddles/roman-numerals-python-kata.git
   ```

2. Enter the repository directory:

   ```console
   cd roman-numerals-python-kata
   ```

3. Run the existing test. Use Make when it is installed:

   ```console
   make test
   ```

   Otherwise, run pytest through `uv` directly:

   ```console
   uv run pytest test_*.py
   ```

   The first run may install Python and the project dependencies. Setup is complete when pytest
   reports `1 passed`.

   If the command fails with `uv: command not found`, install
   [uv](https://docs.astral.sh/uv/getting-started/installation/) and repeat this step.

## Work on the kata

1. Add the next behavior to `test_roman_numerals.py`, then implement it in `roman_numerals.py`.

2. Run the tests after each change. Use Make when it is installed:

   ```console
   make test
   ```

   Otherwise, run pytest through `uv` directly:

   ```console
   uv run pytest test_*.py
   ```

   Continue when the test run passes.

## Run the entry point

The repository retains `main.py` as its command-line entry point. Use Make when it is installed:

```console
make run
```

Otherwise, run it through `uv` directly:

```console
uv run python main.py
```

The command prints `Hello World!`.

## Make command reference

Make is optional. Run `make` or `make help` to list these commands in the terminal.

| Command             | Result                                  |
| ------------------- | --------------------------------------- |
| `make all`          | Run the test suite                      |
| `make help`         | List public Make targets                |
| `make run`          | Run `main.py`                           |
| `make test`         | Run the test suite                      |
| `make format`       | Format tracked Python files             |
| `make format-check` | Check formatting without changing files |
| `make clean`        | Remove generated caches                 |
