# EE-469
# Intro
This code is a simple RISC-V CPU that is capable of running 
simple Fibonacci code.

# Tool use
The format of the code in this file is SystemVerilog, and 
the simulation software used is ModelSim from Microsoft's 
Quartus.

# supported instruction
The code below is the assembly code converted from the txt
file in the instruction memory of this article. This document 
can support instructions such as addi, sub, jr, ret, beq, etc.
```bash
fib: addi sp,sp,-16
     ra,12(sp)SW
     SWs0,8(sp)
     addi s0,a0,0
     addi te,zero,2
     blts0,te,if
else:
     SWs1,4(sp)
     addi a0,s0,-1
     jalra, fib
     adds1,a0,zero
     addi a0,s0,-2
     jalra, fib
     adda0,s1,a0
     lws1,4(sp)
     Iws0,8(sp)
     ra,12(sp)lw
     addi sp,sp,16
     ret
if:
     addi a0,zero,1
     Iws0,8(sp)
     lwra,12(sp)
     addi sp,sp,16
     ret
``
## Contributing

Pull requests are welcome. 

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
