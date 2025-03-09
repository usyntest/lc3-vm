# LC-3 Virtual Machine

This repository contains an implementation of the **LC-3 (Little Computer 3) Virtual Machine**, a 16-bit educational computer architecture. This project is inspired by [this blog post](https://www.jmeiners.com/lc3-vm/) and structured with guidance from [this repository](https://github.com/jsawruk/lc3-vm).

## Features
- Implements the **LC-3 instruction set**, including arithmetic, memory operations, and control flow.
- Supports **TRAP routines** for input and output operations.
- Uses a **fetch-execute cycle** to process LC-3 machine code.
- Implements **computed GOTO for faster instruction dispatch**.
- Supports loading and executing **LC-3 object files**.

## Installation

Ensure you have a C compiler and CMake installed. If not, install them:

```sh
sudo apt update && sudo apt install build-essential cmake
```

## Building the Project

Clone the repository and build the project using CMake:

```sh
git clone git@github.com:usyntest/lc3-vm.git
cd lc3-vm
mkdir build && cd build
cmake ..
make
```

## Running the Virtual Machine

Once built, you can run an LC-3 object file:

```sh
./lc3 ../images/2048.lc3
```

## File Structure
- `lc3.c` – Main entry point; implements the **fetch-execute cycle**.
- `instruction-set.c` – Implements the **LC-3 instruction set**.
- `instruction-set.h` – Header file for LC-3 instructions.
- `core/` – Contains utility functions for bit manipulation, input buffering, and reading object files.
