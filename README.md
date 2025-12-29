## talker-container-build

Building the Athena talker program in a container.

### Using

`podman run --rm -v "$PWD":/code:ro esolang/x86asm-nasm x86asm-nasm /code/hello.s`
`x86asm-nasm hello.s`

`podman run -v `pwd`:/code:ro esolang/x86asm-nasm /code/hello.s`

`docker run -it --rm -v "$PWD":/code:ro esolang/x86asm-nasm sh`

Compile the ASM File: Inside the container, compile the assembly file using:

`nasm -f elf64 hello.s -o hello.o`

Link the Object File: Create an executable with:

`ld -o hello hello.o`

Run the Executable: Execute the program:

`./hello`