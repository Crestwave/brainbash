# brainbash

A brainfuck interpreter in pure Bash

## Program Info

- It reads from a file named in the first argument
	- If there are no arguments, it reads from standard input
- It only depends on Bash 4+ and is designed to be portable
- It does not optimize on specific patterns

## Implementation Info

- Cells are 8-bit
- Cells wrap on overflow and underflow
- The cell is left unchanged on EOF
- The host's native character set is used (untested)
- Negative pointers are allowed 
- Input is line buffered
