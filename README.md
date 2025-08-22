# 🖥️ SystemVerilog Examples & Concepts  

This repository contains **SystemVerilog coding examples and exercises**, developed as part of learning and practice during the **NXP Women In Tech (WIT) training**.  
Each code demonstrates **key SystemVerilog features** including OOP concepts, constraints, randomization, queues, dynamic arrays, FSM-based packets, and more.  

---

## 📚 Table of Contents
1. [Ethernet Packet Class](#1-ethernet-packet-class)  
2. [Queue Operations](#2-queue-operations)  
3. [Dynamic Array Usage](#3-dynamic-array-usage)  
4. [Inheritance Example](#4-inheritance-example)  
5. [Random Number Generation](#5-random-number-generation)  
6. [Constraints with Payload](#6-constraints-with-payload)  
7. [Constraint Conflict](#7-constraint-conflict)  
8. [Scope Resolution Operator](#8-scope-resolution-operator)  

---

## 1. Ethernet Packet Class  
- Models an **Ethernet packet (eth_pkt)** with fields: `da`, `len`, `payload`, `crc`.  
- Implements **randomization** for fields, CRC calculation, and a **print() method** for cleaner display.  
- Demonstrates **class instantiation, constraints, and methods** in SystemVerilog.  

---

## 2. Queue Operations  
- Declares an **unbounded queue** `Q1`.  
- Demonstrates:  
  - Initializing with values  
  - Push from back (manual + built-in)  
  - Extracting values  
  - Inserting at any location  
  - Simulating **FIFO** behavior with `pop_front()`  

---

## 3. Dynamic Array Usage  
- Demonstrates **dynamic memory allocation** in SystemVerilog.  
- Steps:  
  - Allocate memory for 10 values  
  - Fill with random numbers  
  - Resize to 20 while preserving old values  
  - Display all values  

---

## 4. Inheritance Example  
- `eth_pkt` class → base class  
- `eth_good_pkt` → derived class with additional field `count_good`  
- Demonstrates:  
  - **Inheritance**  
  - `super.print` for reusability  
  - `this` and `super` keyword usage  

---

## 5. Random Number Generation  
- Generates **100 random numbers between 1–100**:  
  - With repetitions  
  - Without repetitions (using `randc` and `shuffle()`)  

---

## 6. Constraints with Payload  
- Demonstrates **automatic allocation of payload size** using constraints inside a class.  
- Payload length randomized between 41–49 bytes.  
- Shows how constraints simplify memory allocation in dynamic arrays.  

---

## 7. Constraint Conflict  
- Demonstrates what happens when **conflicting constraints** are applied.  
- Example: payload size `<40` and `>50` at the same time → randomization fails.  
- Introduces `assert(pkt.randomize())` for validation.  

---

## 8. Scope Resolution Operator  
- Demonstrates usage of **scope resolution (`::`)** to access fields in nested classes.  
- Example: accessing `eth_pkt::m_pkt::count`.  

---

## 🚀 How to Run  
1. Clone this repository:
   ```bash
   git clone https://github.com/Sindhu-Yesilanka/System_verilog_examples-and-concepts.git
   cd System_verilog_examples-and-concepts
