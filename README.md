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
- It does not optimize on specific patterns
- Unmatched brackets are detected during runtime

## Implementation Info

- Cells wrap on 8-bit overflow and underflow
- The cell is left unchanged on EOF
- The host's native character set is used (untested)
- Negative pointers are allowed
- Input is line buffered
