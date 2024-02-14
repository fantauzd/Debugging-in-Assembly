
Create a project directory (this template project will work to begin with) and open the solution in Visual Studio.
Download DebugLab.asm Download DebugLab.asmand add it to the project (and remove any other .asm files in the project).
Set a breakpoint on the last line of code within the main procedure, Invoke ExitProcess, 0.
This can be done either by clicking in the far-left margin next to this line of code, or by getting the cursor on this line of code and using the keyboard shortcut (F9)
Run the program in debugging mode (F5).
Ensure the following debug-mode windows (and options) are enabled. The video will help with this.
Registers (Enable CPU, Flags, and Effective Address)
At least one Memory window
At least one Watch window
Clear all existing Watches (Right click in the Watch Window, Clear All)
Disassembly
Breakpoints (Debug->Windows->Breakpoints)
Take a screenshot of your IDE state. Do not include the terminal window (The window that pops up to print the program’s output).
Part 1 Questions
As you answer these questions, please circle (on your screenshot) the location where you found the answers.

What is the current value (in Hex) of the EAX Register?
What is the current state (Set/Clear) of the following flags: Carry, Overflow, Zero, Sign?
 

Part 2 - Navigating Code and Procedures
Now that we know everyone has the same configuration, let’s work a bit on navigating through code using breakpoints and stepping. This program has a simple procedure called greetUser. We haven’t dealt with procedures in the class yet so this procedure is kept simple. Procedures are much like functions in that program flow shifts into a procedure from a CALL statement, and returns back with a RET statement.

If you’re still in debugging mode, stop debugging (Click the “Stop” button or Shift+F5).
Delete all breakpoints
Set a new breakpoint on the CALL greetUser line.
Start Debugging (F5)
The program should pause execution just before executing the CALL greetUser instruction.
Make sure the Registers window is visible, then 'Step Into' the greetUser procedure (F11) and continue stepping (F10 or F11) until the yellow arrow (which indicates the next instruction to be executed) is pointing at CALL WriteHex.
Check the Registers window for the current value of EAX. It should be red (indicating the previous instruction changed its value) and show: 00000064.
This is the current hexadecimal value of the EAX register.
Change the last three digits to the last three digits of your OSU ID number.
You may change the current value of registers in the Registers window by clicking on the value in the Registers debugging window and typing a new value.
(To find your OSU ID number, go to https://my.oregonstate.edu/ then select the "Resources" tab. Search for (and open) "Display OSU ID".)
Step to the next instruction (F10)
This will print out your user number in the console window.
Position your terminal window so it and your debugging environment’s Registers and Editor (DebugLab.asm) windows are all visible at the same time, and take a screenshot!
This will be used in the lab report.
