# adding custom instruction to riscv-compiler

[riscv-gnu-toolchain](https://github.com/riscv-collab/riscv-gnu-toolchain)

add custom instruction by looking at the custom-riscv.patch file.

after adding, build by

``` for 32 bit
./configure --prefix=/opt/riscv --with-arch=rv32gc --with-abi=ilp32d
make linux
```

confirm with,

```
riscv32-unknown-elf-gcc -Os custom.c -o custom
riscv32-unknown-elf-objdump -d custom | grep custom
```

# another way to compile custom instruction
also, see the inline-custom.png file to compile the custom instruction without modifying the compiler.
