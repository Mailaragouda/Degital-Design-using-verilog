# Degital-Design-using-verilog
Verilog codes and testbenches for digital design problems.

###Exploring Default Values and Bit Sizes of Verilog Data Types.

In Verilog, data types are broadly categorized into net types and variable (reg) types. Each has a default value if not explicitly initialized.

#1. Net Types (Used for Structural Connectivity)
Net types represent physical connections between hardware components. The default value for most nets is 'z (high-impedance) unless connected to a driver.













Net Type	Description	Default Value
wire	Default net type, single driver	z (High-Z)
wand	Wired-AND (multiple drivers)	z
wor	Wired-OR (multiple drivers)	z
tri	Similar to wire	z
triand	Similar to wand	z
trior	Similar to wor	z
tri0	Pull-down when not driven	0
tri1	Pull-up when not driven	1
supply0	Constant logic 0 (power rail)	0
supply1	Constant logic 1 (power rail)	1

