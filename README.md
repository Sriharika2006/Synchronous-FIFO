# Synchronous FIFO – Verilog

## Overview

This project implements a **parameterized Synchronous FIFO (First-In-First-Out) buffer** in Verilog HDL. It uses a circular buffer with read/write pointers for efficient data storage and retrieval, along with **full/empty status detection**.

The design supports configurable data width and FIFO depth, making it suitable for buffering and pipelining data in digital systems and SoCs.

---

## Module Structure

### `fifo_sync.v` – RTL Design

The RTL module consists of:

- **FIFO Memory:** Register-based circular buffer with configurable depth and data width.
- **Read/Write Pointers:** Track the current read and write positions with wrap-around logic.
- **Status Flags:** Generate `full` and `empty` signals based on FIFO state.
- **Data Control Logic:** Controls read and write operations based on enable signals and FIFO status.

### `fifo_tb.v` – Testbench

The testbench verifies the FIFO functionality by:

- Performing read and write operations.
- Checking correct **FIFO ordering** of data.
- Verifying pointer updates and wrap-around behavior.
- Testing corner cases such as **full and empty conditions**.

---

## Features

- **Synchronous single-clock design**
- Parameterizable `DATA_WIDTH` and `FIFO_DEPTH`
- Circular buffer architecture
- Pointer-based read/write addressing
- Accurate `full` and `empty` detection
- Controlled read and write operations
- Verified through simulation and waveform analysis

---

## How to Run

1. Open `fifo_sync.v` and `fifo_tb.v` in a Verilog simulator such as **ModelSim** or **EDA Playground**.
2. Set `fifo_tb` as the top-level module.
3. Run the simulation and observe:
   - Data input/output
   - Read/write pointers
   - `full` and `empty` flags
4. Use `$dumpfile` and `$dumpvars` with **GTKWave** for waveform analysis.

---

## Tools Used

- **Verilog HDL**
- **EDA Playground**
- **ModelSim**
- **GTKWave**

---

## Learning Outcomes

- Gained hands-on experience in **RTL-based FIFO design**.
- Developed an understanding of **read/write pointer logic and wrap-around**.
- Implemented **full/empty flag generation**.
- Learned RTL verification using **Verilog testbenches and waveform analysis**.
