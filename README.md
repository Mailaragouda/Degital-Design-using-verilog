# Degital-Design-using-verilog
Verilog codes and testbenches for digital design problems.

###Exploring Default Values and Bit Sizes of Verilog Data Types.

In Verilog, data types are broadly categorized into net types and variable (reg) types. Each has a default value if not explicitly initialized.

##I.Net Type

#1.wire

- Default net type and by default it is single bit unsigned.
- The default size always 1bit.
- Can be used as multibit vector also.
- fully fully synthesizable net type.
- If we use signed keyword, then it takes signed values. The range of signed wire is same as the range of 2's compliment.

#2.wand

- type: Wired-AND.
- Default behavior: Like wire, it is also single-bit and unsigned by default.
- Multibit support: Can be used as a multibit vector.
- Signed support: If declared with signed, it holds signed values. The range follows 2's complement.
- Behavior: Multiple drivers drive the net, and the result is a bitwise AND of all drivers.

#3. wor

- Net type: Wired-OR.
- Default behavior: Like wire, it is also single-bit and unsigned by default.
- Multibit support: Can be used as a multibit vector.
- Signed support: If declared with signed, it holds signed values. The range follows 2's complement.
- Behavior: Multiple drivers drive the net, and the result is a bitwise OR of all drivers.
  
#4.supply0 and supply1 in Verilog

- Net Type: Both are special net types used to represent constant logic levels.
- supply0 = constant logic 0
- supply1 = constant logic 1
- Default Width: Always 1-bit

Value:
- supply0 is always 0
- supply1 is always 1

- Driving Strength: Both have the strongest possible drive strength in Verilog. Cannot be overridden by any other driver.
- Signed Support: Not applicable, as the value is always fixed (0 or 1)
- Multibit Support: Not used as multibit vectors.
- Typically used for modeling power and ground connections.
- Useful in low-level designs or power-aware simulations.
- Synthesizability: Generally not synthesizable, used mainly for simulation purposes.

##II.Reg type

#1. reg

- A data type (not a net) used to store values in procedural blocks (always, initial, etc.).
- By default, it is 1-bit unsigned.
- Can be declared as a multibit vector.
- If declared with the signed keyword, it can hold signed values (2's complement range).
- Used to model storage elements (like flip-flops) in synthesis.

#2. integer

- A signed 32-bit data type used to represent whole numbers.
- Cannot be declared as a vector or with explicit bit width.
- Default range: −2³¹ to +2³¹−1
- Used for loop counters, general calculations, and non-synthesizable tasks like testbenches.
- Not synthesizable in most cases; use logic signed [31:0] for RTL design.

#3. real

- Represents floating-point numbers.
- Used for modeling real-world values (like voltages, delays) in testbenches and simulations.
- Cannot be assigned in procedural assignments using blocking (=) or non-blocking (<=) — special functions are used instead.
- Not synthesizable; purely for simulation purposes.

#4. time

- A 64-bit unsigned integer data type.
- Used to store simulation time values (usually in time units like ns, ps, etc.).
- Mainly used for timing analysis or delay calculations in simulation.
- Not synthesizable; only used in testbenches or debugging.

#5. realtime

- A 64-bit real (floating-point) type.
- Similar to time but stores time values as floating-point for higher precision.
- Useful when sub-timeunit accuracy is needed in simulations.
- Not synthesizable; used only in simulation.

#simulation output

![Screenshot 2025-04-14 152246](https://github.com/user-attachments/assets/fc0dab6e-33b6-4259-a25c-ff62af3cc408)

