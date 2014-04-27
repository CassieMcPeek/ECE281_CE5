ECE281_CE5
==========

MIPS

# Task #1: Simple MIPS Assembly Program

This is to code to complete task 1:
  addi $S0, $0, $44 - this line will assign the 16-bit constant (decimal value of 44) to the register S0
  addi $S1, $0, $-37 - this line will assign the 16-bit constant(decimal value of -37) to the register S1
  add $S2, $S1, $S0 - this line will add the values from registers S0 and S1 and store the result in register S2
  sw $S2, 0X54($0) - this line will store the value of register S2 into the hexadecimal memory address x54.
  
I am not sure if this is the correct syntax, but I just followed the example 6.10 in the book so I think I am at least close to the 
correct format.
