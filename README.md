## talker-container-build

Building the Athena talker program in a container.

### Using

`docker run --rm -v ${PWD}:/code -w /code esolang/x86asm-nasm`
`x86asm-nasm hello.asm`

Compile the ASM File: Inside the container, compile the assembly file using:

`nasm -f elf64 hello.asm -o hello.o`

Link the Object File: Create an executable with:

`ld -o hello hello.o`

Run the Executable: Execute the program:

`./hello`