# Course Modules

This course is structured into modules that progressively build your understanding of digital electronics. Each module contains exercises (short, focused learning tasks) and a project (where you combine everything into a working build).

---

## Module 1: Cascading Decade Counter

**Goal**: Build a multi-digit counter that displays numbers on 7-segment displays

### Exercises
1. **LEDs and Basic Circuits**
   - Learn about voltage, current, and resistance
   - Wire up your first LED circuit
   - Understand breadboards and DIP chips
   - Safety and component handling

2. **Binary to Decimal**
   - How binary numbers work
   - Introduction to IC chips and counters
   - Reading datasheets
   - The CD4026/CD4017 decade counter IC

3. **Counters and Displays**
   - Clock signals and rising/falling edges
   - 7-segment displays and how they work
   - Connecting counters to displays
   - Understanding carry bits

### Project: Cascading Decade Counter
Build a multi-digit counter (00-99) using CD4026 ICs, 7-segment displays, and push-button inputs. Watch your circuit count up with each button press.

**Skills you'll gain**: Circuit wiring, IC pinouts, signal flow, basic troubleshooting

---

## Module 2: Compact Digital Clock

**Goal**: Build a fully functional digital clock with accurate timekeeping

### Exercises
1. **Debouncing**
   - Why buttons "bounce" and how it affects circuits
   - Capacitors and RC circuits
   - Building a debounce circuit
   - Testing your debounced counter

2. **Timing Circuits**
   - Crystal oscillators vs RC timers
   - The 555 timer IC in astable mode
   - Generating precise clock signals
   - Frequency and period calculations

3. **Reset Logic**
   - Using diodes for reset detection
   - Logic gates for custom reset values
   - Building a 60-second and 60-minute counter
   - Cascading reset logic

### Project: Compact Digital Clock
Build a 4-digit digital clock (HH:MM format) using CD4026 counters, 555 timer for 1Hz clock signal, and reset logic to handle 24-hour time. Add buttons to set hours and minutes.

**Skills you'll gain**: Timing circuits, reset logic, multi-stage systems, practical timekeeping

---

## Module 3: Binary Counters and Registers

**Goal**: Understand binary counting and data storage

### Exercises
1. **Binary Counters**
   - CD4040 binary counter
   - Reading binary on LEDs
   - Frequency division
   - Binary vs BCD counting

2. **Flip-Flops**
   - D and T flip-flop behavior
   - Building counters from flip-flops
   - Synchronous vs ripple counters
   - Clock timing and propagation delay

3. **Register Files**
   - What registers are and why we need them
   - Building a 4-bit register
   - Load and hold operations
   - Data storage fundamentals

### Project: Flip-Flop Clock
Build a digital clock using only D flip-flops (74LS107N) and logic gates - no pre-made counter ICs allowed. Decode the binary output to 7-segment displays using a 7446 decoder.

**Skills you'll gain**: Sequential logic, flip-flop design, binary-to-BCD conversion

---

## Module 4: Decoders and Combinational Logic

**Goal**: Design custom logic circuits using gates and lookup tables

### Exercises
1. **Logic Gates**
   - AND, OR, NOT, NAND, NOR, XOR gates
   - Truth tables and Boolean algebra
   - Building a 7-segment decoder from gates
   - Logic simplification

2. **EEPROM Lookup Tables**
   - Using EEPROMs (28C256) as programmable logic
   - Programming an EEPROM
   - Address-to-data mapping
   - Custom character displays

3. **Multiplexing**
   - Time-division multiplexing
   - Driving multiple 7-segment displays
   - Reducing pin count
   - Persistence of vision

### Project: Custom Display System
Build a decoder that drives multiple 7-segment displays using an EEPROM as a lookup table and multiplexing to reduce wiring complexity.

**Skills you'll gain**: Combinational logic, memory programming, multiplexing

---

## Module 5: Arithmetic Circuits

**Goal**: Build circuits that perform mathematical operations

### Exercises
1. **Binary Arithmetic**
   - Number systems (decimal, binary, hexadecimal)
   - Signed numbers (two's complement)
   - Addition and subtraction in binary
   - Overflow and carry

2. **Adders**
   - Half adder logic (XOR + AND)
   - Full adder with carry
   - 4-bit ripple adder
   - Carry propagation

3. **ALU Basics**
   - Introduction to the 74181 ALU
   - Arithmetic vs logic operations
   - Function selection
   - Multi-function digital blocks

### Project: 4-bit Calculator
Build a simple calculator using 74283 adder ICs that can add two 4-bit numbers and display the result on 7-segment displays. Add an accumulator register to store results.

**Skills you'll gain**: Arithmetic logic, ALU design, accumulators

---

## Module 6: Advanced Arithmetic

**Goal**: Build more complex calculation circuits

### Exercises
1. **Accumulator Design**
   - Register + adder integration
   - Storing intermediate results
   - Multi-step calculations
   - CPU-style datapath

2. **Signed Arithmetic**
   - Working with negative numbers
   - Two's complement addition/subtraction
   - Sign extension
   - Overflow detection

3. **BCD Arithmetic**
   - Binary-coded decimal vs binary
   - BCD addition rules
   - Decimal adjust logic
   - Multi-digit BCD

### Project: Signed Calculator
Enhance your calculator to handle signed numbers (positive and negative), display the sign, and detect overflow conditions.

**Skills you'll gain**: Signed arithmetic, BCD operations, error detection

---

## Module 7: Memory Systems

**Goal**: Understand how memory works and integrate it into circuits

### Exercises
1. **Memory Fundamentals**
   - Volatile vs non-volatile memory
   - Address and data buses
   - Read and write operations
   - Memory timing

2. **EEPROM Programming**
   - Writing data to EEPROM
   - Building an EEPROM programmer
   - Memory mapping
   - Data persistence

3. **Memory-Based Logic**
   - Using memory as a lookup table
   - ROM-based state machines
   - Stored program concepts
   - Firmware basics

### Project: Programmable Display
Build a system that stores custom patterns in EEPROM and displays them on an LED matrix or 7-segment display array. Program different patterns and switch between them.

**Skills you'll gain**: Memory operations, data storage, programmable systems

---

## Module 8: Introduction to Microcontrollers

**Goal**: Bridge from discrete logic to programmable systems

### Exercises
1. **Microcontroller Basics**
   - ATmega328P overview
   - GPIO pins and digital I/O
   - Programming in assembly/C
   - Uploading code

2. **Interfacing with Displays**
   - Controlling 7-segment displays from a microcontroller
   - Pin mapping and bit manipulation
   - Multiplexing in software
   - Timing loops

3. **Interrupts and Timing**
   - Hardware interrupts
   - Timer/counter peripherals
   - Accurate timekeeping
   - Event-driven programming

### Project: Microcontroller Clock
Build a digital clock using an ATmega328P microcontroller to drive your 7-segment displays. Compare this approach with your discrete logic clocks.

**Skills you'll gain**: Microcontroller programming, software-hardware interface

---

## Modules 9-12: Final Project

**Goal**: Design and build your own digital system

Choose from these projects or propose your own:

### Game Projects
- **Tetris**: Build Tetris on an LED matrix with button controls
- **Connect 4**: Two-player game with LED display
- **Snake Game**: Classic snake on a dot matrix
- **Pong**: Simple paddle game

### Display Projects  
- **Giant Digital Clock**: Large 6-digit clock with alarm
- **P10 LED Panel Clock**: Full-color scrolling text and time
- **8x8 LED Matrix Display**: Animated patterns and text

### Calculator Projects
- **Base Converter**: Convert between binary, decimal, hex
- **Ternary Calculator**: Work in base-3
- **Scientific Calculator**: Add multiplication and division

### Creative Projects
- **Password Lock**: Keypad entry system with lock mechanism
- **Candy Crush**: Match-3 game on LED grid
- **Custom Design**: Propose your own digital system!

### Project Requirements
- Uses concepts from at least 3 different modules
- Includes both input and output
- Demonstrates understanding of timing, logic, or memory
- Is fully functional and debugged
- Includes documentation of your design process

**Final deliverables**:
- Working circuit on breadboard
- Circuit schematic/diagram
- Component list and datasheets
- Demo video showing functionality
- Written explanation of how it works

---