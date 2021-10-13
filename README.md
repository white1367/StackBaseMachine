# StackBaseMachine

## Description
Stack-base machine is a kind of CPU design architecture which sometimes be compared with register-based machine. Unlike register-based machine which used 3 address code taking 1 opcode and 2 corresponding operands e.g. add %eax, 3, stack based machine was designed with opcode with one or zero operand and one long stack which served as registers to take temporary value in calculation.
This is a project writen in lex and bison syntax. It check the input is valid or not. If valid, it returns the result. If invalid, it returns "Invalid format"

## Compile
run make.sh to generate executable file.
```
$ ./make.sh
```

## Test Case
#### Sample Input
```
load 1 
load 2 
sub 
load 5 
mod
```
#### Sample Output
```
0
```
#### Explanation
```
5 % (2-1) = 0
```

#### Sample Input
```
load 3 
load 4 
inc 
inc
```
#### Sample Output
```
Invalid format
```
#### Explanation
```
If after finish the program, there are more than 1 numbers in the stack it will be consider invalid.
```

#### Sample Input
```
load 1 
load 1 
add 
sub
```
#### Sample Output
```
Invalid format
```
#### Explanation
```
No enough operands in stack to perform sub.
```
