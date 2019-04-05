# brainbash

A brainfuck interpreter written in pure Bash

```shell
$ brainbash examples/numwarp.b
123
    /\
     /\
  /\  /
   / 
 \ \/
  \
   
```

## Program Info

- It reads from a file named in the first argument
	- If there are no arguments, it reads from standard input
- It only depends on Bash 4+ and is portable
	- A patch for Bash 3.2+ support is also available
		- It reads from `/dev/stdin` if there are no arguments
		- It cannot decrement the pointer below zero
- It does not optimize on specific patterns
- Unmatched brackets are detected during runtime

## Implementation Info

- Cells wrap on 8-bit overflow and underflow
- The cell is left unchanged on EOF
- Negative pointers are allowed
- Input is line buffered
- Output is encoded in ASCII
