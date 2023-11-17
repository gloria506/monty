0x19 Stacks, Queue - LIFO,  FIFO

---

**The Monty Language**

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (similar to Python). The project aims to create an interpreter for Monty ByteCodes files.

**Author**
- @gloria506

**Requirements For Building Project**
- Allowed editors: vi, vim, emacs
- All files compiled on Ubuntu 20.04 LTS using gcc, with options -Wall -Werror -Wextra -pedantic -std=c89
- All files should end with a new line
- Mandatory README.md file at the project's root
- Code should follow the Betty style, checked using betty-style.pl and betty-doc.pl
- Maximum of one global variable
- No more than 5 functions per file
- Allowed to use the C standard library
- Prototypes of all functions should be in the header file named monty.h
- Don't forget to push your header file
- Header files should be include guarded.

**Usage/Examples/Compilation**
Compile using:
```bash
$ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty
```

**Monty Bytecode Files**
Files have a .m extension. Each line contains one instruction. There can be any number of spaces before or after the opcode and its argument. Blank lines are allowed.

**The Monty Program**
Example:
```bash
$ cat -e tryingbytecodes/00.m
push 1$
push 2$
push 3$
pall
$ ./monty tryingbytecodes/00.m
3
2
1
```

**Running Tests After Compiling**
Run tests using:
```bash
./monty </path/to bytecodefile>
```

**Running With Valgrind**
To check for memory leaks:
```bash
valgrind ./monty <path/to bytecodefile>
```

**Opcode Usage**
- push \<integer\> OR \<opcode\>
- pall: Prints all elements from the stack.
- pint: Prints the value of the top value on the stack.
- pop: Removes the top element from the stack.
- swap: Swaps the top two elements from the stack.
- nop: Does nothing.
- pchar: Prints the char at the top of the stack.
- pstr: Prints the string starting at the top of the stack.
- rotl: Rotates the stack to the top.
- rotr: Rotates the stack to the bottom.
- stack: Sets the format of the data to a stack (LIFO).
- queue: Sets the format of the data to a queue (FIFO).

**Arithmetic**
- add: Adds the top two elements from the stack.
- sub: Subtracts the first and second elements from the stack.
- div: Divides the second top element of the stack by the top element of the stack.
- mul: Multiplies the second top element of the stack by the top element of the stack.
- mod: Computes the rest of the division of the second top element of the stack by the top element of the stack.
