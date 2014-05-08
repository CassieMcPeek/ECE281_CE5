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


# Task 3

![alt text] (https://raw.github.com/CassieMcPeek/ECE281_CE5/master/Part3_Screenshot.JPG "Testbench Waveform")


For Part 3, I was pretty confused at first. I know I had made the correct changes to the schematic by adding a zero extend and then creating a 4 input multiplexor. The part where I had trouble was making those changes in the vhdl. Originally, I had make the correct changes to the testbench file by adding the extra insruction for the ORI function, and I needed to add the code at the end for the architecture behave for the new multiplexor. I then ran into a lot of syntax problems, which C2C Ryan Good and C2C Lim Ching Hao assisted me in fixing. After receiving some tips and review on the syntax of vhdl, I then stepped through my code line by line and found some places that I needed to add/fix issues based on the errors I was receiving while checking the syntax. I needed to add a new entity for the 4 input multiplexor, I needed to add the case statement for the ORI function, I also had to declare the component for the 4 input multiplexor and then I needed to fix the syntax for the behavioral architecture of the 4 input multiplexor. For the zero extend part, I needed to create a new entity and new component decleration, along with the behavioral architecture. Basically, I had the right idea and code in my file, I just had issues with the syntax, which C2C Good and C2C Hao assisted me with fixing. 
