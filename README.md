# Roman numerals kata in Python

[![CI](https://github.com/Coding-Cuddles/roman-numerals-python-kata/actions/workflows/main.yml/badge.svg)](https://github.com/Coding-Cuddles/roman-numerals-python-kata/actions/workflows/main.yml)
[![Replit](https://replit.com/badge?caption=Try%20with%20Replit&variant=small)](https://replit.com/new/github/Coding-Cuddles/roman-numerals-python-kata)

## Overview

This kata complements [Clean Code: Advanced TDD, Ep. 19](https://cleancoders.com/episode/clean-code-episode-19-p1).

This repository contains two exercises designed to improve your skills in
test-driven development.

## Instructions

The Romans demonstrated remarkable ingenuity, leaving a lasting legacy with
many innovations. However, one numerical concept they never grasped was the
concept of zero. This absence posed a unique challenge when chronicling their
historical feats, yet their numeral system, which employed letters like I, V,
X, L, C, D, and M, endures in modern usage.

### Exercise 1

The task at hand entails crafting a function `to_roman(number: int) -> str` to
convert regular Arabic numbers into Roman numerals, such as:

* 1 --> I
* 10 --> X
* 9 --> IX
* 7 --> VII

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
* If you do knows an algorithm, evaluate if it can be implemented using strict
  TDD principles.

## Usage

You can import this project into [Replit](https://replit.com), and it will
handle all dependencies automatically.

### Prerequisites

* [Python 3.8+](https://www.python.org/)
* [pytest](https://pytest.org)

### Run main

```console
make run
```

### Run tests

```console
make test
```
