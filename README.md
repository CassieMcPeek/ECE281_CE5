ECE281_CE5
==========

MIPS

# Task #1: Simple MIPS Assembly Program

This is to code to complete task 1:
  
  addi $S0, $0, 44 - this line will assign the constant (decimal value of 44) to the register S0
  
  addi $S1, $0, -37 - this line will assign the constant(decimal value of -37) to the register S1
  
  add $S2, $S1, $S0 - this line will add the values from registers S0 and S1 and store the result in register S2
  
  sw $S2, 0X54($0) - this line will store the value of register S2 into the hexadecimal memory address x54.
  
I am not sure if this is the correct syntax, but I just followed the example 6.10 in the book so I think I am at least close to the 
correct format.

# Task 2: Machine Code

  addi $S0, $0, 44 put into hexadecimal code would be 0X2010 002C
  
  addi $S1, $0, -37 put into hexadecimal code would be 0X2011 FFDB
  
  add $S2, $S1, $S0 put into hexadecimal code would be 0X0211 9020
  
  sw $S2, 0X54($0) put into hexadecimal code would be 0XAC12 0036
  
  
I created the testbench and added the proper instructions based on the code above. I then analyzed the waveform and found that it worked properly. I know this because in the screenshot below, the value of 44 is stored into memory part (16), which based on the book is register S0. The value of -37 was stored into (17), which is register S1 and the summation of those two values is stored into register S2, which is (18) in the screenshot. This proves that my machine code above is correct.

![alt text] (https://raw.github.com/CassieMcPeek/ECE281_CE5/master/Testbench_waveform_screenshot.JPG "Testbench Waveform")
