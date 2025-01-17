![image](https://github.com/user-attachments/assets/296cb791-b48d-4e10-aee8-7bafbc86806a)Task 1:Task is to install all the essential tools required for this samsung-RISCV Workshop such as Ubuntu on VMBox & refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler

Install Ubuntu 20.04 LTS on Oracle Virtual Machine Box
Firstly, I have downloaded the virtual box from the links provided to us and loaded a linux version with image dock file sent
Ubuntu and VMBox Installation



C Language based LAB
I have successfully run the virtual machine and compiled the tasks.

Initial task is:-

write a program to compile the sum of first 5 natural numbers in c:
we have written the code sum of 1st 5 numbers in leafpad as shown below.

gcc sum_1ton.c

./a.out
this code will be run in terminal to get output as 15 for 1st 5 numbers as shown below :

image

RISCV based LAB
Using the cat command, the entire C code will be displayed on the terminal.
image

A program is run to obtain risc-v version of the code previously written in c:

riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
image

As the whole version of above code looks lengthier we have used below code to make it shorter

riscv64 -unknown-elf-objdump -d sum1ton.o | less
& we have obtained the required main part to compare the execution in assembly language as shown below :

image

Open the same terminal and run the given command:

riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
image

As the whole version of above code looks lengthier as earlier we have used below code to make it shorter

riscv64 -unknown-elf-objdump -d sum1ton.o | less
& we have obtained the required main part to compare the execution in assembly language as shown below :

image

End of 1st task
